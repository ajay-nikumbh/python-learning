# Chapter 02 — Setup and First Program

Chapter 01 was theory. This chapter is hands-on: you install Python, learn the tools, and write code that actually runs.

The goal is a working feedback loop — write, run, read the output, change something, run again. Everything after this chapter depends on you having that loop.

**By the end of this chapter you will be able to:**

- Install Python and confirm which interpreter you are running
- Use the REPL to answer questions in seconds instead of writing files
- Set up an editor that catches mistakes as you type
- Write and run a script that takes input, decides, and reports
- Create a virtual environment and explain why it matters
- Install packages with `pip` without breaking anything
- Lay out a Python file the way every professional project does

---

## 02.1 Installing Python

Most machines already have Python — often several. The problem is rarely "is it installed?" and usually "which one am I running?"

### Knowing which Python you have

One line settles it:

```python
import sys
print(sys.executable)
```

That prints the full path of the interpreter running your code. Whenever something behaves strangely — a package you installed is missing, a feature does not exist — this is the first thing to check.

For version checks in code, use `sys.version_info`, which compares cleanly against a tuple:

```python
# Reads naturally, because tuples compare element by element.
if sys.version_info >= (3, 12):
    ...
```

### Installing, per platform

<table width="100%">
<tr><th align="left" width="14%">Platform</th><th align="left" width="43%">How</th><th align="left" width="43%">Verify</th></tr>
<tr><td><b>Windows</b></td><td>Installer from python.org — <b>tick "Add python.exe to PATH"</b></td><td><code>python --version</code></td></tr>
<tr><td><b>macOS</b></td><td>Installer from python.org, or <code>brew install python@3.12</code></td><td><code>python3 --version</code></td></tr>
<tr><td><b>Linux</b></td><td><code>sudo apt install python3 python3-venv python3-pip</code></td><td><code>python3 --version</code></td></tr>
</table>

The Windows PATH checkbox is the single most common setup mistake. Miss it and the `python` command will not be found at all.

### `python` vs `python3`

On macOS and Linux the command is usually `python3`. On Windows it is usually `python`.

This is historical: `python` used to mean Python 2, so Unix systems kept `python3` explicit rather than break existing scripts. macOS also reports its platform name as **Darwin**, which surprises people the first time they see it.

---

## 02.2 The Interpreter and the REPL

The **REPL** — Read, Evaluate, Print, Loop — is an interactive session. Type an expression, press Enter, see the result.

It is the fastest way to answer "what does this do?" Start it with `python3`, leave it with `exit()` or Ctrl-D.

### The one difference that confuses beginners

In the REPL, an expression displays its value automatically. In a **file**, it does not — you must `print()` it.

```python
>>> 2 + 3        # REPL: displays 5
5
```

```python
2 + 3            # In a file: computes 5, then throws it away
print(2 + 3)     # In a file: displays 5
```

### Why some lines show nothing

An **expression** produces a value, so the REPL shows it. A **statement** performs an action, so there is nothing to show.

```python
>>> 2 + 3          # expression -> displays
5
>>> x = 5          # statement  -> displays nothing
>>> import math    # statement  -> displays nothing
```

Functions with no `return` give back `None`, which the REPL deliberately hides. That is why those lines look empty too.

### The three tools for exploring

<table width="100%">
<tr><th align="left" width="18%">Tool</th><th align="left" width="38%">Answers</th><th align="left" width="44%">Example</th></tr>
<tr><td><code>help(x)</code></td><td>How do I use this?</td><td><code>help(str.strip)</code></td></tr>
<tr><td><code>dir(x)</code></td><td>What can this do?</td><td><code>dir(list)</code></td></tr>
<tr><td><code>type(x)</code></td><td>What am I holding?</td><td><code>type(value)</code></td></tr>
</table>

`dir()` is how you discover methods without looking anything up. Filter out the dunder names and what remains is the practical vocabulary of that type.

### The underscore

Inside the REPL, `_` holds the last result:

```python
>>> 10 * 5
50
>>> _ + 2        # _ is 50
52
```

This works in the REPL only — `_` is not special inside a file.

---

## 02.3 Editors and IDEs

You can write Python in Notepad. You should not.

A good editor catches mistakes as you type, shows what a function expects, and runs code without leaving the window. That feedback is worth more than any tutorial.

**VS Code** is the recommended choice for this course — install the **Python** and **Jupyter** extensions.

### Editors are not magic

Autocomplete and hints come from information you can read yourself: docstrings, type hints, and signatures. The `inspect` module reads exactly what your editor reads.

Write this:

```python
def calculate_total(price: float, quantity: int, tax_rate: float = 0.18) -> float:
    """Work out the total cost including tax."""
```

…and your editor can now warn you that `calculate_total("100", "3")` passes strings where numbers belong — **before you run anything**.

