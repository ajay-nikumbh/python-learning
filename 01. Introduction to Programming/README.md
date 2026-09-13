# Chapter 01 — Introduction to Programming

This chapter contains almost no Python. That is deliberate.

Before you learn a language, you need to know what a language *is for* — what a computer actually does, what an algorithm is, and why Python looks the way it does. People who skip this chapter can usually write code but cannot debug it, because they have no mental model of what the machine is doing underneath.

**By the end of this chapter you will be able to:**

- Explain what programming is, without using the word "coding"
- Describe how a CPU executes instructions, and where your variables actually live
- Write an algorithm in pseudocode before writing it in a language
- Explain the difference between compiled and interpreted languages, and where Python sits
- Name the major programming paradigms and recognise them in code
- Explain what Python is, where it came from, and what its design philosophy values
- List the domains Python is used in, and where it is a poor fit
- Explain what CPython is, and how it differs from PyPy and other implementations

---

## 01.1 What is Programming

A **program** is a precise sequence of instructions that tells a computer how to transform input into output.

The key word is *precise*. A computer has no common sense, no context, and no ability to guess what you meant. If you tell a person "sort these names," they will figure it out. A computer needs to be told what "sort" means, what order counts as sorted, what to do with duplicates, and what to do if the list is empty.

Programming is therefore two separate skills:

1. **Thinking** — breaking a vague human goal into unambiguous steps.
2. **Writing** — expressing those steps in a language the computer can execute.

Beginners assume the hard part is step 2, the syntax. It is not. Syntax you can look up in thirty seconds. Step 1 — decomposing a problem correctly — is the actual job, and it is language-independent. Someone who thinks clearly in Python will think clearly in Java.

### Source code, and why it is for humans

The instructions you write are called **source code**. Source code is a text file. It is not magic and it is not special — you could write Python in Notepad.

Here is the thing that surprises people: source code exists mainly for *humans*. The computer is perfectly happy with unreadable binary. We invented programming languages so that people could read, review, and change instructions without going insane. This is why "clean code" is not a stylistic preference — code is read far more often than it is written, and by more people than wrote it.

### Program vs process

- A **program** is the instructions sitting on disk. Static. Dead.
- A **process** is a program that is currently running, loaded into memory, with live state.

A recipe in a book is a program. You actually cooking in the kitchen is a process. The same recipe can be cooked by three people at once — the same program can run as three independent processes.

### Why it feels hard at first

Three specific reasons, so you can name them when you hit them:

- **No feedback on intent.** The computer does what you *said*, not what you *meant*. Every bug is this.
- **Invisible state.** Values change over time inside memory and you cannot see them without deliberately looking.
- **Total precision required.** One wrong character breaks everything. No other craft is this unforgiving about typos.

None of that means you are bad at it. It means the medium is strict.

---

## 01.2 How Computers Execute Code

You do not need an electrical engineering degree, but you do need an accurate model. Vague models produce vague debugging.

### Everything is numbers

At the hardware level a computer stores only two states, written as `0` and `1`. One such digit is a **bit**. Eight bits make a **byte**.

Every single thing a computer handles is ultimately a number:

<table width="100%">
<tr>
<th align="left" width="28%">Thing</th>
<th align="left" width="32%">Stored as</th>
<th align="left" width="40%">What decides the meaning</th>
</tr>
<tr><td align="left">The number 65</td><td align="left"><code>01000001</code></td><td align="left">Read as a plain integer</td></tr>
<tr><td align="left">The letter <code>A</code></td><td align="left"><code>01000001</code></td><td align="left">The *same* bits, read as text</td></tr>
<tr><td align="left">A pixel's colour</td><td align="left">Three numbers: red, green, blue</td><td align="left">Position in an image buffer</td></tr>
<tr><td align="left">An instruction</td><td align="left">A number the CPU recognises</td><td align="left">Where the program counter points</td></tr>
</table>

Notice rows 1 and 2. The same bits mean different things depending on how they are *interpreted*. There is no label in the hardware saying "this is text." The type system in a language exists to keep that interpretation straight — which is exactly why Python cares so much about types.

### The three parts that matter

**CPU (processor)** — does the actual work. It can do arithmetic, compare values, move data, and jump to a different instruction. That is essentially the whole list. Everything else is built from those primitives.

**RAM (memory)** — a huge array of numbered slots. Each slot has an **address** (its number) and holds a value. Fast, but erased when power is lost. Your variables live here while your program runs.

