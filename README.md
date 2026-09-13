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

| ✅ | Ch | Chapter | Status |
|----|----|---------|--------|
| ⬜ | 01 | Introduction to Programming | In progress |
| ⬜ | 02 | Setup and First Program | Not started |
| ⬜ | 03 | Syntax Fundamentals | Not started |
| ⬜ | 04 | Variables and Memory Model | Not started |
| ⬜ | 05 | Data Types — Numbers and Booleans | Not started |
| ⬜ | 06 | Operators | Not started |
| ⬜ | 07 | Strings | Not started |
| ⬜ | 08 | Input, Output, and Basic I/O | Not started |
| ⬜ | 09 | Control Flow — Conditionals | Not started |
| ⬜ | 10 | Control Flow — Loops | Not started |
| ⬜ | 11 | Lists | Not started |
| ⬜ | 12 | Tuples | Not started |
| ⬜ | 13 | Sets and Frozensets | Not started |
| ⬜ | 14 | Dictionaries | Not started |
| ⬜ | 15 | Comprehensions | Not started |
| ⬜ | 16 | Functions — Fundamentals | Not started |
| ⬜ | 17 | Functions — Scope and Advanced | Not started |
| ⬜ | 18 | Decorators | Not started |
| ⬜ | 19 | Iterators and Generators | Not started |
| ⬜ | 20 | Modules and Packages | Not started |
| ⬜ | 21 | Standard Library Tour | Not started |
| ⬜ | 22 | File Handling | Not started |
| ⬜ | 23 | Error Handling and Exceptions | Not started |
| ⬜ | 24 | OOP — Fundamentals | Not started |
| ⬜ | 25 | OOP — Encapsulation and Properties | Not started |
| ⬜ | 26 | OOP — Inheritance and Polymorphism | Not started |
| ⬜ | 27 | OOP — Magic Methods | Not started |
| ⬜ | 28 | OOP — Advanced | Not started |
| ⬜ | 29 | Context Managers | Not started |
| ⬜ | 30 | Regular Expressions | Not started |
| ⬜ | 31 | Functional Programming | Not started |
| ⬜ | 32 | Type Hints and Static Typing | Not started |
| ⬜ | 33 | Concurrency — Threading | Not started |
| ⬜ | 34 | Concurrency — Multiprocessing | Not started |
| ⬜ | 35 | Asynchronous Programming | Not started |
| ⬜ | 36 | Testing | Not started |
| ⬜ | 37 | Debugging, Logging, Profiling | Not started |
| ⬜ | 38 | Working with Data Formats and APIs | Not started |
| ⬜ | 39 | Databases | Not started |
| ⬜ | 40 | Project Structure and Packaging | Not started |
| ⬜ | 41 | Code Quality and Tooling | Not started |
| ⬜ | 42 | Security Basics | Not started |
| ⬜ | 43 | Advanced Internals | Not started |
| ⬜ | 44 | Projects | Not started |
| ⬜ | 45 | Appendix | Not started |

---

## Full Syllabus

### 01. Introduction to Programming

| # | Subchapter |
|---|------------|
| 01.1 | What is Programming (theory) |
| 01.2 | How Computers Execute Code (CPU, memory, binary, machine code) |
| 01.3 | Algorithms and Pseudocode |
| 01.4 | Compiled vs Interpreted Languages |
| 01.5 | Programming Paradigms Overview (procedural, OOP, functional) |
| 01.6 | What is Python (history, philosophy, Zen of Python, versions) |
| 01.7 | Where Python is Used (domains) |
| 01.8 | CPython vs PyPy vs Other Implementations |


### 02. Setup and First Program

| # | Subchapter |
|---|------------|
| 02.1 | Installing Python (Windows/macOS/Linux) |
| 02.2 | Python Interpreter and REPL |
| 02.3 | Editors and IDEs (VS Code setup) |
| 02.4 | Writing and Running First Script |
| 02.5 | Virtual Environments Intro (`venv`) |
| 02.6 | `pip` Basics |
| 02.7 | Anatomy of a Python File (shebang, encoding, `__main__`) |


### 03. Syntax Fundamentals

| # | Subchapter |
|---|------------|
| 03.1 | Statements and Expressions |
| 03.2 | Indentation Rules and Blocks |
| 03.3 | Comments (single, multi-line, docstrings) |
| 03.4 | Line Continuation |
| 03.5 | Keywords and Identifiers |
| 03.6 | PEP 8 Introduction |
| 03.7 | Common Beginner Syntax Errors |


