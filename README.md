# Python Learning

A complete, chapter-by-chapter Python course — from "what is programming" all the way to language internals, packaging, and real projects.

Every topic is explained in a written lesson first, then demonstrated in runnable **Jupyter notebooks**. Each notebook alternates explanation and code, so you read a concept and then run it in the very next cell. Code is deliberately plain and readable: no clever one-liners, no unnecessary abstraction, and a comment above every meaningful line explaining what it does and why.

- **Python version:** 3.12+
- **Prerequisites:** none — Chapter 01 starts from zero

---

## How to Use This Repo

1. Work through chapters in order. Each one builds on the previous.
2. Read the chapter `README.md` first — that's the theory.
3. Open each numbered notebook and run the cells top to bottom.
4. Change a cell and run it again. Breaking things on purpose is how you learn what the rules actually are.
5. Do the exercises notebook at the end of each chapter before moving on.

### Setup

```bash
# create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# install Jupyter
pip install jupyterlab
```

### Running a notebook

```bash
# from the repository root
jupyter lab
```

Then open any `.ipynb` file. VS Code also opens notebooks natively — install the Python and Jupyter extensions and click a file.

### Folder layout

```
01. Introduction to Programming/
├── README.md                        # chapter theory and notes
├── 01.1 what_is_programming.ipynb   # one notebook per subchapter
├── 01.2 how_computers_execute.ipynb
└── exercises.ipynb                  # practice problems
```

---

## Progress Tracker

Tick a chapter when you have read the notes, run every example, and finished the exercises.

| ✅ | Ch | Chapter | What You'll Learn | Topics | Status |
|:--:|:--:|:-----------|:-------------------|:--:|:-----------|
| ⬜ | **01** | Introduction to Programming | Think like a programmer before writing any code | 8 | In progress |
| ⬜ | **02** | Setup and First Program | Get Python installed and run your first script | 7 | Not started |
| ⬜ | **03** | Syntax Fundamentals | Read and write correctly formed Python | 7 | Not started |
| ⬜ | **04** | Variables and Memory Model | Understand what a variable really is | 8 | Not started |
| ⬜ | **05** | Data Types — Numbers and Booleans | Work with every kind of number Python offers | 8 | Not started |
| ⬜ | **06** | Operators | Combine and compare values correctly | 9 | Not started |
| ⬜ | **07** | Strings | Handle text confidently, including Unicode | 11 | Not started |
| ⬜ | **08** | Input, Output, and Basic I/O | Talk to the user and the command line | 4 | Not started |
| ⬜ | **09** | Control Flow — Conditionals | Make your programs take decisions | 5 | Not started |
| ⬜ | **10** | Control Flow — Loops | Repeat work without repeating yourself | 9 | Not started |
| ⬜ | **11** | Lists | Store ordered, changeable collections | 9 | Not started |
| ⬜ | **12** | Tuples | Store fixed records that cannot change | 7 | Not started |
| ⬜ | **13** | Sets and Frozensets | Handle uniqueness and fast membership tests | 7 | Not started |
| ⬜ | **14** | Dictionaries | Look data up instantly by key | 10 | Not started |
| ⬜ | **15** | Comprehensions | Build collections in one readable line | 7 | Not started |
| ⬜ | **16** | Functions — Fundamentals | Package logic into reusable functions | 9 | Not started |
| ⬜ | **17** | Functions — Scope and Advanced | Master scope, closures and higher-order functions | 9 | Not started |
| ⬜ | **18** | Decorators | Add behaviour to functions without editing them | 7 | Not started |
| ⬜ | **19** | Iterators and Generators | Process data too large to fit in memory | 9 | Not started |
| ⬜ | **20** | Modules and Packages | Split a program across many files | 10 | Not started |
| ⬜ | **21** | Standard Library Tour | Solve common problems with zero installs | 12 | Not started |
| ⬜ | **22** | File Handling | Read and write files of every kind | 12 | Not started |
| ⬜ | **23** | Error Handling and Exceptions | Handle failure without crashing | 12 | Not started |
| ⬜ | **24** | OOP — Fundamentals | Model your problem domain with classes | 9 | Not started |
| ⬜ | **25** | OOP — Encapsulation and Properties | Control access to an object's internals | 6 | Not started |
| ⬜ | **26** | OOP — Inheritance and Polymorphism | Share and specialise behaviour between classes | 9 | Not started |
| ⬜ | **27** | OOP — Magic Methods | Make your objects work with Python's syntax | 10 | Not started |
| ⬜ | **28** | OOP — Advanced | Use the modern tools that cut boilerplate | 10 | Not started |
| ⬜ | **29** | Context Managers | Manage resources that must be cleaned up | 6 | Not started |
| ⬜ | **30** | Regular Expressions | Search and transform text by pattern | 10 | Not started |
| ⬜ | **31** | Functional Programming | Write predictable, side-effect-free code | 7 | Not started |
| ⬜ | **32** | Type Hints and Static Typing | Catch type bugs before running the code | 8 | Not started |
| ⬜ | **33** | Concurrency — Threading | Run work concurrently, and know the GIL's limits | 8 | Not started |
| ⬜ | **34** | Concurrency — Multiprocessing | Use every CPU core for heavy work | 6 | Not started |
| ⬜ | **35** | Asynchronous Programming | Handle thousands of I/O operations at once | 9 | Not started |
| ⬜ | **36** | Testing | Prove your code works, and keep it working | 10 | Not started |
| ⬜ | **37** | Debugging, Logging, Profiling | Find bugs and bottlenecks systematically | 8 | Not started |
| ⬜ | **38** | Working with Data Formats and APIs | Exchange data with files and web services | 7 | Not started |
| ⬜ | **39** | Databases | Store data that outlives your program | 6 | Not started |
| ⬜ | **40** | Project Structure and Packaging | Turn your code into an installable package | 7 | Not started |
| ⬜ | **41** | Code Quality and Tooling | Write code a team can maintain | 7 | Not started |
| ⬜ | **42** | Security Basics | Avoid the mistakes that cause breaches | 5 | Not started |
| ⬜ | **43** | Advanced Internals | Understand what Python does under the hood | 7 | Not started |
| ⬜ | **44** | Projects | Apply everything to real, complete programs | 8 | Not started |
| ⬜ | **45** | Appendix | Look things up fast when you need them | 6 | Not started |