**Storage (disk/SSD)** — slower, but survives power loss. Your notebooks and source files live here until you run them.

The speed gap is the part beginners underestimate. If a CPU operation took one second, reading RAM would take roughly a minute, and reading a spinning disk would take several years. This is why "just read it from the file each time" is a performance disaster and why we load things into memory.

### The fetch–decode–execute cycle

The CPU runs one loop, billions of times per second:

1. **Fetch** — read the next instruction from memory.
2. **Decode** — work out what operation that instruction means.
3. **Execute** — do it.
4. Repeat.

The CPU tracks its position with a **program counter** — a register holding the address of the next instruction. Normally it just increments. When your code branches (`if`) or loops (`for`), what physically happens is that the program counter gets *set to a different address*. That is all control flow is: changing which instruction comes next.

### Machine code and assembly

The CPU only understands **machine code** — raw binary. Humans cannot work in it, so the thinnest human-readable layer is **assembly language**, where each line maps to roughly one machine instruction:

```asm
MOV AX, 5      ; put the value 5 into register AX
ADD AX, 3      ; add 3 to whatever is in AX
```

Two lines to add two numbers. A real program would be tens of thousands of lines, and it would only run on one processor family. That pain is the entire reason high-level languages exist.

In Python, `total = 5 + 3` is one line, reads like arithmetic, and runs anywhere Python runs. You give up some control over the hardware and get back enormous leverage.

### Where your variables actually live

When you write `age = 25`, roughly this happens:

1. Python creates an integer object holding 25, somewhere in RAM.
2. Python records that the name `age` refers to that object.
3. `age` is a label pointing at a memory location — not a box containing a value.

That distinction seems pedantic now. In Chapter 04 it becomes the single most important concept for understanding why two variables can appear to change together, and why mutable defaults bite people.

---

## 01.3 Algorithms and Pseudocode

An **algorithm** is a finite sequence of unambiguous steps that solves a problem.

It must be:

- **Finite** — it has to stop eventually
- **Unambiguous** — each step has exactly one interpretation
- **Effective** — each step is actually doable
- **Defined for its inputs** — you know what it accepts and what it produces

Algorithms are older than computers. Long division is an algorithm. A recipe is close to one.

### Pseudocode

**Pseudocode** is algorithm-writing in structured English. No syntax rules, no semicolons, nothing to memorise — and crucially, nothing to get *wrong*. You think about the logic without fighting the language.

Finding the largest number in a list:

```
START
  SET largest TO the first number in the list
  FOR each remaining number in the list
    IF the number is greater than largest THEN
      SET largest TO that number
  RETURN largest
END
```

Read it and it obviously works. Now translate it to Python and the structure survives intact:

```python
# Start by assuming the first number is the largest one we have seen.
largest = numbers[0]

# Walk through every number in the list, one at a time.
for number in numbers:
    # If this number beats our current record holder, it becomes the new one.
    if number > largest:
        largest = number
```

This is the habit worth building: **pseudocode first, then translate.** It separates "what should happen" from "how do I spell it," and it turns one hard problem into two easy ones.

### Decomposition

Real problems are too big to solve in one move. You break them down until each piece is obviously solvable.

"Build a to-do app" is not a problem you can start typing. Decomposed:

```
Build a to-do app
├── Store tasks
│   ├── Add a task
│   ├── Mark a task done
│   └── Delete a task
├── Save tasks between runs
│   ├── Write tasks to a file
│   └── Read tasks from a file
└── Show tasks to the user
    ├── Print all tasks
    └── Print only unfinished tasks
```

Every leaf is now a small function you could write today. This is how all software gets built — there is no other way.

### Three building blocks

Every algorithm ever written is made of three structures. This is a proven result (the structured program theorem), not a rule of thumb.

**Sequence** — do this, then this:
```
GET the price
CALCULATE the tax
PRINT the total
```

**Selection** — choose a path (Chapter 09):
```
IF the user is a member THEN
  apply a discount
ELSE
  charge full price
```

**Iteration** — repeat (Chapter 10):
```
FOR each item in the cart
  add its price to the total
```

That is the complete set. Everything else — functions, classes, async — is organisation and convenience layered on top of these three.

---

## 01.4 Compiled vs Interpreted Languages

Your source code is text. The CPU needs machine code. Something has to bridge that gap, and languages choose different bridges.

### Compiled languages

A **compiler** translates your entire source file into machine code *ahead of time*, producing an executable file. C, C++, Rust and Go work this way.

```
source.c  →  [compiler]  →  program.exe  →  [CPU runs it]
```