### 04. Variables and Memory Model

| # | Subchapter |
|---|------------|
| 04.1 | Variables and Assignment |
| 04.2 | Names, Objects, References (theory) |
| 04.3 | `id()`, `type()`, and Object Identity |
| 04.4 | Mutable vs Immutable Objects |
| 04.5 | Reference Semantics and Aliasing |
| 04.6 | Garbage Collection and Reference Counting |
| 04.7 | Constants and Naming Conventions |
| 04.8 | Multiple Assignment and Swapping |


### 05. Data Types — Numbers and Booleans

| # | Subchapter |
|---|------------|
| 05.1 | Integers (arbitrary precision, bases) |
| 05.2 | Floats (IEEE 754, precision pitfalls) |
| 05.3 | Complex Numbers |
| 05.4 | `Decimal` and `Fraction` |
| 05.5 | Booleans and Truthiness |
| 05.6 | `None` Type |
| 05.7 | Type Conversion / Casting |
| 05.8 | `math` Module Essentials |


### 06. Operators

| # | Subchapter |
|---|------------|
| 06.1 | Arithmetic Operators |
| 06.2 | Comparison Operators and Chaining |
| 06.3 | Logical Operators and Short-Circuiting |
| 06.4 | Assignment and Augmented Assignment |
| 06.5 | Bitwise Operators |
| 06.6 | Identity Operators (`is`, `is not`) |
| 06.7 | Membership Operators (`in`, `not in`) |
| 06.8 | Operator Precedence and Associativity |
| 06.9 | Walrus Operator (`:=`) |


### 07. Strings

| # | Subchapter |
|---|------------|
| 07.1 | String Literals and Quoting |
| 07.2 | Indexing and Slicing |
| 07.3 | String Immutability |
| 07.4 | String Methods (complete tour) |
| 07.5 | Formatting: f-strings |
| 07.6 | Formatting: `.format()` and `%` |
| 07.7 | Format Spec Mini-Language |
| 07.8 | Escape Sequences and Raw Strings |
| 07.9 | Unicode, Encoding, `bytes` vs `str` |
| 07.10 | String Concatenation Performance (`join`) |
| 07.11 | `textwrap` and the `string` Module |


### 08. Input, Output, and Basic I/O

| # | Subchapter |
|---|------------|
| 08.1 | `print()` in Depth (sep, end, file, flush) |
| 08.2 | `input()` and Parsing User Input |
| 08.3 | Command-Line Arguments (`sys.argv`) |
| 08.4 | Formatted Console Output |


### 09. Control Flow — Conditionals

| # | Subchapter |
|---|------------|
| 09.1 | `if` / `elif` / `else` |
| 09.2 | Nested Conditionals |
| 09.3 | Conditional (Ternary) Expressions |
| 09.4 | `match` Statement — Structural Pattern Matching |
| 09.5 | Guard Clauses and Readable Conditions |


### 10. Control Flow — Loops

| # | Subchapter |
|---|------------|
| 10.1 | `while` Loops |
| 10.2 | `for` Loops and Iterables |
| 10.3 | `range()` in Depth |
| 10.4 | `break`, `continue`, `pass` |
| 10.5 | `else` Clause on Loops |
| 10.6 | Nested Loops |
| 10.7 | `enumerate()` and `zip()` |
| 10.8 | Infinite Loops and Loop Safety |
| 10.9 | Loop Performance Notes |


### 11. Lists

| # | Subchapter |
|---|------------|
| 11.1 | Creating and Accessing Lists |
| 11.2 | Slicing (including step and negative indices) |
| 11.3 | List Methods (complete) |
| 11.4 | Mutability and In-Place Operations |
| 11.5 | Sorting (`sort` vs `sorted`, `key`, `reverse`) |
| 11.6 | Nested Lists and Matrices |
| 11.7 | Copying: Shallow vs Deep (`copy` module) |
| 11.8 | Lists as Stacks and Queues |
| 11.9 | Common List Pitfalls (mutable default, `*` copy) |


### 12. Tuples

| # | Subchapter |
|---|------------|
| 12.1 | Creating Tuples and the Single-Element Trap |
| 12.2 | Immutability and When to Use Tuples |
| 12.3 | Tuple Methods and Operations |
| 12.4 | Packing and Unpacking |
| 12.5 | Extended Unpacking (`*rest`) |
| 12.6 | Tuples as Dictionary Keys |
| 12.7 | `namedtuple` Preview |