---

## Full Syllabus

### 01. Introduction to Programming

| # | Topic | Covers |
|:--|:------|:-------|
| **01.1** | What is Programming | instructions, precision, program vs process |
| **01.2** | How Computers Execute Code | CPU, memory, binary, machine code |
| **01.3** | Algorithms and Pseudocode | steps, decomposition, the three building blocks |
| **01.4** | Compiled vs Interpreted Languages | bytecode, the PVM, `__pycache__` |
| **01.5** | Programming Paradigms Overview | procedural, OOP, functional |
| **01.6** | What is Python | history, philosophy, Zen of Python, versions |
| **01.7** | Where Python is Used | the domains it leads, and where it is the wrong tool |
| **01.8** | CPython vs PyPy vs Other Implementations | the reference implementation, JIT, the GIL |

### 02. Setup and First Program

| # | Topic | Covers |
|:--|:------|:-------|
| **02.1** | Installing Python | Windows/macOS/Linux |
| **02.2** | Python Interpreter and REPL | interactive mode, `help()`, `dir()` |
| **02.3** | Editors and IDEs | VS Code setup |
| **02.4** | Writing and Running First Script | your first file, running it from a terminal |
| **02.5** | Virtual Environments Intro | `venv` |
| **02.6** | `pip` Basics | installing, upgrading, freezing, uninstalling |
| **02.7** | Anatomy of a Python File | shebang, encoding, `__main__` |

### 03. Syntax Fundamentals

| # | Topic | Covers |
|:--|:------|:-------|
| **03.1** | Statements and Expressions | what evaluates to a value, and what does not |
| **03.2** | Indentation Rules and Blocks | whitespace as syntax, nesting, `IndentationError` |
| **03.3** | Comments | single, multi-line, docstrings |
| **03.4** | Line Continuation | implicit vs explicit, backslashes, brackets |
| **03.5** | Keywords and Identifiers | reserved words, valid names, naming rules |
| **03.6** | PEP 8 Introduction | the style guide every Python project follows |
| **03.7** | Common Beginner Syntax Errors | reading and fixing the errors beginners hit most |

### 04. Variables and Memory Model

| # | Topic | Covers |
|:--|:------|:-------|
| **04.1** | Variables and Assignment | binding a name to a value |
| **04.2** | Names, Objects, References | why a variable is a label, not a box |
| **04.3** | `id()`, `type()`, and Object Identity | what an object actually is, and how to inspect one |
| **04.4** | Mutable vs Immutable Objects | which types can change in place, and which cannot |
| **04.5** | Reference Semantics and Aliasing | why two names can point at one object |
| **04.6** | Garbage Collection and Reference Counting | how Python frees memory you stopped using |
| **04.7** | Constants and Naming Conventions | `UPPER_CASE`, `snake_case`, `_private` |
| **04.8** | Multiple Assignment and Swapping | `a, b = 1, 2` and `a, b = b, a` |

### 05. Data Types — Numbers and Booleans

| # | Topic | Covers |
|:--|:------|:-------|
| **05.1** | Integers | arbitrary precision, bases |
| **05.2** | Floats | IEEE 754, precision pitfalls |
| **05.3** | Complex Numbers | real and imaginary parts, `j` notation |
| **05.4** | `Decimal` and `Fraction` | exact arithmetic when floats will not do |
| **05.5** | Booleans and Truthiness | what counts as `True`, what counts as `False` |
| **05.6** | `None` Type | absence of a value, and why it is not zero |
| **05.7** | Type Conversion / Casting | `int()`, `float()`, `str()`, `bool()` |
| **05.8** | `math` Module Essentials | rounding, roots, logs, constants |