- **Fast at runtime** — translation already happened; the CPU runs native instructions
- **Errors caught early** — the compiler refuses to build broken code
- **Platform-specific** — a Windows build will not run on macOS
- **Slower to iterate** — every change means recompiling

### Interpreted languages

An **interpreter** reads your source and executes it *as it goes*, translating on the fly. Python, JavaScript and Ruby work this way.

```
source.py  →  [interpreter reads and executes, line by line]
```

- **Fast to iterate** — change a line, run it immediately
- **Portable** — same file runs anywhere the interpreter exists
- **Slower at runtime** — translation happens every time you run
- **Some errors surface late** — a typo on line 400 is only found when line 400 runs

That last point matters more than beginners expect. Python will happily run 399 correct lines before hitting your typo. This is why we test (Chapter 36) and why type hints (Chapter 32) exist.

### Where Python actually sits

Calling Python "interpreted" is the useful shorthand, but the truth is a hybrid, and knowing it explains several things you will otherwise find mysterious.

```
source.py
   ↓  compile step (automatic, invisible)
bytecode (.pyc)
   ↓  Python Virtual Machine
CPU executes
```

1. Python **compiles** your source to **bytecode** — a compact instruction set for Python itself, not for your CPU.
2. The **Python Virtual Machine (PVM)** interprets that bytecode.

So Python compiles *and* interprets. Two consequences you will meet in practice:

- The `__pycache__` folder that appears next to your files holds cached `.pyc` bytecode, so unchanged modules skip recompilation on the next run. You can safely delete it; Python regenerates it.
- Syntax errors are caught *before* anything runs, because compilation happens first. Everything else — name errors, type errors — waits until execution.

You will inspect real bytecode with the `dis` module in Chapter 43.

### Why Python is slower, in one sentence

Every operation goes through the interpreter, which must check types at runtime, so `a + b` in Python does considerably more work than the single CPU instruction it compiles to in C.

That gap is real, and it is usually irrelevant. Developer time costs more than CPU time, most programs wait on network or disk rather than CPU, and the genuinely hot numerical paths are handed off to C libraries like NumPy. Optimise when you have measured a problem (Chapter 37), not before.

---

## 01.5 Programming Paradigms

A **paradigm** is a style of organising code — a philosophy about how programs should be structured.

Python is **multi-paradigm**: it supports several and forces none. You will meet all of these properly later; the goal now is recognition.

### Imperative / procedural

Describe *how* to do something, step by step, and group steps into procedures (functions). This is the default style and where you will start.

```python
# Keep a running total, starting from nothing.
total = 0

# Add each number to the total, one at a time.
for number in [1, 2, 3, 4]:
    total = total + number
```

You are telling the computer the exact sequence of operations. **Chapters 09, 10, 16.**

### Object-oriented (OOP)

Bundle data and the functions that operate on it into **objects**. Model the problem as interacting things rather than as a list of steps.

```python
# A Dog bundles its own data (its name) with its own behaviour (barking).
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return f"{self.name} says woof"
```

Good for modelling domains with clear entities — users, orders, files. **Chapters 24–28.**

### Functional

Build programs from functions that transform data and avoid changing state. Emphasises immutability and functions as values.

```python
# Produce a NEW list of doubled values. The original list is untouched.
numbers = [1, 2, 3, 4]
doubled = [number * 2 for number in numbers]
```

Fewer moving parts means fewer bugs, since nothing changes behind your back. **Chapters 17, 31.**

### Declarative

Describe *what* you want, not how to get it. SQL is the classic example; in Python, comprehensions and libraries like pandas lean this way.

```python
# State the result you want. Python works out the looping.
adults = [person for person in people if person.age >= 18]
```

### Choosing

Do not pick a team. Real Python code mixes all of these, usually within one file:

- **Procedural** for scripts and straightforward logic
- **OOP** when you have entities with state and behaviour
- **Functional** for data transformation pipelines
- **Declarative** wherever it reads more clearly

The skill is matching the style to the problem — not applying one style everywhere out of loyalty.

---

## 01.6 What is Python

**Python** is a high-level, general-purpose, dynamically typed, interpreted programming language that emphasises code readability.

Unpacking that definition:

- **High-level** — you work with ideas (lists, files, objects), not memory addresses and registers
- **General-purpose** — not tied to one domain, unlike SQL or CSS
- **Dynamically typed** — variables do not declare a type; types belong to values and are checked at runtime
- **Interpreted** — executed via the interpreter rather than compiled to a native executable (see 01.4 for the nuance)
- **Readable** — enforced indentation and minimal punctuation, by design

