# Chapter 03 — Syntax Fundamentals

This is where the actual language starts. Chapters 01 and 02 were theory and setup; from here the theory lives **inside the notebooks**, next to the code that proves it.

Syntax is the part people assume they can skip. They cannot — nearly every confusing error in Chapters 04 to 10 traces back to something in this chapter.

**By the end you will be able to:**

- Tell an expression from a statement, and explain why it matters
- Explain how indentation becomes `INDENT`/`DEDENT` tokens
- Choose correctly between a comment and a docstring
- Wrap long lines the way every Python project does
- Name the keywords, and avoid the far more dangerous built-ins
- Read PEP 8 code fluently and let tooling apply it
- Read any traceback and find the real cause quickly

---

## How this chapter is structured

Each notebook opens with a **Theory** section explaining the mechanism, then proves every claim with runnable code. Where the behaviour is surprising, the notebook shows the **bytecode** rather than asking you to take it on trust.

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="27%">Notebook</th><th align="left" width="32%">Core idea</th><th align="left" width="34%">Proved by</th></tr>
<tr><td><b>03.1</b></td><td><code>statements_and_expressions</code></td><td>Values vs actions</td><td><code>eval</code> vs <code>exec</code>; <code>POP_TOP</code> vs <code>STORE_NAME</code></td></tr>
<tr><td><b>03.2</b></td><td><code>indentation_and_blocks</code></td><td>Whitespace is syntax</td><td>Live <code>tokenize</code> output showing real INDENT tokens</td></tr>
<tr><td><b>03.3</b></td><td><code>comments_and_docstrings</code></td><td>Discarded vs stored</td><td><code>co_consts</code> — the comment is absent, the docstring is not</td></tr>
<tr><td><b>03.4</b></td><td><code>line_continuation</code></td><td>Brackets over backslashes</td><td>One invisible space breaking a backslash</td></tr>
<tr><td><b>03.5</b></td><td><code>keywords_and_identifiers</code></td><td>Three levels of "taken"</td><td>Shadowed <code>list</code> and <code>sum</code> failing live</td></tr>
<tr><td><b>03.6</b></td><td><code>pep8_introduction</code></td><td>A shared dialect</td><td>Before/after rewrite with every change listed</td></tr>
<tr><td><b>03.7</b></td><td><code>common_syntax_errors</code></td><td>Errors are precise feedback</td><td>Every error triggered for real, not described</td></tr>
<tr><td><b>—</b></td><td><code>exercises</code></td><td>Practice</td><td>Predict, debug, restyle, then write</td></tr>
</table>

---

## Quick reference

### Expression vs statement

The test: **can it go on the right-hand side of an `=`?**

<table width="100%">
<tr><th align="left" width="22%">Category</th><th align="left" width="34%">Examples</th><th align="left" width="44%">Behaviour</th></tr>
<tr><td><b>Expression</b></td><td><code>2 + 3</code>, <code>len(x)</code>, <code>a > b</code></td><td>Produces a value; works with <code>eval()</code></td></tr>
<tr><td><b>Statement</b></td><td><code>x = 5</code>, <code>import os</code>, <code>return</code></td><td>Performs an action; works with <code>exec()</code></td></tr>
</table>

An expression alone on a line is an **expression statement** — its value is computed and discarded. This is why `text.strip()` on its own line does nothing.

### Blocks

A statement ending in `:` opens a block. The tokenizer emits real `INDENT` and `DEDENT` tokens — Python's equivalent of `{` and `}`.

<table width="100%">
<tr><th align="left" width="34%">Error</th><th align="left" width="66%">Means</th></tr>
<tr><td><code>expected an indented block</code></td><td>A colon opened a block, but nothing was indented after it</td></tr>
<tr><td><code>unexpected indent</code></td><td>A line was indented with no block open</td></tr>
<tr><td><code>unindent does not match</code></td><td>The dedent landed between two existing levels</td></tr>
<tr><td><code>TabError</code></td><td>Tabs and spaces mixed ambiguously — Python refuses to guess</td></tr>
</table>

**Four spaces. Never tabs.** Configure your editor once.

### Comments vs docstrings

<table width="100%">
<tr><th align="left" width="20%"></th><th align="left" width="40%">Comment</th><th align="left" width="40%">Docstring</th></tr>
<tr><td><b>Syntax</b></td><td><code>#</code> to end of line</td><td>String as the <i>first statement</i></td></tr>
<tr><td><b>Survives?</b></td><td>No — stripped at compile time</td><td>Yes — stored in <code>__doc__</code></td></tr>
<tr><td><b>Readable at runtime?</b></td><td>Never</td><td>Yes — this is how <code>help()</code> works</td></tr>
<tr><td><b>Explains</b></td><td><i>Why</i> — for whoever edits it</td><td><i>What</i> — for whoever calls it</td></tr>
</table>

Python has **no block comment syntax**. A triple-quoted string is an expression statement, not a comment.

### Line continuation

```python
# Preferred - brackets, with a trailing comma
total = (
    first_value
    + second_value
)

# Avoid - one invisible trailing space breaks it
total = first_value + \
        second_value
```

Break **before** binary operators. Adjacent string literals join at compile time — so a missing comma in a list silently merges two items.

### Names

<table width="100%">
<tr><th align="left" width="20%">Category</th><th align="left" width="26%">Example</th><th align="left" width="54%">If you reuse the name</th></tr>
<tr><td><b>Keyword</b></td><td><code>if</code>, <code>class</code>, <code>return</code></td><td>Immediate <code>SyntaxError</code> — safe, because it is obvious</td></tr>
<tr><td><b>Soft keyword</b></td><td><code>match</code>, <code>case</code>, <code>type</code></td><td>Fine outside its statement position</td></tr>
<tr><td><b>Built-in</b></td><td><code>list</code>, <code>sum</code>, <code>id</code></td><td><b>Allowed</b> — then fails later, confusingly</td></tr>
</table>