### 06. Operators

| # | Topic | Covers |
|:--|:------|:-------|
| **06.1** | Arithmetic Operators | `+  -  *  /  //  %  **` |
| **06.2** | Comparison Operators and Chaining | `==  !=  <  >  <=  >=` and `a < b < c` |
| **06.3** | Logical Operators and Short-Circuiting | `and`, `or`, `not`, and lazy evaluation |
| **06.4** | Assignment and Augmented Assignment | `=`, `+=`, `-=`, `*=` and friends |
| **06.5** | Bitwise Operators | `&`, `\|`, `^`, `~`, `<<`, `>>` |
| **06.6** | Identity Operators | `is`, `is not` |
| **06.7** | Membership Operators | `in`, `not in` |
| **06.8** | Operator Precedence and Associativity | what binds tightest, and when to add brackets |
| **06.9** | Walrus Operator | `:=` |

### 07. Strings

| # | Topic | Covers |
|:--|:------|:-------|
| **07.1** | String Literals and Quoting | single, double, triple quotes |
| **07.2** | Indexing and Slicing | `[i]`, `[a:b]`, `[a:b:step]`, negative indices |
| **07.3** | String Immutability | why strings cannot be changed in place |
| **07.4** | String Methods | complete tour |
| **07.5** | Formatting: f-strings | the modern way to build strings |
| **07.6** | Formatting: `.format()` and `%` | the older styles, and where you still meet them |
| **07.7** | Format Spec Mini-Language | padding, alignment, precision, thousands separators |
| **07.8** | Escape Sequences and Raw Strings | `\n`, `\t`, `\\` and `r"raw"` strings |
| **07.9** | Unicode, Encoding, `bytes` vs `str` | text vs bytes, and why encoding errors happen |
| **07.10** | String Concatenation Performance | `join` |
| **07.11** | `textwrap` and the `string` Module | wrapping paragraphs, and useful constants |

### 08. Input, Output, and Basic I/O