### 13. Sets and Frozensets

| # | Subchapter |
|---|------------|
| 13.1 | Creating Sets, Uniqueness |
| 13.2 | Set Methods |
| 13.3 | Set Operations (union, intersection, difference, symmetric difference) |
| 13.4 | Subset / Superset / Disjoint |
| 13.5 | `frozenset` |
| 13.6 | The Hashability Requirement |
| 13.7 | Performance: Set vs List Lookup |


### 14. Dictionaries

| # | Subchapter |
|---|------------|
| 14.1 | Creating and Accessing Dictionaries |
| 14.2 | Dictionary Methods (complete) |
| 14.3 | Keys, Values, and Items Views |
| 14.4 | Iterating Dictionaries |
| 14.5 | Nested Dictionaries |
| 14.6 | `get`, `setdefault`, `pop`, and Missing Keys |
| 14.7 | Merging Dicts (`|`, `update`, `**`) |
| 14.8 | Dict Ordering Guarantees |
| 14.9 | Hashing and Key Requirements |
| 14.10 | Dict Performance |


### 15. Comprehensions

| # | Subchapter |
|---|------------|
| 15.1 | List Comprehensions |
| 15.2 | Conditional Comprehensions |
| 15.3 | Nested Comprehensions |
| 15.4 | Dict Comprehensions |
| 15.5 | Set Comprehensions |
| 15.6 | Generator Expressions |
| 15.7 | Readability Limits — When Not to Use Them |


### 16. Functions — Fundamentals

| # | Subchapter |
|---|------------|
| 16.1 | Defining and Calling Functions |
| 16.2 | Positional Arguments |
| 16.3 | Keyword Arguments |
| 16.4 | Default Parameters and the Mutable Default Trap |
| 16.5 | `*args` and `**kwargs` |
| 16.6 | Positional-Only (`/`) and Keyword-Only (`*`) Parameters |
| 16.7 | Return Values and Multiple Returns |
| 16.8 | Docstrings (PEP 257) |
| 16.9 | Functions as First-Class Objects |


### 17. Functions — Scope and Advanced

| # | Subchapter |
|---|------------|
| 17.1 | Scope and the LEGB Rule |
| 17.2 | `global` and `nonlocal` |
| 17.3 | Closures |
| 17.4 | Lambda Functions |
| 17.5 | Recursion and Recursion Limits |
| 17.6 | Higher-Order Functions (`map`, `filter`, `reduce`) |
| 17.7 | `functools` (`partial`, `lru_cache`, `wraps`, `reduce`) |
| 17.8 | Pure Functions and Side Effects |
| 17.9 | Function Annotations / Type Hints |


### 18. Decorators

| # | Subchapter |
|---|------------|
| 18.1 | Decorator Theory |
| 18.2 | Writing Simple Decorators |
| 18.3 | Decorators with Arguments |
| 18.4 | `functools.wraps` |
| 18.5 | Stacking Decorators |
| 18.6 | Class Decorators |
| 18.7 | Practical Decorators (timing, retry, logging, caching) |


### 19. Iterators and Generators

| # | Subchapter |
|---|------------|
| 19.1 | Iterable vs Iterator Protocol |
| 19.2 | `iter()` and `next()` |
| 19.3 | Building Custom Iterators |
| 19.4 | Generators and `yield` |
| 19.5 | Generator Expressions |
| 19.6 | `yield from` |
| 19.7 | Sending Values into Generators (`send`, `throw`, `close`) |
| 19.8 | Lazy Evaluation and Memory Benefits |
| 19.9 | `itertools` Complete Tour |


### 20. Modules and Packages

| # | Subchapter |
|---|------------|
| 20.1 | What is a Module |
| 20.2 | `import` Forms and Aliasing |
| 20.3 | Module Search Path (`sys.path`) |
| 20.4 | `if __name__ == "__main__"` |
| 20.5 | Creating Packages and `__init__.py` |
| 20.6 | Relative vs Absolute Imports |
| 20.7 | Namespace Packages |
| 20.8 | Circular Imports and How to Avoid Them |
| 20.9 | Reloading Modules |
| 20.10 | `__all__` and the Public API |


### 21. Standard Library Tour