Naming conventions:

<table width="100%">
<tr><th align="left" width="26%">What</th><th align="left" width="30%">Convention</th><th align="left" width="44%">Example</th></tr>
<tr><td>Variables, functions</td><td><code>snake_case</code></td><td><code>user_name</code>, <code>calculate_total()</code></td></tr>
<tr><td>Constants</td><td><code>UPPER_SNAKE_CASE</code></td><td><code>MAX_RETRIES</code></td></tr>
<tr><td>Classes, exceptions</td><td><code>PascalCase</code></td><td><code>BankAccount</code>, <code>ValidationError</code></td></tr>
<tr><td>Internal</td><td><code>_leading_underscore</code></td><td><code>_cache</code></td></tr>
<tr><td>Name-mangled</td><td><code>__double_leading</code></td><td>Becomes <code>_ClassName__x</code></td></tr>
<tr><td>Throwaway</td><td><code>_</code></td><td><code>for _ in range(3)</code></td></tr>
</table>

Booleans read best with `is_`, `has_`, `can_`, `should_`.

### PEP 8 essentials

- 4-space indent, 79 chars (88 with `black`)
- Two blank lines between top-level definitions, one between methods
- Spaces around `=` for **assignment**; none for **defaults and keyword arguments** — unless annotated (`role: str = "x"`)
- Imports: one per line, at the top, grouped stdlib / third-party / local
- **PEP 8 says consistency within a file beats consistency with PEP 8**

Do not apply it by hand — `ruff check --fix .` and `ruff format .`.

### Reading errors

**Read tracebacks from the bottom up.** Last line = type and message. Line above = the code that failed. Everything higher = how you got there.

<table width="100%">
<tr><th align="left" width="32%">Error</th><th align="left" width="68%">First thing to check</th></tr>
<tr><td><code>SyntaxError: invalid syntax</code></td><td>The line <b>above</b> — usually an unclosed bracket</td></tr>
<tr><td><code>NameError</code></td><td>Typo, or a cell you did not run</td></tr>
<tr><td><code>TypeError</code></td><td><code>print(type(x))</code> — what do you actually have?</td></tr>
<tr><td><code>ValueError</code></td><td>Right type, impossible content — check the input</td></tr>
<tr><td><code>AttributeError</code></td><td><code>dir(x)</code> — what does this object really offer?</td></tr>
<tr><td><code>KeyError</code></td><td>Use <code>.get()</code>, or test with <code>in</code> first</td></tr>
<tr><td><code>IndexError</code></td><td>Off by one — indexing starts at 0</td></tr>
<tr><td><code>ModuleNotFoundError</code></td><td>Not installed, or the wrong virtual environment</td></tr>
</table>

`print(repr(x))` reveals what `print(x)` hides — quotes, trailing spaces, and whether a number is really a string.

### Mistakes that raise no error at all

These are the dangerous ones:

- A missing comma between string literals silently concatenates them
- A mutable default argument (`def f(x=[])`) is created **once**, at definition
- `//` instead of `/` when you wanted a float
- `0.1 + 0.2 == 0.3` is `False`

---

## Key Terms

<table width="100%">
<tr><th align="left" width="20%">Term</th><th align="left" width="44%">Meaning</th><th align="left" width="36%">Where</th></tr>
<tr><td><b>Expression</b></td><td>Code that evaluates to a value</td><td>03.1</td></tr>
<tr><td><b>Statement</b></td><td>Code that performs an action</td><td>03.1</td></tr>
<tr><td><b>Expression statement</b></td><td>An expression alone on a line; value discarded</td><td>03.1 — ends in <code>POP_TOP</code></td></tr>
<tr><td><b>Walrus operator</b></td><td><code>:=</code> — assignment as an expression</td><td>03.1, full detail in Ch06</td></tr>
<tr><td><b>Block</b></td><td>Statements grouped by indentation</td><td>03.2</td></tr>
<tr><td><b>INDENT / DEDENT</b></td><td>Real tokens generated from whitespace</td><td>03.2</td></tr>
<tr><td><b>Guard clause</b></td><td>Handling the exception early to stay flat</td><td>03.2</td></tr>
<tr><td><b>Docstring</b></td><td>String as the first statement; stored in <code>__doc__</code></td><td>03.3</td></tr>
<tr><td><b>Implicit continuation</b></td><td>Newlines ignored inside brackets</td><td>03.4</td></tr>
<tr><td><b>Keyword</b></td><td>Reserved word — 35 of them</td><td>03.5</td></tr>
<tr><td><b>Soft keyword</b></td><td>Reserved only in context</td><td>03.5</td></tr>
<tr><td><b>Shadowing</b></td><td>Hiding a built-in with your own name</td><td>03.5</td></tr>
<tr><td><b>Name mangling</b></td><td><code>__x</code> becomes <code>_Class__x</code></td><td>03.5, full detail in Ch25</td></tr>
<tr><td><b>PEP</b></td><td>Python Enhancement Proposal</td><td>03.6</td></tr>
<tr><td><b>Traceback</b></td><td>The call stack printed on an error</td><td>03.7 — read bottom-up</td></tr>
</table>

---

## Next

**Chapter 04 — Variables and Memory Model.** What a variable actually is, why `a = b` does not copy anything, and why two lists can change together when you only touched one. This is the chapter that explains the bugs that look like magic.