| # | Topic | Covers |
|:--|:------|:-------|
| **08.1** | `print | )` in Depth (sep, end, file, flush |
| **08.2** | `input()` and Parsing User Input | reading input safely, and converting it |
| **08.3** | Command-Line Arguments | `sys.argv` |
| **08.4** | Formatted Console Output | aligning columns and building readable reports |

### 09. Control Flow — Conditionals

| # | Topic | Covers |
|:--|:------|:-------|
| **09.1** | `if` / `elif` / `else` | branching on a condition |
| **09.2** | Nested Conditionals | conditions inside conditions, and when to flatten them |
| **09.3** | Conditional (Ternary) Expressions | `value_if_true if condition else value_if_false` |
| **09.4** | `match` Statement — Structural Pattern Matching | matching shapes, not just values |
| **09.5** | Guard Clauses and Readable Conditions | returning early to keep code flat and readable |

### 10. Control Flow — Loops

| # | Topic | Covers |
|:--|:------|:-------|
| **10.1** | `while` Loops | repeating while a condition holds |
| **10.2** | `for` Loops and Iterables | repeating once per item |
| **10.3** | `range()` in Depth | start, stop, step, and why the stop is excluded |
| **10.4** | `break`, `continue`, `pass` | leaving early, skipping ahead, doing nothing |
| **10.5** | `else` Clause on Loops | the clause almost nobody knows about |
| **10.6** | Nested Loops | loops inside loops, and their cost |
| **10.7** | `enumerate()` and `zip()` | looping with a counter, and looping over pairs |
| **10.8** | Infinite Loops and Loop Safety | how to avoid a program that never stops |
| **10.9** | Loop Performance Notes | what makes a loop slow, and what to do about it |

### 11. Lists

| # | Topic | Covers |
|:--|:------|:-------|
| **11.1** | Creating and Accessing Lists | creating, indexing, changing items |
| **11.2** | Slicing | including step and negative indices |
| **11.3** | List Methods | complete |
| **11.4** | Mutability and In-Place Operations | changing a list in place vs building a new one |
| **11.5** | Sorting | `sort` vs `sorted`, `key`, `reverse` |
| **11.6** | Nested Lists and Matrices | lists inside lists, and grids |
| **11.7** | Copying: Shallow vs Deep | `copy` module |
| **11.8** | Lists as Stacks and Queues | last-in-first-out and first-in-first-out |
| **11.9** | Common List Pitfalls | mutable default, `*` copy |

### 12. Tuples

| # | Topic | Covers |
|:--|:------|:-------|
| **12.1** | Creating Tuples and the Single-Element Trap | why `(5)` is not a tuple but `(5,)` is |
| **12.2** | Immutability and When to Use Tuples | fixed collections, and where they beat lists |
| **12.3** | Tuple Methods and Operations | `count`, `index`, concatenation, repetition |
| **12.4** | Packing and Unpacking | `point = 3, 4` and `x, y = point` |
| **12.5** | Extended Unpacking | `*rest` |
| **12.6** | Tuples as Dictionary Keys | why tuples can be keys but lists cannot |
| **12.7** | `namedtuple` Preview | tuples with named fields |

### 13. Sets and Frozensets

| # | Topic | Covers |
|:--|:------|:-------|
| **13.1** | Creating Sets, Uniqueness | unordered collections with no duplicates |
| **13.2** | Set Methods | `add`, `remove`, `discard`, `pop`, `update` |
| **13.3** | Set Operations | union, intersection, difference, symmetric difference |
| **13.4** | Subset / Superset / Disjoint | comparing one set against another |
| **13.5** | `frozenset` | the immutable set |
| **13.6** | The Hashability Requirement | what can go in a set, and why |
| **13.7** | Performance: Set vs List Lookup | why membership testing is dramatically faster |

### 14. Dictionaries

| # | Topic | Covers |
|:--|:------|:-------|
| **14.1** | Creating and Accessing Dictionaries | key-value pairs, lookup by key |
| **14.2** | Dictionary Methods | complete |
| **14.3** | Keys, Values, and Items Views | live views, and how they differ from lists |
| **14.4** | Iterating Dictionaries | looping over keys, values, or both |
| **14.5** | Nested Dictionaries | dictionaries inside dictionaries |
| **14.6** | `get`, `setdefault`, `pop`, and Missing Keys | handling a key that might not be there |
| **14.7** | Merging Dicts | `\|`, `update`, `**` — three ways to combine |
| **14.8** | Dict Ordering Guarantees | insertion order, guaranteed since 3.7 |
| **14.9** | Hashing and Key Requirements | what makes a valid key |
| **14.10** | Dict Performance | why lookup is fast no matter how big it gets |

### 15. Comprehensions

| # | Topic | Covers |
|:--|:------|:-------|
| **15.1** | List Comprehensions | building a list in one readable line |
| **15.2** | Conditional Comprehensions | filtering while you build |
| **15.3** | Nested Comprehensions | comprehensions inside comprehensions, and their limits |
| **15.4** | Dict Comprehensions | building dictionaries the same way |
| **15.5** | Set Comprehensions | building sets the same way |
| **15.6** | Generator Expressions | the lazy version that does not build a list |
| **15.7** | Readability Limits — When Not to Use Them | when a plain loop is the better choice |

### 16. Functions — Fundamentals

| # | Topic | Covers |
|:--|:------|:-------|
| **16.1** | Defining and Calling Functions | `def`, arguments, calling |
| **16.2** | Positional Arguments | arguments matched by position |
| **16.3** | Keyword Arguments | arguments matched by name |
| **16.4** | Default Parameters and the Mutable Default Trap | the classic bug that catches everyone once |
| **16.5** | `*args` and `**kwargs` | accepting any number of arguments |
| **16.6** | Positional-Only (`/`) and Keyword-Only (`*`) Parameters | controlling how your function may be called |
| **16.7** | Return Values and Multiple Returns | `return`, returning several values at once |
| **16.8** | Docstrings | PEP 257 |
| **16.9** | Functions as First-Class Objects | passing functions around like any other value |

### 17. Functions — Scope and Advanced

| # | Topic | Covers |
|:--|:------|:-------|
| **17.1** | Scope and the LEGB Rule | local, enclosing, global, built-in |
| **17.2** | `global` and `nonlocal` | reaching outward to reassign a name |
| **17.3** | Closures | functions that remember where they came from |
| **17.4** | Lambda Functions | small anonymous functions |
| **17.5** | Recursion and Recursion Limits | functions that call themselves, and when to stop |
| **17.6** | Higher-Order Functions | `map`, `filter`, `reduce` |
| **17.7** | `functools` | `partial`, `lru_cache`, `wraps`, `reduce` |
| **17.8** | Pure Functions and Side Effects | why predictable functions are easier to trust |
| **17.9** | Function Annotations / Type Hints | documenting the types a function expects |

### 18. Decorators

| # | Topic | Covers |
|:--|:------|:-------|
| **18.1** | Decorator Theory | wrapping a function to add behaviour |
| **18.2** | Writing Simple Decorators | your first working decorator |
| **18.3** | Decorators with Arguments | decorators you can configure |
| **18.4** | `functools.wraps` | keeping the wrapped function's identity |
| **18.5** | Stacking Decorators | applying several at once, and the order they run |
| **18.6** | Class Decorators | decorating a class instead of a function |
| **18.7** | Practical Decorators | timing, retry, logging, caching |

### 19. Iterators and Generators

| # | Topic | Covers |
|:--|:------|:-------|
| **19.1** | Iterable vs Iterator Protocol | the difference, and why it matters |
| **19.2** | `iter()` and `next()` | the two functions behind every `for` loop |
| **19.3** | Building Custom Iterators | writing your own |
| **19.4** | Generators and `yield` | pausing and resuming a function |
| **19.5** | Generator Expressions | generators without the `def` |
| **19.6** | `yield from` | delegating to another generator |
| **19.7** | Sending Values into Generators | `send`, `throw`, `close` |
| **19.8** | Lazy Evaluation and Memory Benefits | handling data too big to fit in memory |
| **19.9** | `itertools` Complete Tour | chaining, grouping, combining, cycling |

### 20. Modules and Packages

| # | Topic | Covers |
|:--|:------|:-------|
| **20.1** | What is a Module | one file, importable from another |
| **20.2** | `import` Forms and Aliasing | `import x`, `from x import y`, `as` |
| **20.3** | Module Search Path | `sys.path` |
| **20.4** | `if __name__ == "__main__"` | running a file vs importing it |
| **20.5** | Creating Packages and `__init__.py` | turning a folder into an importable package |
| **20.6** | Relative vs Absolute Imports | `from .sibling import x` vs `from package.module import x` |
| **20.7** | Namespace Packages | packages without an `__init__.py` |
| **20.8** | Circular Imports and How to Avoid Them | why they happen, and how to restructure |
| **20.9** | Reloading Modules | re-importing without restarting |
| **20.10** | `__all__` and the Public API | controlling what `from x import *` exposes |

### 21. Standard Library Tour

| # | Topic | Covers |
|:--|:------|:-------|
| **21.1** | `os` and `sys` | environment, paths, arguments, the interpreter itself |
| **21.2** | `pathlib` | the modern way to handle file paths |
| **21.3** | `datetime`, `time`, `zoneinfo` | dates, times, durations, time zones |
| **21.4** | `random` and `secrets` | random for simulations, secrets for security |
| **21.5** | `collections` | `Counter`, `defaultdict`, `deque`, `OrderedDict`, `namedtuple`, `ChainMap` |
| **21.6** | `json`, `csv`, `pickle` | the three formats you will use constantly |
| **21.7** | `re` Preview | a first look before the full chapter |
| **21.8** | `argparse` | building real command-line tools |
| **21.9** | `logging` | recording what your program did |
| **21.10** | `subprocess` | running other programs from Python |
| **21.11** | `shutil`, `glob`, `tempfile` | copying, finding, and scratch files |
| **21.12** | `statistics`, `enum`, `uuid`, `hashlib` | averages, constants, unique ids, hashing |

### 22. File Handling

| # | Topic | Covers |
|:--|:------|:-------|
| **22.1** | Opening and Closing Files, File Modes | `r`, `w`, `a`, `x`, `b`, `+` |
| **22.2** | Reading Files | `read`, `readline`, `readlines`, iteration |
| **22.3** | Writing and Appending | creating files and adding to them |
| **22.4** | Context Managers | `with` |
| **22.5** | Binary Files | working with bytes instead of text |
| **22.6** | Encodings and `newline` | getting text right across platforms |
| **22.7** | File Positions | `seek`, `tell` |
| **22.8** | `os` and `pathlib` File Operations | creating, moving, renaming, deleting |
| **22.9** | Working with CSV | reading and writing spreadsheet data |
| **22.10** | Working with JSON | reading and writing structured data |
| **22.11** | Serialization: `pickle` | saving Python objects, and why it is risky |
| **22.12** | Temporary Files and Directories | scratch space that cleans itself up |

### 23. Error Handling and Exceptions

| # | Topic | Covers |
|:--|:------|:-------|
| **23.1** | Errors vs Exceptions | theory |
| **23.2** | The Exception Hierarchy | what inherits from what, and why you care |
| **23.3** | `try` / `except` | catching what goes wrong |
| **23.4** | Multiple and Grouped Excepts | handling several failure modes |
| **23.5** | `else` and `finally` | the two clauses people forget |
| **23.6** | `raise` and Re-Raising | raising your own, and passing one along |
| **23.7** | Exception Chaining | `from` |
| **23.8** | Custom Exception Classes | errors that describe your own problem domain |
| **23.9** | `assert` and Assertions | checking assumptions during development |
| **23.10** | Exception Groups and `except*` | handling several errors at once |
| **23.11** | EAFP vs LBYL | ask forgiveness, or ask permission |
| **23.12** | Best Practices and Anti-Patterns | what to catch, what to let through |

### 24. OOP — Fundamentals

| # | Topic | Covers |
|:--|:------|:-------|
| **24.1** | OOP Theory | objects, classes, abstraction |
| **24.2** | Defining Classes, Creating Instances | `class`, instances, the basics |
| **24.3** | Instance Attributes and `self` | data that belongs to one object |
| **24.4** | The `__init__` Constructor | setting an object up when it is created |
| **24.5** | Class Attributes vs Instance Attributes | shared by all, vs owned by one |
| **24.6** | Instance Methods | functions that belong to an object |
| **24.7** | Class Methods and `@classmethod` | methods that work on the class itself |
| **24.8** | Static Methods and `@staticmethod` | methods that need neither instance nor class |
| **24.9** | `__del__` and Object Lifecycle | creation, use, and cleanup |

### 25. OOP — Encapsulation and Properties

| # | Topic | Covers |
|:--|:------|:-------|
| **25.1** | Public, Protected, and Private Conventions | `name`, `_name`, `__name` |
| **25.2** | Name Mangling | what `__name` actually does |
| **25.3** | Getters and Setters | controlling access to an attribute |
| **25.4** | The `@property` Decorator | methods that look like plain attributes |
| **25.5** | Computed Attributes | values worked out on demand |
| **25.6** | `__slots__` | trading flexibility for memory |

### 26. OOP — Inheritance and Polymorphism

| # | Topic | Covers |
|:--|:------|:-------|
| **26.1** | Single Inheritance | one class building on another |
| **26.2** | `super()` in Depth | calling up to the parent, correctly |
| **26.3** | Method Overriding | replacing a parent's behaviour |
| **26.4** | Multiple Inheritance | inheriting from several classes at once |
| **26.5** | Method Resolution Order (MRO) and C3 Linearization | the rule that decides which method wins |
| **26.6** | Mixins | small reusable behaviour, added by inheritance |
| **26.7** | Polymorphism and Duck Typing | if it quacks, it is a duck |
| **26.8** | `isinstance` vs `type` vs Duck Typing | three ways to ask what something is |
| **26.9** | Composition vs Inheritance | has-a, or is-a |

### 27. OOP — Magic Methods

| # | Topic | Covers |
|:--|:------|:-------|
| **27.1** | `__str__` vs `__repr__` | friendly text, and unambiguous text |
| **27.2** | Comparison Dunders | `__eq__`, `__lt__`, … |
| **27.3** | `__hash__` and the Hashability Contract | making your objects usable as keys |
| **27.4** | Arithmetic Operator Overloading | making `+`, `-`, `*` work on your own types |
| **27.5** | Container Dunders | `__len__`, `__getitem__`, `__contains__`, `__iter__` |
| **27.6** | Callable Objects | `__call__` |
| **27.7** | Attribute Access | `__getattr__`, `__setattr__`, `__getattribute__` |
| **27.8** | The Context Manager Protocol | `__enter__`, `__exit__` |
| **27.9** | `__new__` vs `__init__` | creating an object, vs setting it up |
| **27.10** | Complete Dunder Reference | the full list, in one place |

### 28. OOP — Advanced

| # | Topic | Covers |
|:--|:------|:-------|
| **28.1** | Abstract Base Classes | `abc` |
| **28.2** | Protocols and Structural Typing | typing by shape, not by inheritance |
| **28.3** | `dataclasses` Complete | classes that write their own boilerplate |
| **28.4** | `enum` Complete | fixed sets of named values |
| **28.5** | `NamedTuple` and `TypedDict` | typed records and typed dictionaries |
| **28.6** | Descriptors | the machinery behind `@property` |
| **28.7** | Metaclasses | classes that build classes |
| **28.8** | Class Creation Hooks | `__init_subclass__`, `__set_name__` |
| **28.9** | Design Patterns in Python | singleton, factory, observer, strategy |
| **28.10** | SOLID Principles in Python | five design principles, with Python examples |

### 29. Context Managers

| # | Topic | Covers |
|:--|:------|:-------|
| **29.1** | `with` Statement Theory | why `with` exists |
| **29.2** | Class-Based Context Managers | `__enter__` and `__exit__` |
| **29.3** | `contextlib.contextmanager` | the decorator that turns a generator into one |
| **29.4** | `contextlib` Utilities | `suppress`, `closing`, `ExitStack` |
| **29.5** | Multiple Context Managers | managing several resources at once |
| **29.6** | Async Context Managers Preview | `async with`, previewing Chapter 35 |

### 30. Regular Expressions

| # | Topic | Covers |
|:--|:------|:-------|
| **30.1** | Regex Theory and Syntax | what a pattern is, and how matching works |
| **30.2** | Character Classes and Quantifiers | `\d`, `\w`, `[a-z]`, `*`, `+`, `?`, `{n,m}` |
| **30.3** | Anchors and Boundaries | `^`, `$`, `\b` |
| **30.4** | Groups and Capturing | pulling pieces out of a match |
| **30.5** | Named Groups, Lookahead, Lookbehind | readable groups, and matching by context |
| **30.6** | `re` Module Functions | `match`, `search`, `findall`, `finditer`, `sub` |
| **30.7** | Flags | case-insensitive, multiline, verbose |
| **30.8** | Substitution and Splitting | find and replace, and splitting on a pattern |
| **30.9** | Greedy vs Lazy, Catastrophic Backtracking | how a regex can hang your program |
| **30.10** | Practical Patterns | emails, dates, log lines, and how to test them |

### 31. Functional Programming

| # | Topic | Covers |
|:--|:------|:-------|
| **31.1** | Functional Concepts in Python | what transfers from functional languages, and what does not |
| **31.2** | Immutability Practices | working without changing state |
| **31.3** | `map`, `filter`, `reduce` Deep Dive | the three classic transformations |
| **31.4** | Function Composition | building big functions out of small ones |
| **31.5** | Currying and Partial Application | fixing some arguments now, the rest later |
| **31.6** | The `operator` Module | operators as functions you can pass around |
| **31.7** | Limits of FP in Python | why Python is not Haskell, and why that is fine |

### 32. Type Hints and Static Typing

| # | Topic | Covers |
|:--|:------|:-------|
| **32.1** | Why Type Hints | catching bugs before you run the code |
| **32.2** | Basic Annotations | annotating arguments, returns, and variables |
| **32.3** | `typing` Module Core | `Optional`, `Union`, `Any`, `Literal` |
| **32.4** | Generics and `TypeVar` | types that work with any contained type |
| **32.5** | Modern Syntax | `list[int]` and `X \| Y`, replacing `List` and `Union` |
| **32.6** | `Callable`, `Protocol`, `Self` | typing functions, shapes, and returns |
| **32.7** | Using `mypy` | running a type checker over your code |
| **32.8** | Runtime Type Checking and Its Limits | what type hints do not do |

### 33. Concurrency — Threading

| # | Topic | Covers |
|:--|:------|:-------|
| **33.1** | Concurrency vs Parallelism | theory |
| **33.2** | Processes vs Threads | the real difference, and when each applies |
| **33.3** | The GIL Explained | why threads do not speed up CPU work |
| **33.4** | The `threading` Module | starting, joining, and managing threads |
| **33.5** | Locks, RLocks, Semaphores, Events | coordinating threads safely |
| **33.6** | Race Conditions and Deadlocks | the two classic threading bugs |
| **33.7** | `queue` for Thread Communication | passing work between threads safely |
| **33.8** | `concurrent.futures.ThreadPoolExecutor` | the high-level way to run threads |

### 34. Concurrency — Multiprocessing

| # | Topic | Covers |
|:--|:------|:-------|
| **34.1** | The `multiprocessing` Module | true parallelism, at a cost |
| **34.2** | Process Pools | spreading work across CPU cores |
| **34.3** | Inter-Process Communication | Pipes, Queues |
| **34.4** | Shared Memory | sharing memory instead of copying |
| **34.5** | `ProcessPoolExecutor` | the high-level way to run processes |
| **34.6** | Choosing Threads vs Processes vs Async | a decision guide you can actually use |

### 35. Asynchronous Programming

| # | Topic | Covers |
|:--|:------|:-------|
| **35.1** | Async Theory and the Event Loop | how one thread does many things at once |
| **35.2** | `async` / `await` Syntax | the two keywords that drive it all |
| **35.3** | Coroutines and Tasks | scheduling work, and waiting for it |
| **35.4** | `asyncio.gather`, `wait`, `TaskGroup` | running many things concurrently |
| **35.5** | Async Iterators and Generators | `async for` and `yield` together |
| **35.6** | Async Context Managers | `async with` |
| **35.7** | Timeouts and Cancellation | giving up on work that takes too long |
| **35.8** | Mixing Sync and Async Code | the traps at the boundary |
| **35.9** | Practical Async I/O | files and network, without blocking |

### 36. Testing

| # | Topic | Covers |
|:--|:------|:-------|
| **36.1** | Why Test — Theory and Test Types | unit, integration, end-to-end, and what to test |
| **36.2** | `unittest` Basics | the testing framework in the standard library |
| **36.3** | Assertions and Test Fixtures | checking results, and setting up test data |
| **36.4** | `pytest` Basics | the framework most projects actually use |
| **36.5** | `pytest` Fixtures | reusable setup, done properly |
| **36.6** | Parametrized Tests | one test, many inputs |
| **36.7** | Mocking | `unittest.mock`, `monkeypatch` |
| **36.8** | Test Coverage | measuring what your tests actually reach |
| **36.9** | `doctest` | tests that live inside your docstrings |
| **36.10** | The TDD Workflow | write the test first, then the code |

### 37. Debugging, Logging, Profiling

| # | Topic | Covers |
|:--|:------|:-------|
| **37.1** | Reading Tracebacks | reading an error from the bottom up |
| **37.2** | Debugging with `print` vs a Debugger | when each one is the right tool |
| **37.3** | `pdb` / `breakpoint()` | stepping through code line by line |
| **37.4** | The VS Code Debugger | breakpoints, watches, and the call stack |
| **37.5** | `logging` Deep Dive | levels, handlers, formatters, config |
| **37.6** | Profiling | `timeit`, `cProfile`, memory |
| **37.7** | Optimization Strategies | measure first, then optimise |
| **37.8** | Big-O Basics for Python Data Structures | why the right data structure beats clever code |

### 38. Working with Data Formats and APIs

| # | Topic | Covers |
|:--|:------|:-------|
| **38.1** | JSON Deep Dive | nested data, custom encoders, common errors |
| **38.2** | CSV Deep Dive | delimiters, quoting, headers, dialects |
| **38.3** | XML and YAML | when you meet them, and how to handle them |
| **38.4** | HTTP Basics | requests, responses, status codes, headers |
| **38.5** | `urllib` and `requests` | fetching data over the network |
| **38.6** | Consuming REST APIs | authentication, pagination, error handling |
| **38.7** | Web Scraping Basics (`BeautifulSoup`) and Ethics | parsing HTML, and scraping responsibly |

### 39. Databases

| # | Topic | Covers |
|:--|:------|:-------|
| **39.1** | Database Theory and SQL Refresher | tables, rows, keys, and the queries you need |
| **39.2** | The `sqlite3` Module | a real database with no server to install |
| **39.3** | CRUD Operations | create, read, update, delete |
| **39.4** | Parameterized Queries and SQL Injection | the single most important security habit here |
| **39.5** | Transactions | all-or-nothing changes |
| **39.6** | ORM Introduction | SQLAlchemy basics |

### 40. Project Structure and Packaging

| # | Topic | Covers |
|:--|:------|:-------|
| **40.1** | Project Layout Conventions | `src` layout |
| **40.2** | `requirements.txt` vs `pyproject.toml` | declaring what your project needs |
| **40.3** | Dependency Management Tools | `pip-tools`, `poetry`, `uv` |
| **40.4** | Building a Distributable Package | turning your code into something installable |
| **40.5** | Publishing to PyPI | sharing your package with the world |
| **40.6** | Entry Points and CLI Tools | making your package runnable as a command |
| **40.7** | Semantic Versioning | what the numbers in `1.4.2` actually promise |

### 41. Code Quality and Tooling

| # | Topic | Covers |
|:--|:------|:-------|
| **41.1** | PEP 8 Deep Dive | naming, spacing, imports, line length |
| **41.2** | Linters | `ruff`, `flake8`, `pylint` |
| **41.3** | Formatters | `black`, `ruff format` |
| **41.4** | Pre-commit Hooks | running checks automatically before each commit |
| **41.5** | Docstring Standards and `sphinx` / `mkdocs` | writing docs people will actually read |
| **41.6** | Code Smells and Refactoring | recognising bad code, and improving it safely |
| **41.7** | Clean Code Principles | naming, function size, and single responsibility |

### 42. Security Basics

| # | Topic | Covers |
|:--|:------|:-------|
| **42.1** | Input Validation | never trust what comes in from outside |
| **42.2** | Secrets Management | `.env`, environment variables |
| **42.3** | Hashing and Passwords | storing passwords so a leak is survivable |
| **42.4** | Common Python Vulnerabilities | `eval`, `pickle`, path traversal |
| **42.5** | Dependency Security | auditing what your dependencies bring with them |

### 43. Advanced Internals

| # | Topic | Covers |
|:--|:------|:-------|
| **43.1** | Bytecode and `dis` | seeing the instructions your code compiles to |
| **43.2** | Memory Management Deep Dive | reference counting, and the object model |
| **43.3** | The `gc` Module and Circular References | the collector that catches what counting misses |
| **43.4** | `weakref` | references that do not keep an object alive |
| **43.5** | Interning and the Small Integer Cache | why `a is b` is sometimes surprisingly `True` |
| **43.6** | `sys` Internals | recursion limits, sizes, and interpreter internals |
| **43.7** | C Extensions and `ctypes` Introduction | calling C code from Python |

### 44. Projects

| # | Topic | Covers |
|:--|:------|:-------|
| **44.1** | Beginner: CLI Calculator / Number Game | input, conditionals, loops, functions |
| **44.2** | Beginner: Text File Word Counter | file reading, dictionaries, sorting |
| **44.3** | Intermediate: To-Do CLI with JSON Storage | persistence, JSON, and a real command-line interface |
| **44.4** | Intermediate: API Data Fetcher | HTTP, JSON parsing, error handling |
| **44.5** | OOP: Bank / Library Management System | classes, inheritance, encapsulation |
| **44.6** | Database: Contact Book with SQLite | SQL, CRUD, transactions |
| **44.7** | Async: Concurrent Downloader | `asyncio`, concurrency, timing |
| **44.8** | Capstone: Packaged CLI Tool with Tests | packaging, testing, documentation, publishing |

### 45. Appendix

| # | Topic | Covers |
|:--|:------|:-------|
| **45.1** | Complete Built-in Functions Reference | every built-in, with a one-line description |
| **45.2** | Complete Keyword Reference | every keyword, with a one-line description |
| **45.3** | Dunder Method Cheat Sheet | every dunder, grouped by purpose |
| **45.4** | Exception Hierarchy Chart | the full tree, as a diagram |
| **45.5** | Glossary | every term in this course, defined |
| **45.6** | Further Resources | books, docs, and where to go next |


---

## Code Style in This Repo

- Clean and readable over clever. If a loop is clearer than a comprehension, it's a loop.
- A comment above every meaningful line, explaining intent — not restating syntax.
- Descriptive names. No `x`, `tmp`, or `data2`.
- Small examples that each demonstrate one idea.
- Output is printed with labels so you can match each line to the code that produced it.
- One concept per notebook cell, with the explanation in the markdown cell directly above it.
- Notebooks are committed without saved output, so every run is genuinely yours.