| # | Subchapter |
|---|------------|
| 21.1 | `os` and `sys` |
| 21.2 | `pathlib` |
| 21.3 | `datetime`, `time`, `zoneinfo` |
| 21.4 | `random` and `secrets` |
| 21.5 | `collections` (`Counter`, `defaultdict`, `deque`, `OrderedDict`, `namedtuple`, `ChainMap`) |
| 21.6 | `json`, `csv`, `pickle` |
| 21.7 | `re` Preview |
| 21.8 | `argparse` |
| 21.9 | `logging` |
| 21.10 | `subprocess` |
| 21.11 | `shutil`, `glob`, `tempfile` |
| 21.12 | `statistics`, `enum`, `uuid`, `hashlib` |


### 22. File Handling

| # | Subchapter |
|---|------------|
| 22.1 | Opening and Closing Files, File Modes |
| 22.2 | Reading Files (`read`, `readline`, `readlines`, iteration) |
| 22.3 | Writing and Appending |
| 22.4 | Context Managers (`with`) |
| 22.5 | Binary Files |
| 22.6 | Encodings and `newline` |
| 22.7 | File Positions (`seek`, `tell`) |
| 22.8 | `os` and `pathlib` File Operations |
| 22.9 | Working with CSV |
| 22.10 | Working with JSON |
| 22.11 | Serialization: `pickle` |
| 22.12 | Temporary Files and Directories |


### 23. Error Handling and Exceptions

| # | Subchapter |
|---|------------|
| 23.1 | Errors vs Exceptions (theory) |
| 23.2 | The Exception Hierarchy |
| 23.3 | `try` / `except` |
| 23.4 | Multiple and Grouped Excepts |
| 23.5 | `else` and `finally` |
| 23.6 | `raise` and Re-Raising |
| 23.7 | Exception Chaining (`from`) |
| 23.8 | Custom Exception Classes |
| 23.9 | `assert` and Assertions |
| 23.10 | Exception Groups and `except*` |
| 23.11 | EAFP vs LBYL |
| 23.12 | Best Practices and Anti-Patterns |


### 24. OOP — Fundamentals

| # | Subchapter |
|---|------------|
| 24.1 | OOP Theory (objects, classes, abstraction) |
| 24.2 | Defining Classes, Creating Instances |
| 24.3 | Instance Attributes and `self` |
| 24.4 | The `__init__` Constructor |
| 24.5 | Class Attributes vs Instance Attributes |
| 24.6 | Instance Methods |
| 24.7 | Class Methods and `@classmethod` |
| 24.8 | Static Methods and `@staticmethod` |
| 24.9 | `__del__` and Object Lifecycle |


### 25. OOP — Encapsulation and Properties

| # | Subchapter |
|---|------------|
| 25.1 | Public, Protected, and Private Conventions |
| 25.2 | Name Mangling |
| 25.3 | Getters and Setters |
| 25.4 | The `@property` Decorator |
| 25.5 | Computed Attributes |
| 25.6 | `__slots__` |


### 26. OOP — Inheritance and Polymorphism

| # | Subchapter |
|---|------------|
| 26.1 | Single Inheritance |
| 26.2 | `super()` in Depth |
| 26.3 | Method Overriding |
| 26.4 | Multiple Inheritance |
| 26.5 | Method Resolution Order (MRO) and C3 Linearization |
| 26.6 | Mixins |
| 26.7 | Polymorphism and Duck Typing |
| 26.8 | `isinstance` vs `type` vs Duck Typing |
| 26.9 | Composition vs Inheritance |


### 27. OOP — Magic Methods

| # | Subchapter |
|---|------------|
| 27.1 | `__str__` vs `__repr__` |
| 27.2 | Comparison Dunders (`__eq__`, `__lt__`, …) |
| 27.3 | `__hash__` and the Hashability Contract |
| 27.4 | Arithmetic Operator Overloading |
| 27.5 | Container Dunders (`__len__`, `__getitem__`, `__contains__`, `__iter__`) |
| 27.6 | Callable Objects (`__call__`) |
| 27.7 | Attribute Access (`__getattr__`, `__setattr__`, `__getattribute__`) |
| 27.8 | The Context Manager Protocol (`__enter__`, `__exit__`) |
| 27.9 | `__new__` vs `__init__` |
| 27.10 | Complete Dunder Reference |


### 28. OOP — Advanced

