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

<table width="100%">
<tr>
<th align="center" width="5%">✅</th>
<th align="center" width="5%">Ch</th>
<th align="left" width="24%">Chapter</th>
<th align="left" width="44%">What You'll Learn</th>
<th align="center" width="7%">Topics</th>
<th align="left" width="15%">Status</th>
</tr>
<tr><td align="center">⬜</td><td align="center"><b>01</b></td><td align="left">Introduction to Programming</td><td align="left">Think like a programmer before writing any code</td><td align="center">8</td><td align="left">In progress</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>02</b></td><td align="left">Setup and First Program</td><td align="left">Get Python installed and run your first script</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>03</b></td><td align="left">Syntax Fundamentals</td><td align="left">Read and write correctly formed Python</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>04</b></td><td align="left">Variables and Memory Model</td><td align="left">Understand what a variable really is</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>05</b></td><td align="left">Data Types — Numbers and Booleans</td><td align="left">Work with every kind of number Python offers</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>06</b></td><td align="left">Operators</td><td align="left">Combine and compare values correctly</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>07</b></td><td align="left">Strings</td><td align="left">Handle text confidently, including Unicode</td><td align="center">11</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>08</b></td><td align="left">Input, Output, and Basic I/O</td><td align="left">Talk to the user and the command line</td><td align="center">4</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>09</b></td><td align="left">Control Flow — Conditionals</td><td align="left">Make your programs take decisions</td><td align="center">5</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>10</b></td><td align="left">Control Flow — Loops</td><td align="left">Repeat work without repeating yourself</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>11</b></td><td align="left">Lists</td><td align="left">Store ordered, changeable collections</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>12</b></td><td align="left">Tuples</td><td align="left">Store fixed records that cannot change</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>13</b></td><td align="left">Sets and Frozensets</td><td align="left">Handle uniqueness and fast membership tests</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>14</b></td><td align="left">Dictionaries</td><td align="left">Look data up instantly by key</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>15</b></td><td align="left">Comprehensions</td><td align="left">Build collections in one readable line</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>16</b></td><td align="left">Functions — Fundamentals</td><td align="left">Package logic into reusable functions</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>17</b></td><td align="left">Functions — Scope and Advanced</td><td align="left">Master scope, closures and higher-order functions</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>18</b></td><td align="left">Decorators</td><td align="left">Add behaviour to functions without editing them</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>19</b></td><td align="left">Iterators and Generators</td><td align="left">Process data too large to fit in memory</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>20</b></td><td align="left">Modules and Packages</td><td align="left">Split a program across many files</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>21</b></td><td align="left">Standard Library Tour</td><td align="left">Solve common problems with zero installs</td><td align="center">12</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>22</b></td><td align="left">File Handling</td><td align="left">Read and write files of every kind</td><td align="center">12</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>23</b></td><td align="left">Error Handling and Exceptions</td><td align="left">Handle failure without crashing</td><td align="center">12</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>24</b></td><td align="left">OOP — Fundamentals</td><td align="left">Model your problem domain with classes</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>25</b></td><td align="left">OOP — Encapsulation and Properties</td><td align="left">Control access to an object's internals</td><td align="center">6</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>26</b></td><td align="left">OOP — Inheritance and Polymorphism</td><td align="left">Share and specialise behaviour between classes</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>27</b></td><td align="left">OOP — Magic Methods</td><td align="left">Make your objects work with Python's syntax</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>28</b></td><td align="left">OOP — Advanced</td><td align="left">Use the modern tools that cut boilerplate</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>29</b></td><td align="left">Context Managers</td><td align="left">Manage resources that must be cleaned up</td><td align="center">6</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>30</b></td><td align="left">Regular Expressions</td><td align="left">Search and transform text by pattern</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>31</b></td><td align="left">Functional Programming</td><td align="left">Write predictable, side-effect-free code</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>32</b></td><td align="left">Type Hints and Static Typing</td><td align="left">Catch type bugs before running the code</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>33</b></td><td align="left">Concurrency — Threading</td><td align="left">Run work concurrently, and know the GIL's limits</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>34</b></td><td align="left">Concurrency — Multiprocessing</td><td align="left">Use every CPU core for heavy work</td><td align="center">6</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>35</b></td><td align="left">Asynchronous Programming</td><td align="left">Handle thousands of I/O operations at once</td><td align="center">9</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>36</b></td><td align="left">Testing</td><td align="left">Prove your code works, and keep it working</td><td align="center">10</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>37</b></td><td align="left">Debugging, Logging, Profiling</td><td align="left">Find bugs and bottlenecks systematically</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>38</b></td><td align="left">Working with Data Formats and APIs</td><td align="left">Exchange data with files and web services</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>39</b></td><td align="left">Databases</td><td align="left">Store data that outlives your program</td><td align="center">6</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>40</b></td><td align="left">Project Structure and Packaging</td><td align="left">Turn your code into an installable package</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>41</b></td><td align="left">Code Quality and Tooling</td><td align="left">Write code a team can maintain</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>42</b></td><td align="left">Security Basics</td><td align="left">Avoid the mistakes that cause breaches</td><td align="center">5</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>43</b></td><td align="left">Advanced Internals</td><td align="left">Understand what Python does under the hood</td><td align="center">7</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>44</b></td><td align="left">Projects</td><td align="left">Apply everything to real, complete programs</td><td align="center">8</td><td align="left">Not started</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>45</b></td><td align="left">Appendix</td><td align="left">Look things up fast when you need them</td><td align="center">6</td><td align="left">Not started</td></tr>
</table>

---

## Full Syllabus

### 01. Introduction to Programming

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>01.1</b></td><td>What is Programming</td><td>instructions, precision, program vs process</td></tr>
<tr><td><b>01.2</b></td><td>How Computers Execute Code</td><td>CPU, memory, binary, machine code</td></tr>
<tr><td><b>01.3</b></td><td>Algorithms and Pseudocode</td><td>steps, decomposition, the three building blocks</td></tr>
<tr><td><b>01.4</b></td><td>Compiled vs Interpreted Languages</td><td>bytecode, the PVM, <code>__pycache__</code></td></tr>
<tr><td><b>01.5</b></td><td>Programming Paradigms Overview</td><td>procedural, OOP, functional</td></tr>
<tr><td><b>01.6</b></td><td>What is Python</td><td>history, philosophy, Zen of Python, versions</td></tr>
<tr><td><b>01.7</b></td><td>Where Python is Used</td><td>the domains it leads, and where it is the wrong tool</td></tr>
<tr><td><b>01.8</b></td><td>CPython vs PyPy vs Other Implementations</td><td>the reference implementation, JIT, the GIL</td></tr>
</table>

### 02. Setup and First Program

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>02.1</b></td><td>Installing Python</td><td>Windows/macOS/Linux</td></tr>
<tr><td><b>02.2</b></td><td>Python Interpreter and REPL</td><td>interactive mode, <code>help()</code>, <code>dir()</code></td></tr>
<tr><td><b>02.3</b></td><td>Editors and IDEs</td><td>VS Code setup</td></tr>
<tr><td><b>02.4</b></td><td>Writing and Running First Script</td><td>your first file, running it from a terminal</td></tr>
<tr><td><b>02.5</b></td><td>Virtual Environments Intro</td><td><code>venv</code></td></tr>
<tr><td><b>02.6</b></td><td><code>pip</code> Basics</td><td>installing, upgrading, freezing, uninstalling</td></tr>
<tr><td><b>02.7</b></td><td>Anatomy of a Python File</td><td>shebang, encoding, <code>__main__</code></td></tr>
</table>