### Settings to change on day one

<table width="100%">
<tr><th align="left" width="36%">Setting</th><th align="left" width="64%">Why it matters</th></tr>
<tr><td>Insert spaces, not tabs</td><td>Mixing them is a genuine syntax error in Python</td></tr>
<tr><td>Tab size = 4</td><td>PEP 8 requires four spaces per level</td></tr>
<tr><td>Show whitespace</td><td>Makes invisible indentation problems visible</td></tr>
<tr><td>Trim trailing whitespace</td><td>Keeps version control diffs clean</td></tr>
<tr><td>Format on save</td><td>Ends every argument about style, permanently</td></tr>
</table>

Tabs versus spaces is not a style preference here. Python reads indentation as structure, so mixing them stops your program running.

### What a linter catches

Unused variables and imports, typos in names, shadowed built-ins, mutable default arguments, unreachable code. Every one is a real bug that costs time to find by hand.

**Shadowing** deserves special mention, because the error message is baffling the first time:

```python
list = [1, 2, 3]     # now `list` is your data, not the built-in
list("abc")          # TypeError: 'list' object is not callable
```

Never name a variable after a built-in: `list`, `str`, `sum`, `type`, `id`, `dict`, `input`.

---

## 02.4 Writing and Running a Script

A script runs top to bottom, one statement at a time.

### Output and variables

```python
# print() sends text to the terminal.
print("Hello, world!")

# A variable gives a name to a value so you can reuse it.
name = "Ajay"
age = 31
```

### f-strings

Passing many arguments to `print()` gets clumsy. An f-string embeds values directly — note the `f` before the quote:

```python
print(f"{name} is {age} years old.")
print(f"Next year {name} will be {age + 1}.")   # any expression works
print(f"Price: {1234.5678:,.2f}")               # -> Price: 1,234.57
```

### Arithmetic

<table width="100%">
<tr><th align="left" width="14%">Operator</th><th align="left" width="30%">Does</th><th align="left" width="28%">Example</th><th align="left" width="28%">Result</th></tr>
<tr><td><code>+ - *</code></td><td>Add, subtract, multiply</td><td><code>17 * 5</code></td><td><code>85</code></td></tr>
<tr><td><code>/</code></td><td>True division — always a float</td><td><code>17 / 5</code></td><td><code>3.4</code></td></tr>
<tr><td><code>//</code></td><td>Floor division — rounds down</td><td><code>17 // 5</code></td><td><code>3</code></td></tr>
<tr><td><code>%</code></td><td>Remainder</td><td><code>17 % 5</code></td><td><code>2</code></td></tr>
<tr><td><code>**</code></td><td>Power</td><td><code>17 ** 2</code></td><td><code>289</code></td></tr>
</table>

`/` gives a float even when it divides evenly: `10 / 5` is `2.0`, not `2`.

### Input always returns text

This is the trap that catches everyone once:

```python
age = input("Your age: ")    # user types 30
age + 1                      # TypeError - it is the string "30"
```

Convert it first:

```python
age = int(input("Your age: "))
```

### Comments

A **good** comment explains *why*. A **poor** comment restates *what* the code already says.

```python
# Apply the standard rate, confirmed by finance on 2026-01-15.
standard_rate = 0.18

# Set standard_rate to 0.18        <- adds nothing, and will rot
standard_rate = 0.18
```

This course comments every meaningful line because it is teaching material. Production code needs fewer.

---

## 02.5 Virtual Environments

A virtual environment is a private copy of Python for one project, with its own packages.

### The problem it solves

Without them, every project shares one set of packages:

- `website-2024` needs Django 3.2
- `website-2026` needs Django 5.0

Installing one breaks the other. This is **dependency hell**, and `venv` avoids it entirely — each project gets its own `.venv` folder, and neither knows about the other.

### The workflow

```bash
# 1. Create - makes a .venv folder holding a private Python
python3 -m venv .venv

# 2. Activate - points your shell at that private Python
source .venv/bin/activate          # macOS and Linux
.venv\Scripts\activate             # Windows

# 3. Install - affects this project only
pip install jupyterlab

# 4. Record - write down exactly what is installed
pip freeze > requirements.txt

# 5. Leave
deactivate
```

### Confirming it worked

Your prompt gains a prefix:

```
before:  ajay@laptop ~/project $
after:   (.venv) ajay@laptop ~/project $
```

And in code, `sys.prefix` differs from `sys.base_prefix`:

```python
inside_venv = sys.prefix != sys.base_prefix
```

### Rules