| # | Subchapter |
|---|------------|
| 28.1 | Abstract Base Classes (`abc`) |
| 28.2 | Protocols and Structural Typing |
| 28.3 | `dataclasses` Complete |
| 28.4 | `enum` Complete |
| 28.5 | `NamedTuple` and `TypedDict` |
| 28.6 | Descriptors |
| 28.7 | Metaclasses |
| 28.8 | Class Creation Hooks (`__init_subclass__`, `__set_name__`) |
| 28.9 | Design Patterns in Python (singleton, factory, observer, strategy) |
| 28.10 | SOLID Principles in Python |


### 29. Context Managers

| # | Subchapter |
|---|------------|
| 29.1 | `with` Statement Theory |
| 29.2 | Class-Based Context Managers |
| 29.3 | `contextlib.contextmanager` |
| 29.4 | `contextlib` Utilities (`suppress`, `closing`, `ExitStack`) |
| 29.5 | Multiple Context Managers |
| 29.6 | Async Context Managers Preview |


### 30. Regular Expressions

| # | Subchapter |
|---|------------|
| 30.1 | Regex Theory and Syntax |
| 30.2 | Character Classes and Quantifiers |
| 30.3 | Anchors and Boundaries |
| 30.4 | Groups and Capturing |
| 30.5 | Named Groups, Lookahead, Lookbehind |
| 30.6 | `re` Module Functions |
| 30.7 | Flags |
| 30.8 | Substitution and Splitting |
| 30.9 | Greedy vs Lazy, Catastrophic Backtracking |
| 30.10 | Practical Patterns |


### 31. Functional Programming

| # | Subchapter |
|---|------------|
| 31.1 | Functional Concepts in Python |
| 31.2 | Immutability Practices |
| 31.3 | `map`, `filter`, `reduce` Deep Dive |
| 31.4 | Function Composition |
| 31.5 | Currying and Partial Application |
| 31.6 | The `operator` Module |
| 31.7 | Limits of FP in Python |


### 32. Type Hints and Static Typing

| # | Subchapter |
|---|------------|
| 32.1 | Why Type Hints |
| 32.2 | Basic Annotations |
| 32.3 | `typing` Module Core (`Optional`, `Union`, `Any`, `Literal`) |
| 32.4 | Generics and `TypeVar` |
| 32.5 | Modern Syntax (`list[int]`, `X | Y`) |
| 32.6 | `Callable`, `Protocol`, `Self` |
| 32.7 | Using `mypy` |
| 32.8 | Runtime Type Checking and Its Limits |


### 33. Concurrency — Threading

| # | Subchapter |
|---|------------|
| 33.1 | Concurrency vs Parallelism (theory) |
| 33.2 | Processes vs Threads |
| 33.3 | The GIL Explained |
| 33.4 | The `threading` Module |
| 33.5 | Locks, RLocks, Semaphores, Events |
| 33.6 | Race Conditions and Deadlocks |
| 33.7 | `queue` for Thread Communication |
| 33.8 | `concurrent.futures.ThreadPoolExecutor` |


### 34. Concurrency — Multiprocessing

| # | Subchapter |
|---|------------|
| 34.1 | The `multiprocessing` Module |
| 34.2 | Process Pools |
| 34.3 | Inter-Process Communication (Pipes, Queues) |
| 34.4 | Shared Memory |
| 34.5 | `ProcessPoolExecutor` |
| 34.6 | Choosing Threads vs Processes vs Async |


### 35. Asynchronous Programming

| # | Subchapter |
|---|------------|
| 35.1 | Async Theory and the Event Loop |
| 35.2 | `async` / `await` Syntax |
| 35.3 | Coroutines and Tasks |
| 35.4 | `asyncio.gather`, `wait`, `TaskGroup` |
| 35.5 | Async Iterators and Generators |
| 35.6 | Async Context Managers |
| 35.7 | Timeouts and Cancellation |
| 35.8 | Mixing Sync and Async Code |
| 35.9 | Practical Async I/O |


### 36. Testing

| # | Subchapter |
|---|------------|
| 36.1 | Why Test — Theory and Test Types |
| 36.2 | `unittest` Basics |
| 36.3 | Assertions and Test Fixtures |
| 36.4 | `pytest` Basics |
| 36.5 | `pytest` Fixtures |
| 36.6 | Parametrized Tests |
| 36.7 | Mocking (`unittest.mock`, `monkeypatch`) |
| 36.8 | Test Coverage |
| 36.9 | `doctest` |
| 36.10 | The TDD Workflow |


### 37. Debugging, Logging, Profiling