### 03. Syntax Fundamentals

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>03.1</b></td><td>Statements and Expressions</td><td>what evaluates to a value, and what does not</td></tr>
<tr><td><b>03.2</b></td><td>Indentation Rules and Blocks</td><td>whitespace as syntax, nesting, <code>IndentationError</code></td></tr>
<tr><td><b>03.3</b></td><td>Comments</td><td>single, multi-line, docstrings</td></tr>
<tr><td><b>03.4</b></td><td>Line Continuation</td><td>implicit vs explicit, backslashes, brackets</td></tr>
<tr><td><b>03.5</b></td><td>Keywords and Identifiers</td><td>reserved words, valid names, naming rules</td></tr>
<tr><td><b>03.6</b></td><td>PEP 8 Introduction</td><td>the style guide every Python project follows</td></tr>
<tr><td><b>03.7</b></td><td>Common Beginner Syntax Errors</td><td>reading and fixing the errors beginners hit most</td></tr>
</table>

### 04. Variables and Memory Model

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>04.1</b></td><td>Variables and Assignment</td><td>binding a name to a value</td></tr>
<tr><td><b>04.2</b></td><td>Names, Objects, References</td><td>why a variable is a label, not a box</td></tr>
<tr><td><b>04.3</b></td><td><code>id()</code>, <code>type()</code>, and Object Identity</td><td>what an object actually is, and how to inspect one</td></tr>
<tr><td><b>04.4</b></td><td>Mutable vs Immutable Objects</td><td>which types can change in place, and which cannot</td></tr>
<tr><td><b>04.5</b></td><td>Reference Semantics and Aliasing</td><td>why two names can point at one object</td></tr>
<tr><td><b>04.6</b></td><td>Garbage Collection and Reference Counting</td><td>how Python frees memory you stopped using</td></tr>
<tr><td><b>04.7</b></td><td>Constants and Naming Conventions</td><td><code>UPPER_CASE</code>, <code>snake_case</code>, <code>_private</code></td></tr>
<tr><td><b>04.8</b></td><td>Multiple Assignment and Swapping</td><td><code>a, b = 1, 2</code> and <code>a, b = b, a</code></td></tr>
</table>

### 05. Data Types — Numbers and Booleans

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>05.1</b></td><td>Integers</td><td>arbitrary precision, bases</td></tr>
<tr><td><b>05.2</b></td><td>Floats</td><td>IEEE 754, precision pitfalls</td></tr>
<tr><td><b>05.3</b></td><td>Complex Numbers</td><td>real and imaginary parts, <code>j</code> notation</td></tr>
<tr><td><b>05.4</b></td><td><code>Decimal</code> and <code>Fraction</code></td><td>exact arithmetic when floats will not do</td></tr>
<tr><td><b>05.5</b></td><td>Booleans and Truthiness</td><td>what counts as <code>True</code>, what counts as <code>False</code></td></tr>
<tr><td><b>05.6</b></td><td><code>None</code> Type</td><td>absence of a value, and why it is not zero</td></tr>
<tr><td><b>05.7</b></td><td>Type Conversion / Casting</td><td><code>int()</code>, <code>float()</code>, <code>str()</code>, <code>bool()</code></td></tr>
<tr><td><b>05.8</b></td><td><code>math</code> Module Essentials</td><td>rounding, roots, logs, constants</td></tr>
</table>

### 06. Operators

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>06.1</b></td><td>Arithmetic Operators</td><td><code>+  -  *  /  //  %  **</code></td></tr>
<tr><td><b>06.2</b></td><td>Comparison Operators and Chaining</td><td><code>==  !=  &lt;  &gt;  &lt;=  &gt;=</code> and <code>a &lt; b &lt; c</code></td></tr>
<tr><td><b>06.3</b></td><td>Logical Operators and Short-Circuiting</td><td><code>and</code>, <code>or</code>, <code>not</code>, and lazy evaluation</td></tr>
<tr><td><b>06.4</b></td><td>Assignment and Augmented Assignment</td><td><code>=</code>, <code>+=</code>, <code>-=</code>, <code>*=</code> and friends</td></tr>
<tr><td><b>06.5</b></td><td>Bitwise Operators</td><td><code>&amp;</code>, <code>|</code>, <code>^</code>, <code>~</code>, <code>&lt;&lt;</code>, <code>&gt;&gt;</code></td></tr>
<tr><td><b>06.6</b></td><td>Identity Operators</td><td><code>is</code>, <code>is not</code></td></tr>
<tr><td><b>06.7</b></td><td>Membership Operators</td><td><code>in</code>, <code>not in</code></td></tr>
<tr><td><b>06.8</b></td><td>Operator Precedence and Associativity</td><td>what binds tightest, and when to add brackets</td></tr>
<tr><td><b>06.9</b></td><td>Walrus Operator</td><td><code>:=</code></td></tr>
</table>

### 07. Strings

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>07.1</b></td><td>String Literals and Quoting</td><td>single, double, triple quotes</td></tr>
<tr><td><b>07.2</b></td><td>Indexing and Slicing</td><td><code>[i]</code>, <code>[a:b]</code>, <code>[a:b:step]</code>, negative indices</td></tr>
<tr><td><b>07.3</b></td><td>String Immutability</td><td>why strings cannot be changed in place</td></tr>
<tr><td><b>07.4</b></td><td>String Methods</td><td>complete tour</td></tr>
<tr><td><b>07.5</b></td><td>Formatting: f-strings</td><td>the modern way to build strings</td></tr>
<tr><td><b>07.6</b></td><td>Formatting: <code>.format()</code> and <code>%</code></td><td>the older styles, and where you still meet them</td></tr>
<tr><td><b>07.7</b></td><td>Format Spec Mini-Language</td><td>padding, alignment, precision, thousands separators</td></tr>
<tr><td><b>07.8</b></td><td>Escape Sequences and Raw Strings</td><td><code>\n</code>, <code>\t</code>, <code>\\</code> and <code>r"raw"</code> strings</td></tr>
<tr><td><b>07.9</b></td><td>Unicode, Encoding, <code>bytes</code> vs <code>str</code></td><td>text vs bytes, and why encoding errors happen</td></tr>
<tr><td><b>07.10</b></td><td>String Concatenation Performance</td><td><code>join</code></td></tr>
<tr><td><b>07.11</b></td><td><code>textwrap</code> and the <code>string</code> Module</td><td>wrapping paragraphs, and useful constants</td></tr>
</table>