### History

Guido van Rossum began Python in December 1989 as a hobby project over the Christmas holidays, at CWI in the Netherlands. He wanted a language between shell scripting and C: more capable than the former, less painful than the latter.

The name comes from **Monty Python's Flying Circus**, not the snake. This is why example code in the docs is full of spam, eggs and silly walks.

<table width="100%">
<tr>
<th align="left" width="14%">Version</th>
<th align="center" width="10%">Year</th>
<th align="left" width="76%">Why it mattered</th>
</tr>
<tr><td align="left">0.9.0</td><td align="center">1991</td><td align="left">First public release — already had classes, exceptions, functions</td></tr>
<tr><td align="left">1.0</td><td align="center">1994</td><td align="left"><code>lambda</code>, <code>map</code>, <code>filter</code>, <code>reduce</code></td></tr>
<tr><td align="left">2.0</td><td align="center">2000</td><td align="left">List comprehensions, garbage collection</td></tr>
<tr><td align="left">3.0</td><td align="center">2008</td><td align="left">Deliberately backwards-incompatible cleanup</td></tr>
<tr><td align="left">3.6</td><td align="center">2016</td><td align="left">f-strings</td></tr>
<tr><td align="left">3.9</td><td align="center">2020</td><td align="left">Dict merge <code>|</code>, built-in generic types</td></tr>
<tr><td align="left">3.10</td><td align="center">2021</td><td align="left"><code>match</code> statement, better error messages</td></tr>
<tr><td align="left">3.11</td><td align="center">2022</td><td align="left">Major speed improvements (10–60%)</td></tr>
<tr><td align="left">3.12</td><td align="center">2023</td><td align="left">Improved f-strings, better typing</td></tr>
<tr><td align="left">3.13</td><td align="center">2024</td><td align="left">Experimental free-threaded build (no GIL)</td></tr>
</table>

**Python 2 is dead.** It reached end-of-life on 1 January 2020. If a tutorial uses `print "hello"` without parentheses, it is Python 2 — close the tab.

The 2→3 transition is worth knowing about as a cautionary tale: the breaking changes were correct but the migration took over a decade. It is the reason Python is now extremely conservative about breaking compatibility.

### The Zen of Python

Run `import this` in a Python interpreter and you get Tim Peters' 19 aphorisms — the language's design philosophy, shipped inside the language as an easter egg.

The ones that actually change how you write code:

> **Beautiful is better than ugly.**
> **Explicit is better than implicit.** — say what you mean; hidden magic costs more than it saves
> **Simple is better than complex.**
> **Readability counts.** — the central value
> **Special cases aren't special enough to break the rules.**
> **Errors should never pass silently.** — never write a bare `except: pass` (Chapter 23)
> **There should be one — and preferably only one — obvious way to do it.**
> **If the implementation is hard to explain, it's a bad idea.**

That last one is a genuinely useful test. If you cannot explain your function in one sentence, rewrite it.

### What "Pythonic" means

Code that follows the language's idioms rather than transliterating another language's habits.

```python
# NOT Pythonic - manually managing an index counter, the way you would in C.
index = 0
while index < len(items):
    print(items[index])
    index = index + 1

# Pythonic - say what you mean: look at each item.
for item in items:
    print(item)
```

Both work. The second is shorter, has no off-by-one risk, and states the intent directly. You will develop this instinct over the course; you are not expected to have it now.

---

## 01.7 Where Python is Used

Python is not the fastest language, nor the safest, nor the most elegant. It is the most *broadly useful*, and its libraries are its real superpower.

### Where it dominates

**Data science, machine learning and AI** — the strongest position. NumPy, pandas, scikit-learn, PyTorch and TensorFlow make Python the default language of the field. The heavy maths runs in C/C++ under the hood; Python is the steering wheel.

**Automation and scripting** — the original use case. Renaming thousands of files, scraping a site, parsing logs, gluing tools together. If a task is boring and repetitive, Python is usually the shortest path.

**Web backends** — Django (batteries included), Flask (minimal), FastAPI (modern, async, typed). Instagram, Spotify and Dropbox run substantial Python.

**DevOps and infrastructure** — Ansible is Python; AWS, Google Cloud and Azure all ship Python SDKs. Deployment and infrastructure tooling leans on it heavily.

**Scientific and academic computing** — SciPy, Astropy, Biopython. Jupyter notebooks are the standard medium for computational research.