| # | Subchapter |
|---|------------|
| 37.1 | Reading Tracebacks |
| 37.2 | Debugging with `print` vs a Debugger |
| 37.3 | `pdb` / `breakpoint()` |
| 37.4 | The VS Code Debugger |
| 37.5 | `logging` Deep Dive (levels, handlers, formatters, config) |
| 37.6 | Profiling (`timeit`, `cProfile`, memory) |
| 37.7 | Optimization Strategies |
| 37.8 | Big-O Basics for Python Data Structures |


### 38. Working with Data Formats and APIs

| # | Subchapter |
|---|------------|
| 38.1 | JSON Deep Dive |
| 38.2 | CSV Deep Dive |
| 38.3 | XML and YAML |
| 38.4 | HTTP Basics |
| 38.5 | `urllib` and `requests` |
| 38.6 | Consuming REST APIs |
| 38.7 | Web Scraping Basics (`BeautifulSoup`) and Ethics |


### 39. Databases

| # | Subchapter |
|---|------------|
| 39.1 | Database Theory and SQL Refresher |
| 39.2 | The `sqlite3` Module |
| 39.3 | CRUD Operations |
| 39.4 | Parameterized Queries and SQL Injection |
| 39.5 | Transactions |
| 39.6 | ORM Introduction (SQLAlchemy basics) |


### 40. Project Structure and Packaging

| # | Subchapter |
|---|------------|
| 40.1 | Project Layout Conventions (`src` layout) |
| 40.2 | `requirements.txt` vs `pyproject.toml` |
| 40.3 | Dependency Management Tools (`pip-tools`, `poetry`, `uv`) |
| 40.4 | Building a Distributable Package |
| 40.5 | Publishing to PyPI |
| 40.6 | Entry Points and CLI Tools |
| 40.7 | Semantic Versioning |


### 41. Code Quality and Tooling

| # | Subchapter |
|---|------------|
| 41.1 | PEP 8 Deep Dive |
| 41.2 | Linters (`ruff`, `flake8`, `pylint`) |
| 41.3 | Formatters (`black`, `ruff format`) |
| 41.4 | Pre-commit Hooks |
| 41.5 | Docstring Standards and `sphinx` / `mkdocs` |
| 41.6 | Code Smells and Refactoring |
| 41.7 | Clean Code Principles |


### 42. Security Basics

| # | Subchapter |
|---|------------|
| 42.1 | Input Validation |
| 42.2 | Secrets Management (`.env`, environment variables) |
| 42.3 | Hashing and Passwords |
| 42.4 | Common Python Vulnerabilities (`eval`, `pickle`, path traversal) |
| 42.5 | Dependency Security |


### 43. Advanced Internals

| # | Subchapter |
|---|------------|
| 43.1 | Bytecode and `dis` |
| 43.2 | Memory Management Deep Dive |
| 43.3 | The `gc` Module and Circular References |
| 43.4 | `weakref` |
| 43.5 | Interning and the Small Integer Cache |
| 43.6 | `sys` Internals |
| 43.7 | C Extensions and `ctypes` Introduction |


### 44. Projects

| # | Subchapter |
|---|------------|
| 44.1 | Beginner: CLI Calculator / Number Game |
| 44.2 | Beginner: Text File Word Counter |
| 44.3 | Intermediate: To-Do CLI with JSON Storage |
| 44.4 | Intermediate: API Data Fetcher |
| 44.5 | OOP: Bank / Library Management System |
| 44.6 | Database: Contact Book with SQLite |
| 44.7 | Async: Concurrent Downloader |
| 44.8 | Capstone: Packaged CLI Tool with Tests |


### 45. Appendix

| # | Subchapter |
|---|------------|
| 45.1 | Complete Built-in Functions Reference |
| 45.2 | Complete Keyword Reference |
| 45.3 | Dunder Method Cheat Sheet |
| 45.4 | Exception Hierarchy Chart |
| 45.5 | Glossary |
| 45.6 | Further Resources |


---

## Code Style in This Repo

- Clean and readable over clever. If a loop is clearer than a comprehension, it's a loop.
- A comment above every meaningful line, explaining intent — not restating syntax.
- Descriptive names. No `x`, `tmp`, or `data2`.
- Small examples that each demonstrate one idea.
- Output is printed with labels so you can match each line to the code that produced it.
- One concept per notebook cell, with the explanation in the markdown cell directly above it.
- Notebooks are committed without saved output, so every run is genuinely yours.