### 08. Input, Output, and Basic I/O

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>08.1</b></td><td>`print</td><td>)` in Depth (sep, end, file, flush</td></tr>
<tr><td><b>08.2</b></td><td><code>input()</code> and Parsing User Input</td><td>reading input safely, and converting it</td></tr>
<tr><td><b>08.3</b></td><td>Command-Line Arguments</td><td><code>sys.argv</code></td></tr>
<tr><td><b>08.4</b></td><td>Formatted Console Output</td><td>aligning columns and building readable reports</td></tr>
</table>

### 09. Control Flow — Conditionals

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>09.1</b></td><td><code>if</code> / <code>elif</code> / <code>else</code></td><td>branching on a condition</td></tr>
<tr><td><b>09.2</b></td><td>Nested Conditionals</td><td>conditions inside conditions, and when to flatten them</td></tr>
<tr><td><b>09.3</b></td><td>Conditional (Ternary) Expressions</td><td><code>value_if_true if condition else value_if_false</code></td></tr>
<tr><td><b>09.4</b></td><td><code>match</code> Statement — Structural Pattern Matching</td><td>matching shapes, not just values</td></tr>
<tr><td><b>09.5</b></td><td>Guard Clauses and Readable Conditions</td><td>returning early to keep code flat and readable</td></tr>
</table>

### 10. Control Flow — Loops

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>10.1</b></td><td><code>while</code> Loops</td><td>repeating while a condition holds</td></tr>
<tr><td><b>10.2</b></td><td><code>for</code> Loops and Iterables</td><td>repeating once per item</td></tr>
<tr><td><b>10.3</b></td><td><code>range()</code> in Depth</td><td>start, stop, step, and why the stop is excluded</td></tr>
<tr><td><b>10.4</b></td><td><code>break</code>, <code>continue</code>, <code>pass</code></td><td>leaving early, skipping ahead, doing nothing</td></tr>
<tr><td><b>10.5</b></td><td><code>else</code> Clause on Loops</td><td>the clause almost nobody knows about</td></tr>
<tr><td><b>10.6</b></td><td>Nested Loops</td><td>loops inside loops, and their cost</td></tr>
<tr><td><b>10.7</b></td><td><code>enumerate()</code> and <code>zip()</code></td><td>looping with a counter, and looping over pairs</td></tr>
<tr><td><b>10.8</b></td><td>Infinite Loops and Loop Safety</td><td>how to avoid a program that never stops</td></tr>
<tr><td><b>10.9</b></td><td>Loop Performance Notes</td><td>what makes a loop slow, and what to do about it</td></tr>
</table>

### 11. Lists

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>11.1</b></td><td>Creating and Accessing Lists</td><td>creating, indexing, changing items</td></tr>
<tr><td><b>11.2</b></td><td>Slicing</td><td>including step and negative indices</td></tr>
<tr><td><b>11.3</b></td><td>List Methods</td><td>complete</td></tr>
<tr><td><b>11.4</b></td><td>Mutability and In-Place Operations</td><td>changing a list in place vs building a new one</td></tr>
<tr><td><b>11.5</b></td><td>Sorting</td><td><code>sort</code> vs <code>sorted</code>, <code>key</code>, <code>reverse</code></td></tr>
<tr><td><b>11.6</b></td><td>Nested Lists and Matrices</td><td>lists inside lists, and grids</td></tr>
<tr><td><b>11.7</b></td><td>Copying: Shallow vs Deep</td><td><code>copy</code> module</td></tr>
<tr><td><b>11.8</b></td><td>Lists as Stacks and Queues</td><td>last-in-first-out and first-in-first-out</td></tr>
<tr><td><b>11.9</b></td><td>Common List Pitfalls</td><td>mutable default, <code>*</code> copy</td></tr>
</table>

### 12. Tuples

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>12.1</b></td><td>Creating Tuples and the Single-Element Trap</td><td>why <code>(5)</code> is not a tuple but <code>(5,)</code> is</td></tr>
<tr><td><b>12.2</b></td><td>Immutability and When to Use Tuples</td><td>fixed collections, and where they beat lists</td></tr>
<tr><td><b>12.3</b></td><td>Tuple Methods and Operations</td><td><code>count</code>, <code>index</code>, concatenation, repetition</td></tr>
<tr><td><b>12.4</b></td><td>Packing and Unpacking</td><td><code>point = 3, 4</code> and <code>x, y = point</code></td></tr>
<tr><td><b>12.5</b></td><td>Extended Unpacking</td><td><code>*rest</code></td></tr>
<tr><td><b>12.6</b></td><td>Tuples as Dictionary Keys</td><td>why tuples can be keys but lists cannot</td></tr>
<tr><td><b>12.7</b></td><td><code>namedtuple</code> Preview</td><td>tuples with named fields</td></tr>
</table>

### 13. Sets and Frozensets

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>13.1</b></td><td>Creating Sets, Uniqueness</td><td>unordered collections with no duplicates</td></tr>
<tr><td><b>13.2</b></td><td>Set Methods</td><td><code>add</code>, <code>remove</code>, <code>discard</code>, <code>pop</code>, <code>update</code></td></tr>
<tr><td><b>13.3</b></td><td>Set Operations</td><td>union, intersection, difference, symmetric difference</td></tr>
<tr><td><b>13.4</b></td><td>Subset / Superset / Disjoint</td><td>comparing one set against another</td></tr>
<tr><td><b>13.5</b></td><td><code>frozenset</code></td><td>the immutable set</td></tr>
<tr><td><b>13.6</b></td><td>The Hashability Requirement</td><td>what can go in a set, and why</td></tr>
<tr><td><b>13.7</b></td><td>Performance: Set vs List Lookup</td><td>why membership testing is dramatically faster</td></tr>
</table>

### 14. Dictionaries

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>14.1</b></td><td>Creating and Accessing Dictionaries</td><td>key-value pairs, lookup by key</td></tr>
<tr><td><b>14.2</b></td><td>Dictionary Methods</td><td>complete</td></tr>
<tr><td><b>14.3</b></td><td>Keys, Values, and Items Views</td><td>live views, and how they differ from lists</td></tr>
<tr><td><b>14.4</b></td><td>Iterating Dictionaries</td><td>looping over keys, values, or both</td></tr>
<tr><td><b>14.5</b></td><td>Nested Dictionaries</td><td>dictionaries inside dictionaries</td></tr>
<tr><td><b>14.6</b></td><td><code>get</code>, <code>setdefault</code>, <code>pop</code>, and Missing Keys</td><td>handling a key that might not be there</td></tr>
<tr><td><b>14.7</b></td><td>Merging Dicts</td><td><code>|</code>, <code>update</code>, <code>**</code> — three ways to combine</td></tr>
<tr><td><b>14.8</b></td><td>Dict Ordering Guarantees</td><td>insertion order, guaranteed since 3.7</td></tr>
<tr><td><b>14.9</b></td><td>Hashing and Key Requirements</td><td>what makes a valid key</td></tr>
<tr><td><b>14.10</b></td><td>Dict Performance</td><td>why lookup is fast no matter how big it gets</td></tr>
</table>

### 15. Comprehensions

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>15.1</b></td><td>List Comprehensions</td><td>building a list in one readable line</td></tr>
<tr><td><b>15.2</b></td><td>Conditional Comprehensions</td><td>filtering while you build</td></tr>
<tr><td><b>15.3</b></td><td>Nested Comprehensions</td><td>comprehensions inside comprehensions, and their limits</td></tr>
<tr><td><b>15.4</b></td><td>Dict Comprehensions</td><td>building dictionaries the same way</td></tr>
<tr><td><b>15.5</b></td><td>Set Comprehensions</td><td>building sets the same way</td></tr>
<tr><td><b>15.6</b></td><td>Generator Expressions</td><td>the lazy version that does not build a list</td></tr>
<tr><td><b>15.7</b></td><td>Readability Limits — When Not to Use Them</td><td>when a plain loop is the better choice</td></tr>
</table>

### 16. Functions — Fundamentals

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>16.1</b></td><td>Defining and Calling Functions</td><td><code>def</code>, arguments, calling</td></tr>
<tr><td><b>16.2</b></td><td>Positional Arguments</td><td>arguments matched by position</td></tr>
<tr><td><b>16.3</b></td><td>Keyword Arguments</td><td>arguments matched by name</td></tr>
<tr><td><b>16.4</b></td><td>Default Parameters and the Mutable Default Trap</td><td>the classic bug that catches everyone once</td></tr>
<tr><td><b>16.5</b></td><td><code>*args</code> and <code>**kwargs</code></td><td>accepting any number of arguments</td></tr>
<tr><td><b>16.6</b></td><td>Positional-Only (<code>/</code>) and Keyword-Only (<code>*</code>) Parameters</td><td>controlling how your function may be called</td></tr>
<tr><td><b>16.7</b></td><td>Return Values and Multiple Returns</td><td><code>return</code>, returning several values at once</td></tr>
<tr><td><b>16.8</b></td><td>Docstrings</td><td>PEP 257</td></tr>
<tr><td><b>16.9</b></td><td>Functions as First-Class Objects</td><td>passing functions around like any other value</td></tr>
</table>

### 17. Functions — Scope and Advanced

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>17.1</b></td><td>Scope and the LEGB Rule</td><td>local, enclosing, global, built-in</td></tr>
<tr><td><b>17.2</b></td><td><code>global</code> and <code>nonlocal</code></td><td>reaching outward to reassign a name</td></tr>
<tr><td><b>17.3</b></td><td>Closures</td><td>functions that remember where they came from</td></tr>
<tr><td><b>17.4</b></td><td>Lambda Functions</td><td>small anonymous functions</td></tr>
<tr><td><b>17.5</b></td><td>Recursion and Recursion Limits</td><td>functions that call themselves, and when to stop</td></tr>
<tr><td><b>17.6</b></td><td>Higher-Order Functions</td><td><code>map</code>, <code>filter</code>, <code>reduce</code></td></tr>
<tr><td><b>17.7</b></td><td><code>functools</code></td><td><code>partial</code>, <code>lru_cache</code>, <code>wraps</code>, <code>reduce</code></td></tr>
<tr><td><b>17.8</b></td><td>Pure Functions and Side Effects</td><td>why predictable functions are easier to trust</td></tr>
<tr><td><b>17.9</b></td><td>Function Annotations / Type Hints</td><td>documenting the types a function expects</td></tr>
</table>

### 18. Decorators

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>18.1</b></td><td>Decorator Theory</td><td>wrapping a function to add behaviour</td></tr>
<tr><td><b>18.2</b></td><td>Writing Simple Decorators</td><td>your first working decorator</td></tr>
<tr><td><b>18.3</b></td><td>Decorators with Arguments</td><td>decorators you can configure</td></tr>
<tr><td><b>18.4</b></td><td><code>functools.wraps</code></td><td>keeping the wrapped function's identity</td></tr>
<tr><td><b>18.5</b></td><td>Stacking Decorators</td><td>applying several at once, and the order they run</td></tr>
<tr><td><b>18.6</b></td><td>Class Decorators</td><td>decorating a class instead of a function</td></tr>
<tr><td><b>18.7</b></td><td>Practical Decorators</td><td>timing, retry, logging, caching</td></tr>
</table>

### 19. Iterators and Generators

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>19.1</b></td><td>Iterable vs Iterator Protocol</td><td>the difference, and why it matters</td></tr>
<tr><td><b>19.2</b></td><td><code>iter()</code> and <code>next()</code></td><td>the two functions behind every <code>for</code> loop</td></tr>
<tr><td><b>19.3</b></td><td>Building Custom Iterators</td><td>writing your own</td></tr>
<tr><td><b>19.4</b></td><td>Generators and <code>yield</code></td><td>pausing and resuming a function</td></tr>
<tr><td><b>19.5</b></td><td>Generator Expressions</td><td>generators without the <code>def</code></td></tr>
<tr><td><b>19.6</b></td><td><code>yield from</code></td><td>delegating to another generator</td></tr>
<tr><td><b>19.7</b></td><td>Sending Values into Generators</td><td><code>send</code>, <code>throw</code>, <code>close</code></td></tr>
<tr><td><b>19.8</b></td><td>Lazy Evaluation and Memory Benefits</td><td>handling data too big to fit in memory</td></tr>
<tr><td><b>19.9</b></td><td><code>itertools</code> Complete Tour</td><td>chaining, grouping, combining, cycling</td></tr>
</table>

### 20. Modules and Packages

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>20.1</b></td><td>What is a Module</td><td>one file, importable from another</td></tr>
<tr><td><b>20.2</b></td><td><code>import</code> Forms and Aliasing</td><td><code>import x</code>, <code>from x import y</code>, <code>as</code></td></tr>
<tr><td><b>20.3</b></td><td>Module Search Path</td><td><code>sys.path</code></td></tr>
<tr><td><b>20.4</b></td><td><code>if __name__ == "__main__"</code></td><td>running a file vs importing it</td></tr>
<tr><td><b>20.5</b></td><td>Creating Packages and <code>__init__.py</code></td><td>turning a folder into an importable package</td></tr>
<tr><td><b>20.6</b></td><td>Relative vs Absolute Imports</td><td><code>from .sibling import x</code> vs <code>from package.module import x</code></td></tr>
<tr><td><b>20.7</b></td><td>Namespace Packages</td><td>packages without an <code>__init__.py</code></td></tr>
<tr><td><b>20.8</b></td><td>Circular Imports and How to Avoid Them</td><td>why they happen, and how to restructure</td></tr>
<tr><td><b>20.9</b></td><td>Reloading Modules</td><td>re-importing without restarting</td></tr>
<tr><td><b>20.10</b></td><td><code>__all__</code> and the Public API</td><td>controlling what <code>from x import *</code> exposes</td></tr>
</table>

### 21. Standard Library Tour

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>21.1</b></td><td><code>os</code> and <code>sys</code></td><td>environment, paths, arguments, the interpreter itself</td></tr>
<tr><td><b>21.2</b></td><td><code>pathlib</code></td><td>the modern way to handle file paths</td></tr>
<tr><td><b>21.3</b></td><td><code>datetime</code>, <code>time</code>, <code>zoneinfo</code></td><td>dates, times, durations, time zones</td></tr>
<tr><td><b>21.4</b></td><td><code>random</code> and <code>secrets</code></td><td>random for simulations, secrets for security</td></tr>
<tr><td><b>21.5</b></td><td><code>collections</code></td><td><code>Counter</code>, <code>defaultdict</code>, <code>deque</code>, <code>OrderedDict</code>, <code>namedtuple</code>, <code>ChainMap</code></td></tr>
<tr><td><b>21.6</b></td><td><code>json</code>, <code>csv</code>, <code>pickle</code></td><td>the three formats you will use constantly</td></tr>
<tr><td><b>21.7</b></td><td><code>re</code> Preview</td><td>a first look before the full chapter</td></tr>
<tr><td><b>21.8</b></td><td><code>argparse</code></td><td>building real command-line tools</td></tr>
<tr><td><b>21.9</b></td><td><code>logging</code></td><td>recording what your program did</td></tr>
<tr><td><b>21.10</b></td><td><code>subprocess</code></td><td>running other programs from Python</td></tr>
<tr><td><b>21.11</b></td><td><code>shutil</code>, <code>glob</code>, <code>tempfile</code></td><td>copying, finding, and scratch files</td></tr>
<tr><td><b>21.12</b></td><td><code>statistics</code>, <code>enum</code>, <code>uuid</code>, <code>hashlib</code></td><td>averages, constants, unique ids, hashing</td></tr>
</table>

### 22. File Handling

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>22.1</b></td><td>Opening and Closing Files, File Modes</td><td><code>r</code>, <code>w</code>, <code>a</code>, <code>x</code>, <code>b</code>, <code>+</code></td></tr>
<tr><td><b>22.2</b></td><td>Reading Files</td><td><code>read</code>, <code>readline</code>, <code>readlines</code>, iteration</td></tr>
<tr><td><b>22.3</b></td><td>Writing and Appending</td><td>creating files and adding to them</td></tr>
<tr><td><b>22.4</b></td><td>Context Managers</td><td><code>with</code></td></tr>
<tr><td><b>22.5</b></td><td>Binary Files</td><td>working with bytes instead of text</td></tr>
<tr><td><b>22.6</b></td><td>Encodings and <code>newline</code></td><td>getting text right across platforms</td></tr>
<tr><td><b>22.7</b></td><td>File Positions</td><td><code>seek</code>, <code>tell</code></td></tr>
<tr><td><b>22.8</b></td><td><code>os</code> and <code>pathlib</code> File Operations</td><td>creating, moving, renaming, deleting</td></tr>
<tr><td><b>22.9</b></td><td>Working with CSV</td><td>reading and writing spreadsheet data</td></tr>
<tr><td><b>22.10</b></td><td>Working with JSON</td><td>reading and writing structured data</td></tr>
<tr><td><b>22.11</b></td><td>Serialization: <code>pickle</code></td><td>saving Python objects, and why it is risky</td></tr>
<tr><td><b>22.12</b></td><td>Temporary Files and Directories</td><td>scratch space that cleans itself up</td></tr>
</table>

### 23. Error Handling and Exceptions

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>23.1</b></td><td>Errors vs Exceptions</td><td>theory</td></tr>
<tr><td><b>23.2</b></td><td>The Exception Hierarchy</td><td>what inherits from what, and why you care</td></tr>
<tr><td><b>23.3</b></td><td><code>try</code> / <code>except</code></td><td>catching what goes wrong</td></tr>
<tr><td><b>23.4</b></td><td>Multiple and Grouped Excepts</td><td>handling several failure modes</td></tr>
<tr><td><b>23.5</b></td><td><code>else</code> and <code>finally</code></td><td>the two clauses people forget</td></tr>
<tr><td><b>23.6</b></td><td><code>raise</code> and Re-Raising</td><td>raising your own, and passing one along</td></tr>
<tr><td><b>23.7</b></td><td>Exception Chaining</td><td><code>from</code></td></tr>
<tr><td><b>23.8</b></td><td>Custom Exception Classes</td><td>errors that describe your own problem domain</td></tr>
<tr><td><b>23.9</b></td><td><code>assert</code> and Assertions</td><td>checking assumptions during development</td></tr>
<tr><td><b>23.10</b></td><td>Exception Groups and <code>except*</code></td><td>handling several errors at once</td></tr>
<tr><td><b>23.11</b></td><td>EAFP vs LBYL</td><td>ask forgiveness, or ask permission</td></tr>
<tr><td><b>23.12</b></td><td>Best Practices and Anti-Patterns</td><td>what to catch, what to let through</td></tr>
</table>

### 24. OOP — Fundamentals

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>24.1</b></td><td>OOP Theory</td><td>objects, classes, abstraction</td></tr>
<tr><td><b>24.2</b></td><td>Defining Classes, Creating Instances</td><td><code>class</code>, instances, the basics</td></tr>
<tr><td><b>24.3</b></td><td>Instance Attributes and <code>self</code></td><td>data that belongs to one object</td></tr>
<tr><td><b>24.4</b></td><td>The <code>__init__</code> Constructor</td><td>setting an object up when it is created</td></tr>
<tr><td><b>24.5</b></td><td>Class Attributes vs Instance Attributes</td><td>shared by all, vs owned by one</td></tr>
<tr><td><b>24.6</b></td><td>Instance Methods</td><td>functions that belong to an object</td></tr>
<tr><td><b>24.7</b></td><td>Class Methods and <code>@classmethod</code></td><td>methods that work on the class itself</td></tr>
<tr><td><b>24.8</b></td><td>Static Methods and <code>@staticmethod</code></td><td>methods that need neither instance nor class</td></tr>
<tr><td><b>24.9</b></td><td><code>__del__</code> and Object Lifecycle</td><td>creation, use, and cleanup</td></tr>
</table>

### 25. OOP — Encapsulation and Properties

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>25.1</b></td><td>Public, Protected, and Private Conventions</td><td><code>name</code>, <code>_name</code>, <code>__name</code></td></tr>
<tr><td><b>25.2</b></td><td>Name Mangling</td><td>what <code>__name</code> actually does</td></tr>
<tr><td><b>25.3</b></td><td>Getters and Setters</td><td>controlling access to an attribute</td></tr>
<tr><td><b>25.4</b></td><td>The <code>@property</code> Decorator</td><td>methods that look like plain attributes</td></tr>
<tr><td><b>25.5</b></td><td>Computed Attributes</td><td>values worked out on demand</td></tr>
<tr><td><b>25.6</b></td><td><code>__slots__</code></td><td>trading flexibility for memory</td></tr>
</table>

### 26. OOP — Inheritance and Polymorphism

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>26.1</b></td><td>Single Inheritance</td><td>one class building on another</td></tr>
<tr><td><b>26.2</b></td><td><code>super()</code> in Depth</td><td>calling up to the parent, correctly</td></tr>
<tr><td><b>26.3</b></td><td>Method Overriding</td><td>replacing a parent's behaviour</td></tr>
<tr><td><b>26.4</b></td><td>Multiple Inheritance</td><td>inheriting from several classes at once</td></tr>
<tr><td><b>26.5</b></td><td>Method Resolution Order (MRO) and C3 Linearization</td><td>the rule that decides which method wins</td></tr>
<tr><td><b>26.6</b></td><td>Mixins</td><td>small reusable behaviour, added by inheritance</td></tr>
<tr><td><b>26.7</b></td><td>Polymorphism and Duck Typing</td><td>if it quacks, it is a duck</td></tr>
<tr><td><b>26.8</b></td><td><code>isinstance</code> vs <code>type</code> vs Duck Typing</td><td>three ways to ask what something is</td></tr>
<tr><td><b>26.9</b></td><td>Composition vs Inheritance</td><td>has-a, or is-a</td></tr>
</table>

### 27. OOP — Magic Methods

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>27.1</b></td><td><code>__str__</code> vs <code>__repr__</code></td><td>friendly text, and unambiguous text</td></tr>
<tr><td><b>27.2</b></td><td>Comparison Dunders</td><td><code>__eq__</code>, <code>__lt__</code>, …</td></tr>
<tr><td><b>27.3</b></td><td><code>__hash__</code> and the Hashability Contract</td><td>making your objects usable as keys</td></tr>
<tr><td><b>27.4</b></td><td>Arithmetic Operator Overloading</td><td>making <code>+</code>, <code>-</code>, <code>*</code> work on your own types</td></tr>
<tr><td><b>27.5</b></td><td>Container Dunders</td><td><code>__len__</code>, <code>__getitem__</code>, <code>__contains__</code>, <code>__iter__</code></td></tr>
<tr><td><b>27.6</b></td><td>Callable Objects</td><td><code>__call__</code></td></tr>
<tr><td><b>27.7</b></td><td>Attribute Access</td><td><code>__getattr__</code>, <code>__setattr__</code>, <code>__getattribute__</code></td></tr>
<tr><td><b>27.8</b></td><td>The Context Manager Protocol</td><td><code>__enter__</code>, <code>__exit__</code></td></tr>
<tr><td><b>27.9</b></td><td><code>__new__</code> vs <code>__init__</code></td><td>creating an object, vs setting it up</td></tr>
<tr><td><b>27.10</b></td><td>Complete Dunder Reference</td><td>the full list, in one place</td></tr>
</table>

### 28. OOP — Advanced

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>28.1</b></td><td>Abstract Base Classes</td><td><code>abc</code></td></tr>
<tr><td><b>28.2</b></td><td>Protocols and Structural Typing</td><td>typing by shape, not by inheritance</td></tr>
<tr><td><b>28.3</b></td><td><code>dataclasses</code> Complete</td><td>classes that write their own boilerplate</td></tr>
<tr><td><b>28.4</b></td><td><code>enum</code> Complete</td><td>fixed sets of named values</td></tr>
<tr><td><b>28.5</b></td><td><code>NamedTuple</code> and <code>TypedDict</code></td><td>typed records and typed dictionaries</td></tr>
<tr><td><b>28.6</b></td><td>Descriptors</td><td>the machinery behind <code>@property</code></td></tr>
<tr><td><b>28.7</b></td><td>Metaclasses</td><td>classes that build classes</td></tr>
<tr><td><b>28.8</b></td><td>Class Creation Hooks</td><td><code>__init_subclass__</code>, <code>__set_name__</code></td></tr>
<tr><td><b>28.9</b></td><td>Design Patterns in Python</td><td>singleton, factory, observer, strategy</td></tr>
<tr><td><b>28.10</b></td><td>SOLID Principles in Python</td><td>five design principles, with Python examples</td></tr>
</table>

### 29. Context Managers

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>29.1</b></td><td><code>with</code> Statement Theory</td><td>why <code>with</code> exists</td></tr>
<tr><td><b>29.2</b></td><td>Class-Based Context Managers</td><td><code>__enter__</code> and <code>__exit__</code></td></tr>
<tr><td><b>29.3</b></td><td><code>contextlib.contextmanager</code></td><td>the decorator that turns a generator into one</td></tr>
<tr><td><b>29.4</b></td><td><code>contextlib</code> Utilities</td><td><code>suppress</code>, <code>closing</code>, <code>ExitStack</code></td></tr>
<tr><td><b>29.5</b></td><td>Multiple Context Managers</td><td>managing several resources at once</td></tr>
<tr><td><b>29.6</b></td><td>Async Context Managers Preview</td><td><code>async with</code>, previewing Chapter 35</td></tr>
</table>

### 30. Regular Expressions

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>30.1</b></td><td>Regex Theory and Syntax</td><td>what a pattern is, and how matching works</td></tr>
<tr><td><b>30.2</b></td><td>Character Classes and Quantifiers</td><td><code>\d</code>, <code>\w</code>, <code>[a-z]</code>, <code>*</code>, <code>+</code>, <code>?</code>, <code>{n,m}</code></td></tr>
<tr><td><b>30.3</b></td><td>Anchors and Boundaries</td><td><code>^</code>, <code>$</code>, <code>\b</code></td></tr>
<tr><td><b>30.4</b></td><td>Groups and Capturing</td><td>pulling pieces out of a match</td></tr>
<tr><td><b>30.5</b></td><td>Named Groups, Lookahead, Lookbehind</td><td>readable groups, and matching by context</td></tr>
<tr><td><b>30.6</b></td><td><code>re</code> Module Functions</td><td><code>match</code>, <code>search</code>, <code>findall</code>, <code>finditer</code>, <code>sub</code></td></tr>
<tr><td><b>30.7</b></td><td>Flags</td><td>case-insensitive, multiline, verbose</td></tr>
<tr><td><b>30.8</b></td><td>Substitution and Splitting</td><td>find and replace, and splitting on a pattern</td></tr>
<tr><td><b>30.9</b></td><td>Greedy vs Lazy, Catastrophic Backtracking</td><td>how a regex can hang your program</td></tr>
<tr><td><b>30.10</b></td><td>Practical Patterns</td><td>emails, dates, log lines, and how to test them</td></tr>
</table>

### 31. Functional Programming

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>31.1</b></td><td>Functional Concepts in Python</td><td>what transfers from functional languages, and what does not</td></tr>
<tr><td><b>31.2</b></td><td>Immutability Practices</td><td>working without changing state</td></tr>
<tr><td><b>31.3</b></td><td><code>map</code>, <code>filter</code>, <code>reduce</code> Deep Dive</td><td>the three classic transformations</td></tr>
<tr><td><b>31.4</b></td><td>Function Composition</td><td>building big functions out of small ones</td></tr>
<tr><td><b>31.5</b></td><td>Currying and Partial Application</td><td>fixing some arguments now, the rest later</td></tr>
<tr><td><b>31.6</b></td><td>The <code>operator</code> Module</td><td>operators as functions you can pass around</td></tr>
<tr><td><b>31.7</b></td><td>Limits of FP in Python</td><td>why Python is not Haskell, and why that is fine</td></tr>
</table>

### 32. Type Hints and Static Typing

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>32.1</b></td><td>Why Type Hints</td><td>catching bugs before you run the code</td></tr>
<tr><td><b>32.2</b></td><td>Basic Annotations</td><td>annotating arguments, returns, and variables</td></tr>
<tr><td><b>32.3</b></td><td><code>typing</code> Module Core</td><td><code>Optional</code>, <code>Union</code>, <code>Any</code>, <code>Literal</code></td></tr>
<tr><td><b>32.4</b></td><td>Generics and <code>TypeVar</code></td><td>types that work with any contained type</td></tr>
<tr><td><b>32.5</b></td><td>Modern Syntax</td><td><code>list[int]</code> and <code>X | Y</code>, replacing <code>List</code> and <code>Union</code></td></tr>
<tr><td><b>32.6</b></td><td><code>Callable</code>, <code>Protocol</code>, <code>Self</code></td><td>typing functions, shapes, and returns</td></tr>
<tr><td><b>32.7</b></td><td>Using <code>mypy</code></td><td>running a type checker over your code</td></tr>
<tr><td><b>32.8</b></td><td>Runtime Type Checking and Its Limits</td><td>what type hints do not do</td></tr>
</table>

### 33. Concurrency — Threading

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>33.1</b></td><td>Concurrency vs Parallelism</td><td>theory</td></tr>
<tr><td><b>33.2</b></td><td>Processes vs Threads</td><td>the real difference, and when each applies</td></tr>
<tr><td><b>33.3</b></td><td>The GIL Explained</td><td>why threads do not speed up CPU work</td></tr>
<tr><td><b>33.4</b></td><td>The <code>threading</code> Module</td><td>starting, joining, and managing threads</td></tr>
<tr><td><b>33.5</b></td><td>Locks, RLocks, Semaphores, Events</td><td>coordinating threads safely</td></tr>
<tr><td><b>33.6</b></td><td>Race Conditions and Deadlocks</td><td>the two classic threading bugs</td></tr>
<tr><td><b>33.7</b></td><td><code>queue</code> for Thread Communication</td><td>passing work between threads safely</td></tr>
<tr><td><b>33.8</b></td><td><code>concurrent.futures.ThreadPoolExecutor</code></td><td>the high-level way to run threads</td></tr>
</table>

### 34. Concurrency — Multiprocessing

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>34.1</b></td><td>The <code>multiprocessing</code> Module</td><td>true parallelism, at a cost</td></tr>
<tr><td><b>34.2</b></td><td>Process Pools</td><td>spreading work across CPU cores</td></tr>
<tr><td><b>34.3</b></td><td>Inter-Process Communication</td><td>Pipes, Queues</td></tr>
<tr><td><b>34.4</b></td><td>Shared Memory</td><td>sharing memory instead of copying</td></tr>
<tr><td><b>34.5</b></td><td><code>ProcessPoolExecutor</code></td><td>the high-level way to run processes</td></tr>
<tr><td><b>34.6</b></td><td>Choosing Threads vs Processes vs Async</td><td>a decision guide you can actually use</td></tr>
</table>

### 35. Asynchronous Programming

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>35.1</b></td><td>Async Theory and the Event Loop</td><td>how one thread does many things at once</td></tr>
<tr><td><b>35.2</b></td><td><code>async</code> / <code>await</code> Syntax</td><td>the two keywords that drive it all</td></tr>
<tr><td><b>35.3</b></td><td>Coroutines and Tasks</td><td>scheduling work, and waiting for it</td></tr>
<tr><td><b>35.4</b></td><td><code>asyncio.gather</code>, <code>wait</code>, <code>TaskGroup</code></td><td>running many things concurrently</td></tr>
<tr><td><b>35.5</b></td><td>Async Iterators and Generators</td><td><code>async for</code> and <code>yield</code> together</td></tr>
<tr><td><b>35.6</b></td><td>Async Context Managers</td><td><code>async with</code></td></tr>
<tr><td><b>35.7</b></td><td>Timeouts and Cancellation</td><td>giving up on work that takes too long</td></tr>
<tr><td><b>35.8</b></td><td>Mixing Sync and Async Code</td><td>the traps at the boundary</td></tr>
<tr><td><b>35.9</b></td><td>Practical Async I/O</td><td>files and network, without blocking</td></tr>
</table>

### 36. Testing

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>36.1</b></td><td>Why Test — Theory and Test Types</td><td>unit, integration, end-to-end, and what to test</td></tr>
<tr><td><b>36.2</b></td><td><code>unittest</code> Basics</td><td>the testing framework in the standard library</td></tr>
<tr><td><b>36.3</b></td><td>Assertions and Test Fixtures</td><td>checking results, and setting up test data</td></tr>
<tr><td><b>36.4</b></td><td><code>pytest</code> Basics</td><td>the framework most projects actually use</td></tr>
<tr><td><b>36.5</b></td><td><code>pytest</code> Fixtures</td><td>reusable setup, done properly</td></tr>
<tr><td><b>36.6</b></td><td>Parametrized Tests</td><td>one test, many inputs</td></tr>
<tr><td><b>36.7</b></td><td>Mocking</td><td><code>unittest.mock</code>, <code>monkeypatch</code></td></tr>
<tr><td><b>36.8</b></td><td>Test Coverage</td><td>measuring what your tests actually reach</td></tr>
<tr><td><b>36.9</b></td><td><code>doctest</code></td><td>tests that live inside your docstrings</td></tr>
<tr><td><b>36.10</b></td><td>The TDD Workflow</td><td>write the test first, then the code</td></tr>
</table>

### 37. Debugging, Logging, Profiling

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>37.1</b></td><td>Reading Tracebacks</td><td>reading an error from the bottom up</td></tr>
<tr><td><b>37.2</b></td><td>Debugging with <code>print</code> vs a Debugger</td><td>when each one is the right tool</td></tr>
<tr><td><b>37.3</b></td><td><code>pdb</code> / <code>breakpoint()</code></td><td>stepping through code line by line</td></tr>
<tr><td><b>37.4</b></td><td>The VS Code Debugger</td><td>breakpoints, watches, and the call stack</td></tr>
<tr><td><b>37.5</b></td><td><code>logging</code> Deep Dive</td><td>levels, handlers, formatters, config</td></tr>
<tr><td><b>37.6</b></td><td>Profiling</td><td><code>timeit</code>, <code>cProfile</code>, memory</td></tr>
<tr><td><b>37.7</b></td><td>Optimization Strategies</td><td>measure first, then optimise</td></tr>
<tr><td><b>37.8</b></td><td>Big-O Basics for Python Data Structures</td><td>why the right data structure beats clever code</td></tr>
</table>

### 38. Working with Data Formats and APIs

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>38.1</b></td><td>JSON Deep Dive</td><td>nested data, custom encoders, common errors</td></tr>
<tr><td><b>38.2</b></td><td>CSV Deep Dive</td><td>delimiters, quoting, headers, dialects</td></tr>
<tr><td><b>38.3</b></td><td>XML and YAML</td><td>when you meet them, and how to handle them</td></tr>
<tr><td><b>38.4</b></td><td>HTTP Basics</td><td>requests, responses, status codes, headers</td></tr>
<tr><td><b>38.5</b></td><td><code>urllib</code> and <code>requests</code></td><td>fetching data over the network</td></tr>
<tr><td><b>38.6</b></td><td>Consuming REST APIs</td><td>authentication, pagination, error handling</td></tr>
<tr><td><b>38.7</b></td><td>Web Scraping Basics (<code>BeautifulSoup</code>) and Ethics</td><td>parsing HTML, and scraping responsibly</td></tr>
</table>

### 39. Databases

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>39.1</b></td><td>Database Theory and SQL Refresher</td><td>tables, rows, keys, and the queries you need</td></tr>
<tr><td><b>39.2</b></td><td>The <code>sqlite3</code> Module</td><td>a real database with no server to install</td></tr>
<tr><td><b>39.3</b></td><td>CRUD Operations</td><td>create, read, update, delete</td></tr>
<tr><td><b>39.4</b></td><td>Parameterized Queries and SQL Injection</td><td>the single most important security habit here</td></tr>
<tr><td><b>39.5</b></td><td>Transactions</td><td>all-or-nothing changes</td></tr>
<tr><td><b>39.6</b></td><td>ORM Introduction</td><td>SQLAlchemy basics</td></tr>
</table>

### 40. Project Structure and Packaging

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>40.1</b></td><td>Project Layout Conventions</td><td><code>src</code> layout</td></tr>
<tr><td><b>40.2</b></td><td><code>requirements.txt</code> vs <code>pyproject.toml</code></td><td>declaring what your project needs</td></tr>
<tr><td><b>40.3</b></td><td>Dependency Management Tools</td><td><code>pip-tools</code>, <code>poetry</code>, <code>uv</code></td></tr>
<tr><td><b>40.4</b></td><td>Building a Distributable Package</td><td>turning your code into something installable</td></tr>
<tr><td><b>40.5</b></td><td>Publishing to PyPI</td><td>sharing your package with the world</td></tr>
<tr><td><b>40.6</b></td><td>Entry Points and CLI Tools</td><td>making your package runnable as a command</td></tr>
<tr><td><b>40.7</b></td><td>Semantic Versioning</td><td>what the numbers in <code>1.4.2</code> actually promise</td></tr>
</table>

### 41. Code Quality and Tooling

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>41.1</b></td><td>PEP 8 Deep Dive</td><td>naming, spacing, imports, line length</td></tr>
<tr><td><b>41.2</b></td><td>Linters</td><td><code>ruff</code>, <code>flake8</code>, <code>pylint</code></td></tr>
<tr><td><b>41.3</b></td><td>Formatters</td><td><code>black</code>, <code>ruff format</code></td></tr>
<tr><td><b>41.4</b></td><td>Pre-commit Hooks</td><td>running checks automatically before each commit</td></tr>
<tr><td><b>41.5</b></td><td>Docstring Standards and <code>sphinx</code> / <code>mkdocs</code></td><td>writing docs people will actually read</td></tr>
<tr><td><b>41.6</b></td><td>Code Smells and Refactoring</td><td>recognising bad code, and improving it safely</td></tr>
<tr><td><b>41.7</b></td><td>Clean Code Principles</td><td>naming, function size, and single responsibility</td></tr>
</table>

### 42. Security Basics

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>42.1</b></td><td>Input Validation</td><td>never trust what comes in from outside</td></tr>
<tr><td><b>42.2</b></td><td>Secrets Management</td><td><code>.env</code>, environment variables</td></tr>
<tr><td><b>42.3</b></td><td>Hashing and Passwords</td><td>storing passwords so a leak is survivable</td></tr>
<tr><td><b>42.4</b></td><td>Common Python Vulnerabilities</td><td><code>eval</code>, <code>pickle</code>, path traversal</td></tr>
<tr><td><b>42.5</b></td><td>Dependency Security</td><td>auditing what your dependencies bring with them</td></tr>
</table>

### 43. Advanced Internals

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>43.1</b></td><td>Bytecode and <code>dis</code></td><td>seeing the instructions your code compiles to</td></tr>
<tr><td><b>43.2</b></td><td>Memory Management Deep Dive</td><td>reference counting, and the object model</td></tr>
<tr><td><b>43.3</b></td><td>The <code>gc</code> Module and Circular References</td><td>the collector that catches what counting misses</td></tr>
<tr><td><b>43.4</b></td><td><code>weakref</code></td><td>references that do not keep an object alive</td></tr>
<tr><td><b>43.5</b></td><td>Interning and the Small Integer Cache</td><td>why <code>a is b</code> is sometimes surprisingly <code>True</code></td></tr>
<tr><td><b>43.6</b></td><td><code>sys</code> Internals</td><td>recursion limits, sizes, and interpreter internals</td></tr>
<tr><td><b>43.7</b></td><td>C Extensions and <code>ctypes</code> Introduction</td><td>calling C code from Python</td></tr>
</table>

### 44. Projects

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>44.1</b></td><td>Beginner: CLI Calculator / Number Game</td><td>input, conditionals, loops, functions</td></tr>
<tr><td><b>44.2</b></td><td>Beginner: Text File Word Counter</td><td>file reading, dictionaries, sorting</td></tr>
<tr><td><b>44.3</b></td><td>Intermediate: To-Do CLI with JSON Storage</td><td>persistence, JSON, and a real command-line interface</td></tr>
<tr><td><b>44.4</b></td><td>Intermediate: API Data Fetcher</td><td>HTTP, JSON parsing, error handling</td></tr>
<tr><td><b>44.5</b></td><td>OOP: Bank / Library Management System</td><td>classes, inheritance, encapsulation</td></tr>
<tr><td><b>44.6</b></td><td>Database: Contact Book with SQLite</td><td>SQL, CRUD, transactions</td></tr>
<tr><td><b>44.7</b></td><td>Async: Concurrent Downloader</td><td><code>asyncio</code>, concurrency, timing</td></tr>
<tr><td><b>44.8</b></td><td>Capstone: Packaged CLI Tool with Tests</td><td>packaging, testing, documentation, publishing</td></tr>
</table>

### 45. Appendix

<table width="100%">
<tr><th align="left" width="8%">#</th><th align="left" width="37%">Topic</th><th align="left" width="55%">Covers</th></tr>
<tr><td><b>45.1</b></td><td>Complete Built-in Functions Reference</td><td>every built-in, with a one-line description</td></tr>
<tr><td><b>45.2</b></td><td>Complete Keyword Reference</td><td>every keyword, with a one-line description</td></tr>
<tr><td><b>45.3</b></td><td>Dunder Method Cheat Sheet</td><td>every dunder, grouped by purpose</td></tr>
<tr><td><b>45.4</b></td><td>Exception Hierarchy Chart</td><td>the full tree, as a diagram</td></tr>
<tr><td><b>45.5</b></td><td>Glossary</td><td>every term in this course, defined</td></tr>
<tr><td><b>45.6</b></td><td>Further Resources</td><td>books, docs, and where to go next</td></tr>
</table>


---

## Code Style in This Repo

- Clean and readable over clever. If a loop is clearer than a comprehension, it's a loop.
- A comment above every meaningful line, explaining intent — not restating syntax.
- Descriptive names. No `x`, `tmp`, or `data2`.
- Small examples that each demonstrate one idea.
- Output is printed with labels so you can match each line to the code that produced it.
- One concept per notebook cell, with the explanation in the markdown cell directly above it.
- Notebooks are committed without saved output, so every run is genuinely yours.