<table width="100%">
<tr><th align="left" width="36%">Rule</th><th align="left" width="64%">Why</th></tr>
<tr><td>One environment per project</td><td>Never share one between projects</td></tr>
<tr><td>Name it <code>.venv</code></td><td>Tools and editors look for this name</td></tr>
<tr><td>Never commit <code>.venv</code></td><td>Large, machine-specific, and rebuildable</td></tr>
<tr><td>Always commit <code>requirements.txt</code></td><td>This is what others actually need</td></tr>
<tr><td>Activate before installing</td><td>Otherwise pip installs system-wide</td></tr>
<tr><td>Delete freely</td><td><code>rm -rf .venv</code> then rebuild — nothing is lost</td></tr>
</table>

That last rule surprises people: an environment is **disposable**. Everything needed to rebuild it lives in `requirements.txt`.

---

## 02.6 pip Basics

`pip` installs packages other people wrote. This is the main reason Python is so productive.

### Check the standard library first

Python ships with a large standard library — `json`, `csv`, `datetime`, `pathlib`, `re`, `sqlite3` all need no installation. Chapter 21 tours what is included. Reach for `pip` only when the standard library does not already solve your problem.

### The commands

<table width="100%">
<tr><th align="left" width="46%">Command</th><th align="left" width="54%">Does</th></tr>
<tr><td><code>pip install requests</code></td><td>Install the latest version</td></tr>
<tr><td><code>pip install requests==2.31.0</code></td><td>Install one exact version</td></tr>
<tr><td><code>pip install -r requirements.txt</code></td><td>Install everything listed in a file</td></tr>
<tr><td><code>pip install --upgrade requests</code></td><td>Upgrade to the latest</td></tr>
<tr><td><code>pip uninstall requests</code></td><td>Remove it</td></tr>
<tr><td><code>pip list</code></td><td>Show everything installed</td></tr>
<tr><td><code>pip show requests</code></td><td>Details, including dependencies</td></tr>
<tr><td><code>pip freeze &gt; requirements.txt</code></td><td>Record exact versions to a file</td></tr>
</table>

### Use `python3 -m pip`

With several Pythons installed, a bare `pip` can install into the wrong one. You then get `ModuleNotFoundError` for a package you just watched install successfully.

```bash
python3 -m pip install requests
```

Running pip *through* the interpreter guarantees it installs where your code will look.

### Version specifiers

<table width="100%">
<tr><th align="left" width="30%">Specifier</th><th align="left" width="70%">Meaning</th></tr>
<tr><td><code>requests</code></td><td>Any version — whatever is newest today</td></tr>
<tr><td><code>requests==2.31.0</code></td><td>Exactly this version, nothing else</td></tr>
<tr><td><code>requests&gt;=2.28</code></td><td>This version or newer</td></tr>
<tr><td><code>requests&gt;=2.28,&lt;3.0</code></td><td>A range — the usual choice for libraries</td></tr>
</table>

Applications usually pin exactly for reproducible installs. Libraries usually allow a range, so they can coexist with other packages.

### Safety

- **Check the name carefully** — typo-squatting packages have shipped real malware
- **Activate your venv first** — otherwise you install system-wide
- **Never `sudo pip install`** — it can break your operating system's Python
- **Review new dependencies** — each one is code you are choosing to trust

---

## 02.7 Anatomy of a Python File

Every real Python file follows a conventional layout.

```python
#!/usr/bin/env python3          # 1. shebang (Unix only, optional)
"""What this module is for."""  # 2. module docstring

import sys                      # 3. imports: standard library
from pathlib import Path

import requests                 #    then third-party

from myproject import helpers   #    then your own

DEFAULT_TAX_RATE = 0.18         # 4. constants, UPPER_CASE

def calculate_total(...):       # 5. functions and classes
    """What this does."""

if __name__ == "__main__":      # 6. main guard, last
    ...
```

### The main guard

Python sets `__name__` to `"__main__"` when a file is **run**, and to the module's name when it is **imported**.

```python
if __name__ == "__main__":
    # Runs only on direct execution, never on import.
```

This is what lets one file be both a runnable script and an importable library. Without it, importing the file would execute everything inside.

### File naming

<table width="100%">
<tr><th align="left" width="26%">Filename</th><th align="left" width="18%">Verdict</th><th align="left" width="56%">Why</th></tr>
<tr><td><code>my_script.py</code></td><td>good</td><td>Lowercase with underscores</td></tr>
<tr><td><code>MyScript.py</code></td><td>avoid</td><td>Capitals are for class names</td></tr>
<tr><td><code>my-script.py</code></td><td>broken</td><td>Cannot be imported — the hyphen reads as minus</td></tr>
<tr><td><code>2024_report.py</code></td><td>broken</td><td>Cannot start with a digit</td></tr>
<tr><td><code>json.py</code></td><td>dangerous</td><td>Shadows the standard library module</td></tr>
</table>

The last one causes genuinely baffling bugs: your own file gets imported instead of the real library.

---