**Testing** — `pytest` and Selenium are widely used to test systems written in *other* languages.

### Where it is used but is not the leader

- **Desktop GUI apps** — possible (Tkinter, PyQt), but distribution is awkward
- **Game development** — Pygame is great for learning; commercial games use C++ or C#
- **Mobile apps** — Kivy and BeeWare exist; Swift and Kotlin dominate

### Where you should pick something else

Being honest about this is part of engineering judgement:

- **Systems programming** (operating systems, drivers) — C, C++, Rust
- **Real-time embedded** with hard timing guarantees — C, Rust (though MicroPython serves hobby boards well)
- **Browser frontend** — JavaScript/TypeScript is the only native option
- **CPU-bound work needing maximum throughput** — C++, Rust, Go (or call into them from Python)

### The honest summary

Python's niche is **problems where developer time matters more than machine time** — which is most problems. When machine time genuinely dominates, Python is still often the right choice as the orchestration layer around fast native libraries.

---

## 01.8 CPython vs PyPy and Other Implementations

Here is a distinction that clears up a surprising amount of confusion: **Python is a specification, not a program.**

The language is defined by a document. Anyone can write a program that implements that specification. Several people have, and they have made different trade-offs.

### CPython — the reference implementation

Written in C. This is what you get from python.org and what 95%+ of the world runs. When someone says "Python," they mean CPython.

- The reference implementation — if CPython does it, that is the behaviour, full stop
- Best library compatibility, since C extensions are built against it
- Has the **GIL** (Global Interpreter Lock), which limits true multi-threaded CPU parallelism (Chapter 33)
- Not the fastest option, though 3.11+ improved substantially

**Use it unless you have a specific, measured reason not to.**

### PyPy — the fast one

Python written in Python (RPython), with a **JIT compiler**: it watches which code runs hot and compiles those paths to machine code while running.

- Often 4–10× faster on long-running, CPU-bound pure-Python code
- Uses more memory, and starts up slower — short scripts can end up *slower* overall
- Weaker support for C extensions, though it has improved a lot

Worth trying when you have a long-running pure-Python workload and have already confirmed CPython is the bottleneck.

### The others, briefly

<table width="100%">
<tr>
<th align="left" width="24%">Implementation</th>
<th align="left" width="26%">Host platform</th>
<th align="left" width="50%">Typical use</th>
</tr>
<tr><td align="left"><b>Jython</b></td><td align="left">JVM</td><td align="left">Calling Java libraries from Python</td></tr>
<tr><td align="left"><b>IronPython</b></td><td align="left">.NET</td><td align="left">Calling .NET libraries from Python</td></tr>
<tr><td align="left"><b>MicroPython</b></td><td align="left">Microcontrollers</td><td align="left">Embedded boards, hardware projects</td></tr>
<tr><td align="left"><b>CircuitPython</b></td><td align="left">Microcontrollers</td><td align="left">Education-focused MicroPython fork</td></tr>
<tr><td align="left"><b>Cython</b></td><td align="left">Compiles to C</td><td align="left">Speeding up hot paths with C-level types</td></tr>
<tr><td align="left"><b>Graal Python</b></td><td align="left">GraalVM</td><td align="left">Polyglot JVM applications</td></tr>
</table>

### Terms you will see and should not confuse

- **Python** — the language specification
- **CPython** — the standard implementation, written in C
- **Cython** — a *different* thing: a superset of Python that compiles to C for speed
- **PVM** — the Python Virtual Machine, the part of CPython that executes bytecode

CPython and Cython being one letter apart is an unfortunate accident of naming. They are unrelated tools.

### What this means for you

Install CPython from python.org. Everything in this course targets it. Revisit the alternatives only when you have measured a real performance problem — and read Chapter 37 on profiling first, because the bottleneck is rarely where people guess.

---

## Chapter Files