## Chapter Files

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="27%">Notebook</th><th align="left" width="31%">Covers</th><th align="left" width="35%">The one idea to take away</th></tr>
<tr><td><b>02.1</b></td><td><code>02.1 installing_python.ipynb</code></td><td>Install, verify, platform detection</td><td><code>sys.executable</code> settles every "which Python?" question</td></tr>
<tr><td><b>02.2</b></td><td><code>02.2 interpreter_and_repl.ipynb</code></td><td>REPL, <code>help</code>, <code>dir</code>, <code>type</code></td><td>Expressions display; statements do not</td></tr>
<tr><td><b>02.3</b></td><td><code>02.3 editors_and_ides.ipynb</code></td><td>Editors, linters, settings</td><td>Editors read docstrings and hints — nothing magic</td></tr>
<tr><td><b>02.4</b></td><td><code>02.4 first_script.ipynb</code></td><td>Variables, f-strings, input, loops</td><td><code>input()</code> always returns text</td></tr>
<tr><td><b>02.5</b></td><td><code>02.5 virtual_environments.ipynb</code></td><td>venv, activation, requirements</td><td>Environments are disposable; the file is not</td></tr>
<tr><td><b>02.6</b></td><td><code>02.6 pip_basics.ipynb</code></td><td>Installing, pinning, safety</td><td>Use <code>python3 -m pip</code> to hit the right interpreter</td></tr>
<tr><td><b>02.7</b></td><td><code>02.7 anatomy_of_a_file.ipynb</code></td><td>File layout, main guard, naming</td><td>The main guard makes a file script <i>and</i> library</td></tr>
<tr><td><b>—</b></td><td><code>exercises.ipynb</code></td><td>Practice problems with solutions</td><td>Predict the output before you run it</td></tr>
</table>

---

## Key Terms

<table width="100%">
<tr><th align="left" width="18%">Term</th><th align="left" width="46%">Meaning</th><th align="left" width="36%">Where it comes up</th></tr>
<tr><td><b>REPL</b></td><td>Interactive Read-Evaluate-Print Loop session</td><td>02.2 — your fastest feedback loop</td></tr>
<tr><td><b>Expression</b></td><td>Code that produces a value</td><td>02.2 — the REPL displays these</td></tr>
<tr><td><b>Statement</b></td><td>Code that performs an action</td><td>02.2 — these display nothing</td></tr>
<tr><td><b>Script</b></td><td>A file of Python run top to bottom</td><td>02.4 — what you write most often</td></tr>
<tr><td><b>f-string</b></td><td>Text with values embedded via <code>{}</code></td><td>02.4 — full detail in Chapter 07</td></tr>
<tr><td><b>Virtual environment</b></td><td>A private Python and packages for one project</td><td>02.5 — one per project, always</td></tr>
<tr><td><b><code>requirements.txt</code></b></td><td>The recorded list of exact package versions</td><td>02.5 — commit this, not <code>.venv</code></td></tr>
<tr><td><b>PyPI</b></td><td>The Python Package Index, where pip downloads from</td><td>02.6 — publishing covered in Chapter 40</td></tr>
<tr><td><b>Shebang</b></td><td><code>#!/usr/bin/env python3</code> — makes a file directly runnable</td><td>02.7 — Unix only, must be line 1</td></tr>
<tr><td><b>Main guard</b></td><td><code>if __name__ == "__main__":</code></td><td>02.7 — script and library in one file</td></tr>
<tr><td><b>Shadowing</b></td><td>Reusing a built-in's name for your own variable</td><td>02.3 — produces confusing errors</td></tr>
</table>

---

## Common Errors in This Chapter

<table width="100%">
<tr><th align="left" width="30%">Error</th><th align="left" width="34%">Usual cause</th><th align="left" width="36%">Fix</th></tr>
<tr><td><code>command not found: python</code></td><td>Not on PATH, or wrong command name</td><td>Try <code>python3</code>; on Windows reinstall with "Add to PATH" ticked</td></tr>
<tr><td><code>TypeError: can only concatenate str</code></td><td>Doing arithmetic on <code>input()</code> output</td><td>Wrap it: <code>int(input(...))</code></td></tr>
<tr><td><code>IndentationError</code></td><td>Inconsistent indentation, or tabs mixed with spaces</td><td>Use four spaces; turn on "show whitespace"</td></tr>
<tr><td><code>ModuleNotFoundError</code></td><td>Installed into a different Python</td><td>Use <code>python3 -m pip install</code></td></tr>
<tr><td><code>'list' object is not callable</code></td><td>Shadowed a built-in name</td><td>Rename your variable</td></tr>
</table>

---

## Next

**Chapter 03 — Syntax Fundamentals.** Statements and expressions, indentation rules, comments and docstrings, keywords and identifiers, PEP 8, and how to read the errors you will inevitably hit.