<table width="100%">
<tr>
<th align="left" width="7%">#</th>
<th align="left" width="28%">Notebook</th>
<th align="left" width="30%">Covers</th>
<th align="left" width="35%">The one idea to take away</th>
</tr>
<tr><td align="left"><b>01.1</b></td><td align="left"><code>01.1 what_is_programming.ipynb</code></td><td align="left">Programs, instructions, precision</td><td align="left">The computer does what you say, not what you mean</td></tr>
<tr><td align="left"><b>01.2</b></td><td align="left"><code>01.2 how_computers_execute.ipynb</code></td><td align="left">Bits, bytes, memory, the CPU cycle</td><td align="left">A variable is a label pointing at memory, not a box</td></tr>
<tr><td align="left"><b>01.3</b></td><td align="left"><code>01.3 algorithms_and_pseudocode.ipynb</code></td><td align="left">Algorithms, decomposition, the three building blocks</td><td align="left">Write the steps in English before writing any code</td></tr>
<tr><td align="left"><b>01.4</b></td><td align="left"><code>01.4 compiled_vs_interpreted.ipynb</code></td><td align="left">Bytecode, <code>__pycache__</code>, the compile step</td><td align="left">Python compiles *and* interprets — it is a hybrid</td></tr>
<tr><td align="left"><b>01.5</b></td><td align="left"><code>01.5 programming_paradigms.ipynb</code></td><td align="left">The same task in four paradigms</td><td align="left">Match the style to the problem, not to a loyalty</td></tr>
<tr><td align="left"><b>01.6</b></td><td align="left"><code>01.6 what_is_python.ipynb</code></td><td align="left">Zen of Python, version info, Pythonic style</td><td align="left">Readability is the language's central value</td></tr>
<tr><td align="left"><b>01.7</b></td><td align="left"><code>01.7 where_python_is_used.ipynb</code></td><td align="left">Domains and honest limitations</td><td align="left">Python wins where developer time beats machine time</td></tr>
<tr><td align="left"><b>01.8</b></td><td align="left"><code>01.8 python_implementations.ipynb</code></td><td align="left">Detecting your implementation at runtime</td><td align="left">Use CPython unless you have measured a reason not to</td></tr>
<tr><td align="left"><b>—</b></td><td align="left"><code>exercises.ipynb</code></td><td align="left">Practice problems with solutions</td><td align="left">Answer before you run — that is where learning happens</td></tr>
</table>

---

## Key Terms

<table width="100%">
<tr>
<th align="left" width="16%">Term</th>
<th align="left" width="48%">Meaning</th>
<th align="left" width="36%">Where it comes up</th>
</tr>
<tr><td align="left"><b>Program</b></td><td align="left">Instructions stored on disk</td><td align="left">01.1 — the file you save</td></tr>
<tr><td align="left"><b>Process</b></td><td align="left">A running program with live state in memory</td><td align="left">01.1 — what starts when you run it</td></tr>
<tr><td align="left"><b>Source code</b></td><td align="left">Human-readable instructions you write</td><td align="left">01.1 — written for humans, not machines</td></tr>
<tr><td align="left"><b>Machine code</b></td><td align="left">Binary instructions the CPU executes directly</td><td align="left">01.2 — what the processor truly understands</td></tr>
<tr><td align="left"><b>Bytecode</b></td><td align="left">Intermediate instructions the Python VM executes</td><td align="left">01.4 — inspect it with <code>dis</code> in Chapter 43</td></tr>
<tr><td align="left"><b>Algorithm</b></td><td align="left">Finite, unambiguous sequence of steps solving a problem</td><td align="left">01.3 — the thinking half of the job</td></tr>
<tr><td align="left"><b>Pseudocode</b></td><td align="left">Structured English description of an algorithm</td><td align="left">01.3 — write this before any code</td></tr>
<tr><td align="left"><b>Compiler</b></td><td align="left">Translates all source to machine code ahead of time</td><td align="left">01.4 — how C and Rust work</td></tr>
<tr><td align="left"><b>Interpreter</b></td><td align="left">Reads and executes source as it goes</td><td align="left">01.4 — how Python mostly works</td></tr>
<tr><td align="left"><b>Paradigm</b></td><td align="left">A style of organising code</td><td align="left">01.5 — Chapters 16, 24–28, 31</td></tr>
<tr><td align="left"><b>CPython</b></td><td align="left">The reference Python implementation, written in C</td><td align="left">01.8 — almost certainly what you run</td></tr>
<tr><td align="left"><b>PVM</b></td><td align="left">Python Virtual Machine — executes bytecode</td><td align="left">01.4 — the "interpreted" half of Python</td></tr>
<tr><td align="left"><b>GIL</b></td><td align="left">Global Interpreter Lock — limits CPU parallelism across threads</td><td align="left">01.8 — the full story in Chapter 33</td></tr>
<tr><td align="left"><b>Pythonic</b></td><td align="left">Idiomatic Python, following the language's conventions</td><td align="left">01.6 — an instinct you build over time</td></tr>
</table>

---

## Next

**Chapter 02 — Setup and First Program.** Install Python, meet the REPL, set up VS Code, understand virtual environments, and run real code.
