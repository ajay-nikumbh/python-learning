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
<tr><td align="center">✅</td><td align="center"><b>01</b></td><td align="left">Introduction to Programming</td><td align="left">Think like a programmer before writing any code</td><td align="center">8</td><td align="left">Complete</td></tr>
<tr><td align="center">✅</td><td align="center"><b>02</b></td><td align="left">Setup and First Program</td><td align="left">Get Python installed and run your first script</td><td align="center">7</td><td align="left">Complete</td></tr>
<tr><td align="center">✅</td><td align="center"><b>03</b></td><td align="left">Syntax Fundamentals</td><td align="left">Read and write correctly formed Python</td><td align="center">7</td><td align="left">Complete</td></tr>
<tr><td align="center">⬜</td><td align="center"><b>04</b></td><td align="left">Variables and Memory Model</td><td align="left">Understand what a variable really is</td><td align="center">8</td><td align="left">Up next</td></tr>
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

**Level:** ● beginner &nbsp;·&nbsp; ●● intermediate &nbsp;·&nbsp; ●●● advanced

### 01. Introduction to Programming

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>01.1</b></td><td>What is Programming</td><td>instructions, precision, program vs process</td><td>Every bug traces back to this gap</td><td align="center">●</td></tr>
<tr><td><b>01.2</b></td><td>How Computers Execute Code</td><td>CPU, memory, binary, machine code</td><td>Explains errors that look like magic</td><td align="center">●</td></tr>
<tr><td><b>01.3</b></td><td>Algorithms and Pseudocode</td><td>steps, decomposition, the three building blocks</td><td>The skill that survives any language</td><td align="center">●</td></tr>
<tr><td><b>01.4</b></td><td>Compiled vs Interpreted Languages</td><td>bytecode, the PVM, <code>__pycache__</code></td><td>Explains when errors appear</td><td align="center">●</td></tr>
<tr><td><b>01.5</b></td><td>Programming Paradigms Overview</td><td>procedural, OOP, functional</td><td>Stops you forcing one style everywhere</td><td align="center">●</td></tr>
<tr><td><b>01.6</b></td><td>What is Python</td><td>history, philosophy, Zen of Python, versions</td><td>Tells you what good Python looks like</td><td align="center">●</td></tr>
<tr><td><b>01.7</b></td><td>Where Python is Used</td><td>the domains it leads, and where it is the wrong tool</td><td>Knowing the limits is engineering judgement</td><td align="center">●</td></tr>
<tr><td><b>01.8</b></td><td>CPython vs PyPy vs Other Implementations</td><td>the reference implementation, JIT, the GIL</td><td>Avoids chasing the wrong performance fix</td><td align="center">●</td></tr>
</table>

### 02. Setup and First Program

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>02.1</b></td><td>Installing Python</td><td>Windows/macOS/Linux</td><td>A broken install blocks everything else</td><td align="center">●</td></tr>
<tr><td><b>02.2</b></td><td>Python Interpreter and REPL</td><td>interactive mode, <code>help()</code>, <code>dir()</code></td><td>Your fastest way to test an idea</td><td align="center">●</td></tr>
<tr><td><b>02.3</b></td><td>Editors and IDEs</td><td>VS Code setup</td><td>Good tooling catches errors as you type</td><td align="center">●</td></tr>
<tr><td><b>02.4</b></td><td>Writing and Running First Script</td><td>your first file, running it from a terminal</td><td>The first real feedback loop</td><td align="center">●</td></tr>
<tr><td><b>02.5</b></td><td>Virtual Environments Intro</td><td><code>venv</code></td><td>Prevents projects breaking each other</td><td align="center">●</td></tr>
<tr><td><b>02.6</b></td><td><code>pip</code> Basics</td><td>installing, upgrading, freezing, uninstalling</td><td>Unlocks the whole library ecosystem</td><td align="center">●</td></tr>
<tr><td><b>02.7</b></td><td>Anatomy of a Python File</td><td>shebang, encoding, <code>__main__</code></td><td>Explains what every real file contains</td><td align="center">●</td></tr>
</table>

### 03. Syntax Fundamentals

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>03.1</b></td><td>Statements and Expressions</td><td>what evaluates to a value, and what does not</td><td>Explains what you can assign or pass</td><td align="center">●</td></tr>
<tr><td><b>03.2</b></td><td>Indentation Rules and Blocks</td><td>whitespace as syntax, nesting, <code>IndentationError</code></td><td>Python's most common beginner error</td><td align="center">●</td></tr>
<tr><td><b>03.3</b></td><td>Comments</td><td>single, multi-line, docstrings</td><td>Code is read more often than written</td><td align="center">●</td></tr>
<tr><td><b>03.4</b></td><td>Line Continuation</td><td>implicit vs explicit, backslashes, brackets</td><td>Keeps long lines readable</td><td align="center">●</td></tr>
<tr><td><b>03.5</b></td><td>Keywords and Identifiers</td><td>reserved words, valid names, naming rules</td><td>Avoids shadowing built-ins by accident</td><td align="center">●</td></tr>
<tr><td><b>03.6</b></td><td>PEP 8 Introduction</td><td>the style guide every Python project follows</td><td>The shared style every project expects</td><td align="center">●</td></tr>
<tr><td><b>03.7</b></td><td>Common Beginner Syntax Errors</td><td>reading and fixing the errors beginners hit most</td><td>Turns cryptic messages into quick fixes</td><td align="center">●</td></tr>
</table>

### 04. Variables and Memory Model

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>04.1</b></td><td>Variables and Assignment</td><td>binding a name to a value</td><td>The foundation of every program</td><td align="center">●</td></tr>
<tr><td><b>04.2</b></td><td>Names, Objects, References</td><td>why a variable is a label, not a box</td><td>The single biggest beginner misconception</td><td align="center">●</td></tr>
<tr><td><b>04.3</b></td><td><code>id()</code>, <code>type()</code>, and Object Identity</td><td>what an object actually is, and how to inspect one</td><td>Lets you inspect anything at runtime</td><td align="center">●</td></tr>
<tr><td><b>04.4</b></td><td>Mutable vs Immutable Objects</td><td>which types can change in place, and which cannot</td><td>Decides whether a change is visible elsewhere</td><td align="center">●</td></tr>
<tr><td><b>04.5</b></td><td>Reference Semantics and Aliasing</td><td>why two names can point at one object</td><td>Explains bugs where data changes by itself</td><td align="center">●</td></tr>
<tr><td><b>04.6</b></td><td>Garbage Collection and Reference Counting</td><td>how Python frees memory you stopped using</td><td>Explains when memory is actually freed</td><td align="center">●</td></tr>
<tr><td><b>04.7</b></td><td>Constants and Naming Conventions</td><td><code>UPPER_CASE</code>, <code>snake_case</code>, <code>_private</code></td><td>Signals intent to the next reader</td><td align="center">●</td></tr>
<tr><td><b>04.8</b></td><td>Multiple Assignment and Swapping</td><td><code>a, b = 1, 2</code> and <code>a, b = b, a</code></td><td>Cleaner than juggling temporary variables</td><td align="center">●</td></tr>
</table>

### 05. Data Types — Numbers and Booleans

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>05.1</b></td><td>Integers</td><td>arbitrary precision, bases</td><td>No overflow, unlike most languages</td><td align="center">●</td></tr>
<tr><td><b>05.2</b></td><td>Floats</td><td>IEEE 754, precision pitfalls</td><td>Why 0.1 + 0.2 is not 0.3</td><td align="center">●</td></tr>
<tr><td><b>05.3</b></td><td>Complex Numbers</td><td>real and imaginary parts, <code>j</code> notation</td><td>Needed for signal and scientific work</td><td align="center">●</td></tr>
<tr><td><b>05.4</b></td><td><code>Decimal</code> and <code>Fraction</code></td><td>exact arithmetic when floats will not do</td><td>Required wherever money is involved</td><td align="center">●</td></tr>
<tr><td><b>05.5</b></td><td>Booleans and Truthiness</td><td>what counts as <code>True</code>, what counts as <code>False</code></td><td>Powers every condition you write</td><td align="center">●</td></tr>
<tr><td><b>05.6</b></td><td><code>None</code> Type</td><td>absence of a value, and why it is not zero</td><td>The default return of every function</td><td align="center">●</td></tr>
<tr><td><b>05.7</b></td><td>Type Conversion / Casting</td><td><code>int()</code>, <code>float()</code>, <code>str()</code>, <code>bool()</code></td><td>Input arrives as text and must be converted</td><td align="center">●</td></tr>
<tr><td><b>05.8</b></td><td><code>math</code> Module Essentials</td><td>rounding, roots, logs, constants</td><td>Covers most everyday maths</td><td align="center">●</td></tr>
</table>

### 06. Operators

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>06.1</b></td><td>Arithmetic Operators</td><td><code>+  -  *  /  //  %  **</code></td><td>Used in almost every line you write</td><td align="center">●</td></tr>
<tr><td><b>06.2</b></td><td>Comparison Operators and Chaining</td><td><code>==  !=  &lt;  &gt;  &lt;=  &gt;=</code> and <code>a &lt; b &lt; c</code></td><td>Drives every decision in your code</td><td align="center">●</td></tr>
<tr><td><b>06.3</b></td><td>Logical Operators and Short-Circuiting</td><td><code>and</code>, <code>or</code>, <code>not</code>, and lazy evaluation</td><td>Lets you guard against errors safely</td><td align="center">●</td></tr>
<tr><td><b>06.4</b></td><td>Assignment and Augmented Assignment</td><td><code>=</code>, <code>+=</code>, <code>-=</code>, <code>*=</code> and friends</td><td>Shorter and clearer than repeating a name</td><td align="center">●</td></tr>
<tr><td><b>06.5</b></td><td>Bitwise Operators</td><td><code>&amp;</code>, <code>|</code>, <code>^</code>, <code>~</code>, <code>&lt;&lt;</code>, <code>&gt;&gt;</code></td><td>Needed for flags, masks and low-level work</td><td align="center">●</td></tr>
<tr><td><b>06.6</b></td><td>Identity Operators</td><td><code>is</code>, <code>is not</code></td><td>The classic `is` vs `==` trap</td><td align="center">●</td></tr>
<tr><td><b>06.7</b></td><td>Membership Operators</td><td><code>in</code>, <code>not in</code></td><td>The readable way to search a collection</td><td align="center">●</td></tr>
<tr><td><b>06.8</b></td><td>Operator Precedence and Associativity</td><td>what binds tightest, and when to add brackets</td><td>Prevents silently wrong calculations</td><td align="center">●</td></tr>
<tr><td><b>06.9</b></td><td>Walrus Operator</td><td><code>:=</code></td><td>Assign and test in one step</td><td align="center">●</td></tr>
</table>

### 07. Strings

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>07.1</b></td><td>String Literals and Quoting</td><td>single, double, triple quotes</td><td>Choosing quotes avoids escaping pain</td><td align="center">●</td></tr>
<tr><td><b>07.2</b></td><td>Indexing and Slicing</td><td><code>[i]</code>, <code>[a:b]</code>, <code>[a:b:step]</code>, negative indices</td><td>Extracting parts of text is constant work</td><td align="center">●</td></tr>
<tr><td><b>07.3</b></td><td>String Immutability</td><td>why strings cannot be changed in place</td><td>Explains why methods return new strings</td><td align="center">●</td></tr>
<tr><td><b>07.4</b></td><td>String Methods</td><td>complete tour</td><td>Covers most text work you will ever do</td><td align="center">●</td></tr>
<tr><td><b>07.5</b></td><td>Formatting: f-strings</td><td>the modern way to build strings</td><td>The clearest way to build text</td><td align="center">●</td></tr>
<tr><td><b>07.6</b></td><td>Formatting: <code>.format()</code> and <code>%</code></td><td>the older styles, and where you still meet them</td><td>You will meet these in existing code</td><td align="center">●</td></tr>
<tr><td><b>07.7</b></td><td>Format Spec Mini-Language</td><td>padding, alignment, precision, thousands separators</td><td>Turns raw numbers into readable output</td><td align="center">●</td></tr>
<tr><td><b>07.8</b></td><td>Escape Sequences and Raw Strings</td><td><code>\n</code>, <code>\t</code>, <code>\\</code> and <code>r"raw"</code> strings</td><td>Essential for paths and regex patterns</td><td align="center">●</td></tr>
<tr><td><b>07.9</b></td><td>Unicode, Encoding, <code>bytes</code> vs <code>str</code></td><td>text vs bytes, and why encoding errors happen</td><td>The cause of most text-handling bugs</td><td align="center">●●●</td></tr>
<tr><td><b>07.10</b></td><td>String Concatenation Performance</td><td><code>join</code></td><td>Turns a slow loop into a fast one</td><td align="center">●</td></tr>
<tr><td><b>07.11</b></td><td><code>textwrap</code> and the <code>string</code> Module</td><td>wrapping paragraphs, and useful constants</td><td>Formatting help you would otherwise write</td><td align="center">●</td></tr>
</table>

### 08. Input, Output, and Basic I/O

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>08.1</b></td><td>`print</td><td>)` in Depth (sep, end, file, flush</td><td>Your first debugging tool</td><td align="center">●</td></tr>
<tr><td><b>08.2</b></td><td><code>input()</code> and Parsing User Input</td><td>reading input safely, and converting it</td><td>Input is text and is never trustworthy</td><td align="center">●</td></tr>
<tr><td><b>08.3</b></td><td>Command-Line Arguments</td><td><code>sys.argv</code></td><td>Makes scripts reusable without editing</td><td align="center">●</td></tr>
<tr><td><b>08.4</b></td><td>Formatted Console Output</td><td>aligning columns and building readable reports</td><td>Readable output saves the reader's time</td><td align="center">●</td></tr>
</table>

### 09. Control Flow — Conditionals

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>09.1</b></td><td><code>if</code> / <code>elif</code> / <code>else</code></td><td>branching on a condition</td><td>Without it a program cannot react</td><td align="center">●</td></tr>
<tr><td><b>09.2</b></td><td>Nested Conditionals</td><td>conditions inside conditions, and when to flatten them</td><td>Deep nesting is where logic bugs hide</td><td align="center">●</td></tr>
<tr><td><b>09.3</b></td><td>Conditional (Ternary) Expressions</td><td><code>value_if_true if condition else value_if_false</code></td><td>Removes four lines of noise</td><td align="center">●</td></tr>
<tr><td><b>09.4</b></td><td><code>match</code> Statement — Structural Pattern Matching</td><td>matching shapes, not just values</td><td>Far clearer than nested if-chains</td><td align="center">●</td></tr>
<tr><td><b>09.5</b></td><td>Guard Clauses and Readable Conditions</td><td>returning early to keep code flat and readable</td><td>Keeps functions flat and easy to follow</td><td align="center">●</td></tr>
</table>

### 10. Control Flow — Loops

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>10.1</b></td><td><code>while</code> Loops</td><td>repeating while a condition holds</td><td>For when you cannot count the steps</td><td align="center">●</td></tr>
<tr><td><b>10.2</b></td><td><code>for</code> Loops and Iterables</td><td>repeating once per item</td><td>The loop you will write most often</td><td align="center">●</td></tr>
<tr><td><b>10.3</b></td><td><code>range()</code> in Depth</td><td>start, stop, step, and why the stop is excluded</td><td>The off-by-one error's favourite home</td><td align="center">●</td></tr>
<tr><td><b>10.4</b></td><td><code>break</code>, <code>continue</code>, <code>pass</code></td><td>leaving early, skipping ahead, doing nothing</td><td>Exit early instead of adding flags</td><td align="center">●</td></tr>
<tr><td><b>10.5</b></td><td><code>else</code> Clause on Loops</td><td>the clause almost nobody knows about</td><td>The clean way to express search-and-fail</td><td align="center">●</td></tr>
<tr><td><b>10.6</b></td><td>Nested Loops</td><td>loops inside loops, and their cost</td><td>Needed for grids, tables and matrices</td><td align="center">●</td></tr>
<tr><td><b>10.7</b></td><td><code>enumerate()</code> and <code>zip()</code></td><td>looping with a counter, and looping over pairs</td><td>Removes manual index bookkeeping</td><td align="center">●</td></tr>
<tr><td><b>10.8</b></td><td>Infinite Loops and Loop Safety</td><td>how to avoid a program that never stops</td><td>Prevents a program that never finishes</td><td align="center">●</td></tr>
<tr><td><b>10.9</b></td><td>Loop Performance Notes</td><td>what makes a loop slow, and what to do about it</td><td>Small changes can mean large speedups</td><td align="center">●</td></tr>
</table>

### 11. Lists

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>11.1</b></td><td>Creating and Accessing Lists</td><td>creating, indexing, changing items</td><td>Python's default collection</td><td align="center">●●</td></tr>
<tr><td><b>11.2</b></td><td>Slicing</td><td>including step and negative indices</td><td>Extracts any part of a sequence</td><td align="center">●●</td></tr>
<tr><td><b>11.3</b></td><td>List Methods</td><td>complete</td><td>The everyday vocabulary of list work</td><td align="center">●●</td></tr>
<tr><td><b>11.4</b></td><td>Mutability and In-Place Operations</td><td>changing a list in place vs building a new one</td><td>Explains changes seen through another name</td><td align="center">●●</td></tr>
<tr><td><b>11.5</b></td><td>Sorting</td><td><code>sort</code> vs <code>sorted</code>, <code>key</code>, <code>reverse</code></td><td>Ordering data is a constant requirement</td><td align="center">●●</td></tr>
<tr><td><b>11.6</b></td><td>Nested Lists and Matrices</td><td>lists inside lists, and grids</td><td>How tables and grids are represented</td><td align="center">●●</td></tr>
<tr><td><b>11.7</b></td><td>Copying: Shallow vs Deep</td><td><code>copy</code> module</td><td>The bug that hits everyone once</td><td align="center">●●●</td></tr>
<tr><td><b>11.8</b></td><td>Lists as Stacks and Queues</td><td>last-in-first-out and first-in-first-out</td><td>Two core structures, no library needed</td><td align="center">●●</td></tr>
<tr><td><b>11.9</b></td><td>Common List Pitfalls</td><td>mutable default, <code>*</code> copy</td><td>The traps that produce silent wrong answers</td><td align="center">●●</td></tr>
</table>

### 12. Tuples

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>12.1</b></td><td>Creating Tuples and the Single-Element Trap</td><td>why <code>(5)</code> is not a tuple but <code>(5,)</code> is</td><td>A missing comma changes the type</td><td align="center">●●</td></tr>
<tr><td><b>12.2</b></td><td>Immutability and When to Use Tuples</td><td>fixed collections, and where they beat lists</td><td>Signals data that must not change</td><td align="center">●●</td></tr>
<tr><td><b>12.3</b></td><td>Tuple Methods and Operations</td><td><code>count</code>, <code>index</code>, concatenation, repetition</td><td>Small surface, quickly learned</td><td align="center">●●</td></tr>
<tr><td><b>12.4</b></td><td>Packing and Unpacking</td><td><code>point = 3, 4</code> and <code>x, y = point</code></td><td>Powers multiple return values</td><td align="center">●●</td></tr>
<tr><td><b>12.5</b></td><td>Extended Unpacking</td><td><code>*rest</code></td><td>Splits head from tail cleanly</td><td align="center">●●</td></tr>
<tr><td><b>12.6</b></td><td>Tuples as Dictionary Keys</td><td>why tuples can be keys but lists cannot</td><td>Enables compound dictionary keys</td><td align="center">●●</td></tr>
<tr><td><b>12.7</b></td><td><code>namedtuple</code> Preview</td><td>tuples with named fields</td><td>Readable fields without writing a class</td><td align="center">●●</td></tr>
</table>

### 13. Sets and Frozensets

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>13.1</b></td><td>Creating Sets, Uniqueness</td><td>unordered collections with no duplicates</td><td>Deduplicating in one operation</td><td align="center">●●</td></tr>
<tr><td><b>13.2</b></td><td>Set Methods</td><td><code>add</code>, <code>remove</code>, <code>discard</code>, <code>pop</code>, <code>update</code></td><td>The vocabulary of set work</td><td align="center">●●</td></tr>
<tr><td><b>13.3</b></td><td>Set Operations</td><td>union, intersection, difference, symmetric difference</td><td>Comparisons that would take nested loops</td><td align="center">●●</td></tr>
<tr><td><b>13.4</b></td><td>Subset / Superset / Disjoint</td><td>comparing one set against another</td><td>Answers containment questions directly</td><td align="center">●●</td></tr>
<tr><td><b>13.5</b></td><td><code>frozenset</code></td><td>the immutable set</td><td>Lets a set be used as a key</td><td align="center">●●</td></tr>
<tr><td><b>13.6</b></td><td>The Hashability Requirement</td><td>what can go in a set, and why</td><td>Explains why some values are rejected</td><td align="center">●●</td></tr>
<tr><td><b>13.7</b></td><td>Performance: Set vs List Lookup</td><td>why membership testing is dramatically faster</td><td>Thousands of times faster at scale</td><td align="center">●●</td></tr>
</table>

### 14. Dictionaries

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>14.1</b></td><td>Creating and Accessing Dictionaries</td><td>key-value pairs, lookup by key</td><td>The workhorse of real Python code</td><td align="center">●●</td></tr>
<tr><td><b>14.2</b></td><td>Dictionary Methods</td><td>complete</td><td>The vocabulary of dictionary work</td><td align="center">●●</td></tr>
<tr><td><b>14.3</b></td><td>Keys, Values, and Items Views</td><td>live views, and how they differ from lists</td><td>They update as the dictionary changes</td><td align="center">●●</td></tr>
<tr><td><b>14.4</b></td><td>Iterating Dictionaries</td><td>looping over keys, values, or both</td><td>How you process structured records</td><td align="center">●●</td></tr>
<tr><td><b>14.5</b></td><td>Nested Dictionaries</td><td>dictionaries inside dictionaries</td><td>The shape of JSON and API responses</td><td align="center">●●</td></tr>
<tr><td><b>14.6</b></td><td><code>get</code>, <code>setdefault</code>, <code>pop</code>, and Missing Keys</td><td>handling a key that might not be there</td><td>Avoids the most common `KeyError`</td><td align="center">●●</td></tr>
<tr><td><b>14.7</b></td><td>Merging Dicts</td><td><code>|</code>, <code>update</code>, <code>**</code> — three ways to combine</td><td>Combining configuration and defaults</td><td align="center">●●</td></tr>
<tr><td><b>14.8</b></td><td>Dict Ordering Guarantees</td><td>insertion order, guaranteed since 3.7</td><td>Output order you can rely on</td><td align="center">●●</td></tr>
<tr><td><b>14.9</b></td><td>Hashing and Key Requirements</td><td>what makes a valid key</td><td>Explains why a key is rejected</td><td align="center">●●●</td></tr>
<tr><td><b>14.10</b></td><td>Dict Performance</td><td>why lookup is fast no matter how big it gets</td><td>Constant time, no matter the size</td><td align="center">●●</td></tr>
</table>

### 15. Comprehensions

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>15.1</b></td><td>List Comprehensions</td><td>building a list in one readable line</td><td>Replaces three lines with one clear one</td><td align="center">●●</td></tr>
<tr><td><b>15.2</b></td><td>Conditional Comprehensions</td><td>filtering while you build</td><td>Select and transform in one pass</td><td align="center">●●</td></tr>
<tr><td><b>15.3</b></td><td>Nested Comprehensions</td><td>comprehensions inside comprehensions, and their limits</td><td>Flattening nested data</td><td align="center">●●</td></tr>
<tr><td><b>15.4</b></td><td>Dict Comprehensions</td><td>building dictionaries the same way</td><td>Building lookups from raw data</td><td align="center">●●</td></tr>
<tr><td><b>15.5</b></td><td>Set Comprehensions</td><td>building sets the same way</td><td>Deduplicating while transforming</td><td align="center">●●</td></tr>
<tr><td><b>15.6</b></td><td>Generator Expressions</td><td>the lazy version that does not build a list</td><td>Handles data too large for memory</td><td align="center">●●</td></tr>
<tr><td><b>15.7</b></td><td>Readability Limits — When Not to Use Them</td><td>when a plain loop is the better choice</td><td>Knowing when the loop is clearer</td><td align="center">●●</td></tr>
</table>

### 16. Functions — Fundamentals

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>16.1</b></td><td>Defining and Calling Functions</td><td><code>def</code>, arguments, calling</td><td>How you stop repeating yourself</td><td align="center">●●</td></tr>
<tr><td><b>16.2</b></td><td>Positional Arguments</td><td>arguments matched by position</td><td>The simplest way to pass data in</td><td align="center">●●</td></tr>
<tr><td><b>16.3</b></td><td>Keyword Arguments</td><td>arguments matched by name</td><td>Makes call sites self-documenting</td><td align="center">●●</td></tr>
<tr><td><b>16.4</b></td><td>Default Parameters and the Mutable Default Trap</td><td>the classic bug that catches everyone once</td><td>The bug that surprises every newcomer</td><td align="center">●●●</td></tr>
<tr><td><b>16.5</b></td><td><code>*args</code> and <code>**kwargs</code></td><td>accepting any number of arguments</td><td>Writing flexible wrappers and decorators</td><td align="center">●●</td></tr>
<tr><td><b>16.6</b></td><td>Positional-Only (<code>/</code>) and Keyword-Only (<code>*</code>) Parameters</td><td>controlling how your function may be called</td><td>Lets you rename parameters safely later</td><td align="center">●●</td></tr>
<tr><td><b>16.7</b></td><td>Return Values and Multiple Returns</td><td><code>return</code>, returning several values at once</td><td>How work gets back to the caller</td><td align="center">●●</td></tr>
<tr><td><b>16.8</b></td><td>Docstrings</td><td>PEP 257</td><td>Documentation that tooling can read</td><td align="center">●●</td></tr>
<tr><td><b>16.9</b></td><td>Functions as First-Class Objects</td><td>passing functions around like any other value</td><td>The basis of callbacks and decorators</td><td align="center">●●</td></tr>
</table>

### 17. Functions — Scope and Advanced

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>17.1</b></td><td>Scope and the LEGB Rule</td><td>local, enclosing, global, built-in</td><td>Explains most `NameError` surprises</td><td align="center">●●</td></tr>
<tr><td><b>17.2</b></td><td><code>global</code> and <code>nonlocal</code></td><td>reaching outward to reassign a name</td><td>Needed for counters and accumulators</td><td align="center">●●</td></tr>
<tr><td><b>17.3</b></td><td>Closures</td><td>functions that remember where they came from</td><td>The machinery behind decorators</td><td align="center">●●●</td></tr>
<tr><td><b>17.4</b></td><td>Lambda Functions</td><td>small anonymous functions</td><td>Ideal for sort keys and short callbacks</td><td align="center">●●</td></tr>
<tr><td><b>17.5</b></td><td>Recursion and Recursion Limits</td><td>functions that call themselves, and when to stop</td><td>Natural fit for trees and nested data</td><td align="center">●●</td></tr>
<tr><td><b>17.6</b></td><td>Higher-Order Functions</td><td><code>map</code>, <code>filter</code>, <code>reduce</code></td><td>Transform collections without a loop</td><td align="center">●●</td></tr>
<tr><td><b>17.7</b></td><td><code>functools</code></td><td><code>partial</code>, <code>lru_cache</code>, <code>wraps</code>, <code>reduce</code></td><td>Caching alone can transform performance</td><td align="center">●●</td></tr>
<tr><td><b>17.8</b></td><td>Pure Functions and Side Effects</td><td>why predictable functions are easier to trust</td><td>Easier to test and to reason about</td><td align="center">●●</td></tr>
<tr><td><b>17.9</b></td><td>Function Annotations / Type Hints</td><td>documenting the types a function expects</td><td>Catches whole classes of bug early</td><td align="center">●●</td></tr>
</table>

### 18. Decorators

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>18.1</b></td><td>Decorator Theory</td><td>wrapping a function to add behaviour</td><td>Used by every major Python framework</td><td align="center">●●</td></tr>
<tr><td><b>18.2</b></td><td>Writing Simple Decorators</td><td>your first working decorator</td><td>Cross-cutting behaviour in one place</td><td align="center">●●</td></tr>
<tr><td><b>18.3</b></td><td>Decorators with Arguments</td><td>decorators you can configure</td><td>Reusable, configurable behaviour</td><td align="center">●●</td></tr>
<tr><td><b>18.4</b></td><td><code>functools.wraps</code></td><td>keeping the wrapped function's identity</td><td>Without it, debugging becomes confusing</td><td align="center">●●</td></tr>
<tr><td><b>18.5</b></td><td>Stacking Decorators</td><td>applying several at once, and the order they run</td><td>Order changes the result</td><td align="center">●●</td></tr>
<tr><td><b>18.6</b></td><td>Class Decorators</td><td>decorating a class instead of a function</td><td>Register or extend classes automatically</td><td align="center">●●</td></tr>
<tr><td><b>18.7</b></td><td>Practical Decorators</td><td>timing, retry, logging, caching</td><td>Patterns you will genuinely reuse</td><td align="center">●●</td></tr>
</table>

### 19. Iterators and Generators

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>19.1</b></td><td>Iterable vs Iterator Protocol</td><td>the difference, and why it matters</td><td>Explains what `for` really requires</td><td align="center">●●</td></tr>
<tr><td><b>19.2</b></td><td><code>iter()</code> and <code>next()</code></td><td>the two functions behind every <code>for</code> loop</td><td>The protocol behind every loop</td><td align="center">●●</td></tr>
<tr><td><b>19.3</b></td><td>Building Custom Iterators</td><td>writing your own</td><td>Make your own objects loopable</td><td align="center">●●</td></tr>
<tr><td><b>19.4</b></td><td>Generators and <code>yield</code></td><td>pausing and resuming a function</td><td>Huge memory savings for little effort</td><td align="center">●●</td></tr>
<tr><td><b>19.5</b></td><td>Generator Expressions</td><td>generators without the <code>def</code></td><td>Lazy evaluation with no extra syntax</td><td align="center">●●</td></tr>
<tr><td><b>19.6</b></td><td><code>yield from</code></td><td>delegating to another generator</td><td>Composing generators cleanly</td><td align="center">●●</td></tr>
<tr><td><b>19.7</b></td><td>Sending Values into Generators</td><td><code>send</code>, <code>throw</code>, <code>close</code></td><td>Two-way communication with a generator</td><td align="center">●●●</td></tr>
<tr><td><b>19.8</b></td><td>Lazy Evaluation and Memory Benefits</td><td>handling data too big to fit in memory</td><td>Process files larger than your RAM</td><td align="center">●●</td></tr>
<tr><td><b>19.9</b></td><td><code>itertools</code> Complete Tour</td><td>chaining, grouping, combining, cycling</td><td>Solves problems you would hand-roll badly</td><td align="center">●●</td></tr>
</table>

### 20. Modules and Packages

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>20.1</b></td><td>What is a Module</td><td>one file, importable from another</td><td>How code grows past one file</td><td align="center">●●</td></tr>
<tr><td><b>20.2</b></td><td><code>import</code> Forms and Aliasing</td><td><code>import x</code>, <code>from x import y</code>, <code>as</code></td><td>Bad imports cause name collisions</td><td align="center">●●</td></tr>
<tr><td><b>20.3</b></td><td>Module Search Path</td><td><code>sys.path</code></td><td>Explains most `ModuleNotFoundError` cases</td><td align="center">●●</td></tr>
<tr><td><b>20.4</b></td><td><code>if __name__ == "__main__"</code></td><td>running a file vs importing it</td><td>Stops code running on import</td><td align="center">●●</td></tr>
<tr><td><b>20.5</b></td><td>Creating Packages and <code>__init__.py</code></td><td>turning a folder into an importable package</td><td>How real projects are organised</td><td align="center">●●</td></tr>
<tr><td><b>20.6</b></td><td>Relative vs Absolute Imports</td><td><code>from .sibling import x</code> vs <code>from package.module import x</code></td><td>Choosing wrong breaks on refactor</td><td align="center">●●</td></tr>
<tr><td><b>20.7</b></td><td>Namespace Packages</td><td>packages without an <code>__init__.py</code></td><td>Splitting a package across directories</td><td align="center">●●</td></tr>
<tr><td><b>20.8</b></td><td>Circular Imports and How to Avoid Them</td><td>why they happen, and how to restructure</td><td>A common failure in growing projects</td><td align="center">●●●</td></tr>
<tr><td><b>20.9</b></td><td>Reloading Modules</td><td>re-importing without restarting</td><td>Useful in notebooks and long sessions</td><td align="center">●●</td></tr>
<tr><td><b>20.10</b></td><td><code>__all__</code> and the Public API</td><td>controlling what <code>from x import *</code> exposes</td><td>Defines what your package promises</td><td align="center">●●</td></tr>
</table>

### 21. Standard Library Tour

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>21.1</b></td><td><code>os</code> and <code>sys</code></td><td>environment, paths, arguments, the interpreter itself</td><td>Interacting with the world outside Python</td><td align="center">●●</td></tr>
<tr><td><b>21.2</b></td><td><code>pathlib</code></td><td>the modern way to handle file paths</td><td>Replaces fragile string path juggling</td><td align="center">●●</td></tr>
<tr><td><b>21.3</b></td><td><code>datetime</code>, <code>time</code>, <code>zoneinfo</code></td><td>dates, times, durations, time zones</td><td>Time zone bugs are notoriously costly</td><td align="center">●●</td></tr>
<tr><td><b>21.4</b></td><td><code>random</code> and <code>secrets</code></td><td>random for simulations, secrets for security</td><td>Using the wrong one is a security flaw</td><td align="center">●●</td></tr>
<tr><td><b>21.5</b></td><td><code>collections</code></td><td><code>Counter</code>, <code>defaultdict</code>, <code>deque</code>, <code>OrderedDict</code>, <code>namedtuple</code>, <code>ChainMap</code></td><td>Removes boilerplate you would write daily</td><td align="center">●●</td></tr>
<tr><td><b>21.6</b></td><td><code>json</code>, <code>csv</code>, <code>pickle</code></td><td>the three formats you will use constantly</td><td>The formats data actually arrives in</td><td align="center">●●</td></tr>
<tr><td><b>21.7</b></td><td><code>re</code> Preview</td><td>a first look before the full chapter</td><td>Enough to recognise when to use it</td><td align="center">●●</td></tr>
<tr><td><b>21.8</b></td><td><code>argparse</code></td><td>building real command-line tools</td><td>Turns a script into a usable tool</td><td align="center">●●</td></tr>
<tr><td><b>21.9</b></td><td><code>logging</code></td><td>recording what your program did</td><td>`print` does not scale to real systems</td><td align="center">●●</td></tr>
<tr><td><b>21.10</b></td><td><code>subprocess</code></td><td>running other programs from Python</td><td>Automating tools you already have</td><td align="center">●●</td></tr>
<tr><td><b>21.11</b></td><td><code>shutil</code>, <code>glob</code>, <code>tempfile</code></td><td>copying, finding, and scratch files</td><td>Everyday file chores, already solved</td><td align="center">●●</td></tr>
<tr><td><b>21.12</b></td><td><code>statistics</code>, <code>enum</code>, <code>uuid</code>, <code>hashlib</code></td><td>averages, constants, unique ids, hashing</td><td>Small modules with big time savings</td><td align="center">●●</td></tr>
</table>

### 22. File Handling

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>22.1</b></td><td>Opening and Closing Files, File Modes</td><td><code>r</code>, <code>w</code>, <code>a</code>, <code>x</code>, <code>b</code>, <code>+</code></td><td>The wrong mode can erase your data</td><td align="center">●●</td></tr>
<tr><td><b>22.2</b></td><td>Reading Files</td><td><code>read</code>, <code>readline</code>, <code>readlines</code>, iteration</td><td>Choosing wrong can exhaust memory</td><td align="center">●●</td></tr>
<tr><td><b>22.3</b></td><td>Writing and Appending</td><td>creating files and adding to them</td><td>How programs produce lasting output</td><td align="center">●●</td></tr>
<tr><td><b>22.4</b></td><td>Context Managers</td><td><code>with</code></td><td>Guarantees cleanup even on error</td><td align="center">●●</td></tr>
<tr><td><b>22.5</b></td><td>Binary Files</td><td>working with bytes instead of text</td><td>Images, archives and network data</td><td align="center">●●</td></tr>
<tr><td><b>22.6</b></td><td>Encodings and <code>newline</code></td><td>getting text right across platforms</td><td>The cause of most cross-platform text bugs</td><td align="center">●●</td></tr>
<tr><td><b>22.7</b></td><td>File Positions</td><td><code>seek</code>, <code>tell</code></td><td>Needed for large or structured files</td><td align="center">●●</td></tr>
<tr><td><b>22.8</b></td><td><code>os</code> and <code>pathlib</code> File Operations</td><td>creating, moving, renaming, deleting</td><td>Automating file management safely</td><td align="center">●●</td></tr>
<tr><td><b>22.9</b></td><td>Working with CSV</td><td>reading and writing spreadsheet data</td><td>The universal data exchange format</td><td align="center">●●</td></tr>
<tr><td><b>22.10</b></td><td>Working with JSON</td><td>reading and writing structured data</td><td>The language of web APIs</td><td align="center">●●</td></tr>
<tr><td><b>22.11</b></td><td>Serialization: <code>pickle</code></td><td>saving Python objects, and why it is risky</td><td>Convenient, but unsafe with untrusted data</td><td align="center">●●</td></tr>
<tr><td><b>22.12</b></td><td>Temporary Files and Directories</td><td>scratch space that cleans itself up</td><td>Safe scratch space, cleaned up for you</td><td align="center">●●</td></tr>
</table>

### 23. Error Handling and Exceptions

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>23.1</b></td><td>Errors vs Exceptions</td><td>theory</td><td>Separates typos from expected failures</td><td align="center">●●</td></tr>
<tr><td><b>23.2</b></td><td>The Exception Hierarchy</td><td>what inherits from what, and why you care</td><td>Lets you catch at the right level</td><td align="center">●●</td></tr>
<tr><td><b>23.3</b></td><td><code>try</code> / <code>except</code></td><td>catching what goes wrong</td><td>The difference between a crash and a message</td><td align="center">●●</td></tr>
<tr><td><b>23.4</b></td><td>Multiple and Grouped Excepts</td><td>handling several failure modes</td><td>Different failures need different responses</td><td align="center">●●</td></tr>
<tr><td><b>23.5</b></td><td><code>else</code> and <code>finally</code></td><td>the two clauses people forget</td><td>Guarantees cleanup runs</td><td align="center">●●</td></tr>
<tr><td><b>23.6</b></td><td><code>raise</code> and Re-Raising</td><td>raising your own, and passing one along</td><td>Signalling failure from your own code</td><td align="center">●●</td></tr>
<tr><td><b>23.7</b></td><td>Exception Chaining</td><td><code>from</code></td><td>Preserves the original cause</td><td align="center">●●</td></tr>
<tr><td><b>23.8</b></td><td>Custom Exception Classes</td><td>errors that describe your own problem domain</td><td>Callers can catch exactly what you mean</td><td align="center">●●</td></tr>
<tr><td><b>23.9</b></td><td><code>assert</code> and Assertions</td><td>checking assumptions during development</td><td>Documents assumptions and checks them</td><td align="center">●●</td></tr>
<tr><td><b>23.10</b></td><td>Exception Groups and <code>except*</code></td><td>handling several errors at once</td><td>Needed for concurrent and grouped failures</td><td align="center">●●</td></tr>
<tr><td><b>23.11</b></td><td>EAFP vs LBYL</td><td>ask forgiveness, or ask permission</td><td>Shapes how Python code is written</td><td align="center">●●</td></tr>
<tr><td><b>23.12</b></td><td>Best Practices and Anti-Patterns</td><td>what to catch, what to let through</td><td>A swallowed error is worse than a crash</td><td align="center">●●</td></tr>
</table>

### 24. OOP — Fundamentals

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>24.1</b></td><td>OOP Theory</td><td>objects, classes, abstraction</td><td>Manage complexity as programs grow</td><td align="center">●●</td></tr>
<tr><td><b>24.2</b></td><td>Defining Classes, Creating Instances</td><td><code>class</code>, instances, the basics</td><td>How you define a new type</td><td align="center">●●</td></tr>
<tr><td><b>24.3</b></td><td>Instance Attributes and <code>self</code></td><td>data that belongs to one object</td><td>Gives each object its own state</td><td align="center">●●</td></tr>
<tr><td><b>24.4</b></td><td>The <code>__init__</code> Constructor</td><td>setting an object up when it is created</td><td>Guarantees objects start valid</td><td align="center">●●</td></tr>
<tr><td><b>24.5</b></td><td>Class Attributes vs Instance Attributes</td><td>shared by all, vs owned by one</td><td>Mixing them up causes shared-state bugs</td><td align="center">●●</td></tr>
<tr><td><b>24.6</b></td><td>Instance Methods</td><td>functions that belong to an object</td><td>Behaviour that belongs with its data</td><td align="center">●●</td></tr>
<tr><td><b>24.7</b></td><td>Class Methods and <code>@classmethod</code></td><td>methods that work on the class itself</td><td>The standard alternative constructor pattern</td><td align="center">●●</td></tr>
<tr><td><b>24.8</b></td><td>Static Methods and <code>@staticmethod</code></td><td>methods that need neither instance nor class</td><td>Groups related helpers with the class</td><td align="center">●●</td></tr>
<tr><td><b>24.9</b></td><td><code>__del__</code> and Object Lifecycle</td><td>creation, use, and cleanup</td><td>Explains when cleanup actually happens</td><td align="center">●●</td></tr>
</table>

### 25. OOP — Encapsulation and Properties

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>25.1</b></td><td>Public, Protected, and Private Conventions</td><td><code>name</code>, <code>_name</code>, <code>__name</code></td><td>Signals what is safe to depend on</td><td align="center">●●</td></tr>
<tr><td><b>25.2</b></td><td>Name Mangling</td><td>what <code>__name</code> actually does</td><td>Explains a surprising attribute error</td><td align="center">●●</td></tr>
<tr><td><b>25.3</b></td><td>Getters and Setters</td><td>controlling access to an attribute</td><td>Validate before a bad value is stored</td><td align="center">●●</td></tr>
<tr><td><b>25.4</b></td><td>The <code>@property</code> Decorator</td><td>methods that look like plain attributes</td><td>Add validation without breaking callers</td><td align="center">●●</td></tr>
<tr><td><b>25.5</b></td><td>Computed Attributes</td><td>values worked out on demand</td><td>Never store what you can derive</td><td align="center">●●</td></tr>
<tr><td><b>25.6</b></td><td><code>__slots__</code></td><td>trading flexibility for memory</td><td>Large savings when objects number millions</td><td align="center">●●</td></tr>
</table>

### 26. OOP — Inheritance and Polymorphism

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>26.1</b></td><td>Single Inheritance</td><td>one class building on another</td><td>Share behaviour without copying code</td><td align="center">●●</td></tr>
<tr><td><b>26.2</b></td><td><code>super()</code> in Depth</td><td>calling up to the parent, correctly</td><td>Calling the parent wrongly is a classic bug</td><td align="center">●●</td></tr>
<tr><td><b>26.3</b></td><td>Method Overriding</td><td>replacing a parent's behaviour</td><td>Specialise behaviour for a subclass</td><td align="center">●●</td></tr>
<tr><td><b>26.4</b></td><td>Multiple Inheritance</td><td>inheriting from several classes at once</td><td>Powerful, and easy to misuse</td><td align="center">●●</td></tr>
<tr><td><b>26.5</b></td><td>Method Resolution Order (MRO) and C3 Linearization</td><td>the rule that decides which method wins</td><td>Explains which method actually runs</td><td align="center">●●●</td></tr>
<tr><td><b>26.6</b></td><td>Mixins</td><td>small reusable behaviour, added by inheritance</td><td>Compose features without deep hierarchies</td><td align="center">●●</td></tr>
<tr><td><b>26.7</b></td><td>Polymorphism and Duck Typing</td><td>if it quacks, it is a duck</td><td>Why Python needs fewer interfaces</td><td align="center">●●</td></tr>
<tr><td><b>26.8</b></td><td><code>isinstance</code> vs <code>type</code> vs Duck Typing</td><td>three ways to ask what something is</td><td>Choosing wrong breaks subclasses</td><td align="center">●●</td></tr>
<tr><td><b>26.9</b></td><td>Composition vs Inheritance</td><td>has-a, or is-a</td><td>Usually the better default</td><td align="center">●●</td></tr>
</table>

### 27. OOP — Magic Methods

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>27.1</b></td><td><code>__str__</code> vs <code>__repr__</code></td><td>friendly text, and unambiguous text</td><td>Makes debugging output actually useful</td><td align="center">●●</td></tr>
<tr><td><b>27.2</b></td><td>Comparison Dunders</td><td><code>__eq__</code>, <code>__lt__</code>, …</td><td>Enables sorting and equality tests</td><td align="center">●●</td></tr>
<tr><td><b>27.3</b></td><td><code>__hash__</code> and the Hashability Contract</td><td>making your objects usable as keys</td><td>Get this wrong and dictionaries misbehave</td><td align="center">●●</td></tr>
<tr><td><b>27.4</b></td><td>Arithmetic Operator Overloading</td><td>making <code>+</code>, <code>-</code>, <code>*</code> work on your own types</td><td>Natural syntax for numeric types</td><td align="center">●●</td></tr>
<tr><td><b>27.5</b></td><td>Container Dunders</td><td><code>__len__</code>, <code>__getitem__</code>, <code>__contains__</code>, <code>__iter__</code></td><td>Your class works with `len`, `in` and `for`</td><td align="center">●●</td></tr>
<tr><td><b>27.6</b></td><td>Callable Objects</td><td><code>__call__</code></td><td>Objects that carry state between calls</td><td align="center">●●</td></tr>
<tr><td><b>27.7</b></td><td>Attribute Access</td><td><code>__getattr__</code>, <code>__setattr__</code>, <code>__getattribute__</code></td><td>Powers proxies and lazy loading</td><td align="center">●●</td></tr>
<tr><td><b>27.8</b></td><td>The Context Manager Protocol</td><td><code>__enter__</code>, <code>__exit__</code></td><td>Your own resources work with `with`</td><td align="center">●●</td></tr>
<tr><td><b>27.9</b></td><td><code>__new__</code> vs <code>__init__</code></td><td>creating an object, vs setting it up</td><td>Needed for immutable types and singletons</td><td align="center">●●●</td></tr>
<tr><td><b>27.10</b></td><td>Complete Dunder Reference</td><td>the full list, in one place</td><td>One place to look it all up</td><td align="center">●●</td></tr>
</table>

### 28. OOP — Advanced

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>28.1</b></td><td>Abstract Base Classes</td><td><code>abc</code></td><td>Enforces a contract on subclasses</td><td align="center">●●</td></tr>
<tr><td><b>28.2</b></td><td>Protocols and Structural Typing</td><td>typing by shape, not by inheritance</td><td>Type safety without inheritance</td><td align="center">●●</td></tr>
<tr><td><b>28.3</b></td><td><code>dataclasses</code> Complete</td><td>classes that write their own boilerplate</td><td>Removes dozens of lines of boilerplate</td><td align="center">●●</td></tr>
<tr><td><b>28.4</b></td><td><code>enum</code> Complete</td><td>fixed sets of named values</td><td>Replaces magic strings and numbers</td><td align="center">●●</td></tr>
<tr><td><b>28.5</b></td><td><code>NamedTuple</code> and <code>TypedDict</code></td><td>typed records and typed dictionaries</td><td>Typed records and typed JSON shapes</td><td align="center">●●</td></tr>
<tr><td><b>28.6</b></td><td>Descriptors</td><td>the machinery behind <code>@property</code></td><td>Reusable attribute behaviour</td><td align="center">●●●</td></tr>
<tr><td><b>28.7</b></td><td>Metaclasses</td><td>classes that build classes</td><td>Used by ORMs and frameworks</td><td align="center">●●●</td></tr>
<tr><td><b>28.8</b></td><td>Class Creation Hooks</td><td><code>__init_subclass__</code>, <code>__set_name__</code></td><td>Cleaner than reaching for a metaclass</td><td align="center">●●</td></tr>
<tr><td><b>28.9</b></td><td>Design Patterns in Python</td><td>singleton, factory, observer, strategy</td><td>Named solutions to recurring problems</td><td align="center">●●</td></tr>
<tr><td><b>28.10</b></td><td>SOLID Principles in Python</td><td>five design principles, with Python examples</td><td>Keeps large codebases changeable</td><td align="center">●●</td></tr>
</table>

### 29. Context Managers

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>29.1</b></td><td><code>with</code> Statement Theory</td><td>why <code>with</code> exists</td><td>Leaked resources are a real production risk</td><td align="center">●●</td></tr>
<tr><td><b>29.2</b></td><td>Class-Based Context Managers</td><td><code>__enter__</code> and <code>__exit__</code></td><td>Full control over setup and cleanup</td><td align="center">●●</td></tr>
<tr><td><b>29.3</b></td><td><code>contextlib.contextmanager</code></td><td>the decorator that turns a generator into one</td><td>A context manager in a few lines</td><td align="center">●●</td></tr>
<tr><td><b>29.4</b></td><td><code>contextlib</code> Utilities</td><td><code>suppress</code>, <code>closing</code>, <code>ExitStack</code></td><td>Solves problems you would hand-roll</td><td align="center">●●</td></tr>
<tr><td><b>29.5</b></td><td>Multiple Context Managers</td><td>managing several resources at once</td><td>Cleanly handling several resources</td><td align="center">●●</td></tr>
<tr><td><b>29.6</b></td><td>Async Context Managers Preview</td><td><code>async with</code>, previewing Chapter 35</td><td>Required for async resources</td><td align="center">●●</td></tr>
</table>

### 30. Regular Expressions

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>30.1</b></td><td>Regex Theory and Syntax</td><td>what a pattern is, and how matching works</td><td>Text problems that loops handle badly</td><td align="center">●●</td></tr>
<tr><td><b>30.2</b></td><td>Character Classes and Quantifiers</td><td><code>\d</code>, <code>\w</code>, <code>[a-z]</code>, <code>*</code>, <code>+</code>, <code>?</code>, <code>{n,m}</code></td><td>The core of every pattern you write</td><td align="center">●●</td></tr>
<tr><td><b>30.3</b></td><td>Anchors and Boundaries</td><td><code>^</code>, <code>$</code>, <code>\b</code></td><td>Prevents accidental partial matches</td><td align="center">●●</td></tr>
<tr><td><b>30.4</b></td><td>Groups and Capturing</td><td>pulling pieces out of a match</td><td>Extracting data, not just finding it</td><td align="center">●●</td></tr>
<tr><td><b>30.5</b></td><td>Named Groups, Lookahead, Lookbehind</td><td>readable groups, and matching by context</td><td>Patterns you can still read next year</td><td align="center">●●</td></tr>
<tr><td><b>30.6</b></td><td><code>re</code> Module Functions</td><td><code>match</code>, <code>search</code>, <code>findall</code>, <code>finditer</code>, <code>sub</code></td><td>Choosing wrong gives confusing results</td><td align="center">●●</td></tr>
<tr><td><b>30.7</b></td><td>Flags</td><td>case-insensitive, multiline, verbose</td><td>Handles multiline and case-insensitive text</td><td align="center">●●</td></tr>
<tr><td><b>30.8</b></td><td>Substitution and Splitting</td><td>find and replace, and splitting on a pattern</td><td>Transforming text, not just matching</td><td align="center">●●</td></tr>
<tr><td><b>30.9</b></td><td>Greedy vs Lazy, Catastrophic Backtracking</td><td>how a regex can hang your program</td><td>A bad pattern can hang your server</td><td align="center">●●●</td></tr>
<tr><td><b>30.10</b></td><td>Practical Patterns</td><td>emails, dates, log lines, and how to test them</td><td>Tested patterns you can reuse safely</td><td align="center">●●</td></tr>
</table>

### 31. Functional Programming

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>31.1</b></td><td>Functional Concepts in Python</td><td>what transfers from functional languages, and what does not</td><td>Fewer moving parts, fewer bugs</td><td align="center">●●</td></tr>
<tr><td><b>31.2</b></td><td>Immutability Practices</td><td>working without changing state</td><td>Removes a whole category of bug</td><td align="center">●●</td></tr>
<tr><td><b>31.3</b></td><td><code>map</code>, <code>filter</code>, <code>reduce</code> Deep Dive</td><td>the three classic transformations</td><td>Express transformations directly</td><td align="center">●●</td></tr>
<tr><td><b>31.4</b></td><td>Function Composition</td><td>building big functions out of small ones</td><td>Build pipelines from small pieces</td><td align="center">●●</td></tr>
<tr><td><b>31.5</b></td><td>Currying and Partial Application</td><td>fixing some arguments now, the rest later</td><td>Adapt a function without rewriting it</td><td align="center">●●</td></tr>
<tr><td><b>31.6</b></td><td>The <code>operator</code> Module</td><td>operators as functions you can pass around</td><td>Cleaner than a lambda for simple cases</td><td align="center">●●</td></tr>
<tr><td><b>31.7</b></td><td>Limits of FP in Python</td><td>why Python is not Haskell, and why that is fine</td><td>Knowing when to stop being clever</td><td align="center">●●</td></tr>
</table>

### 32. Type Hints and Static Typing

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>32.1</b></td><td>Why Type Hints</td><td>catching bugs before you run the code</td><td>Catches bugs before the code runs</td><td align="center">●●</td></tr>
<tr><td><b>32.2</b></td><td>Basic Annotations</td><td>annotating arguments, returns, and variables</td><td>Documentation your editor understands</td><td align="center">●●</td></tr>
<tr><td><b>32.3</b></td><td><code>typing</code> Module Core</td><td><code>Optional</code>, <code>Union</code>, <code>Any</code>, <code>Literal</code></td><td>Covers most real annotations</td><td align="center">●●</td></tr>
<tr><td><b>32.4</b></td><td>Generics and <code>TypeVar</code></td><td>types that work with any contained type</td><td>Reusable code that stays type-safe</td><td align="center">●●</td></tr>
<tr><td><b>32.5</b></td><td>Modern Syntax</td><td><code>list[int]</code> and <code>X | Y</code>, replacing <code>List</code> and <code>Union</code></td><td>Shorter, and what new code uses</td><td align="center">●●</td></tr>
<tr><td><b>32.6</b></td><td><code>Callable</code>, <code>Protocol</code>, <code>Self</code></td><td>typing functions, shapes, and returns</td><td>Typing callbacks and fluent interfaces</td><td align="center">●●</td></tr>
<tr><td><b>32.7</b></td><td>Using <code>mypy</code></td><td>running a type checker over your code</td><td>Where hints actually become checks</td><td align="center">●●</td></tr>
<tr><td><b>32.8</b></td><td>Runtime Type Checking and Its Limits</td><td>what type hints do not do</td><td>Hints do not enforce anything at runtime</td><td align="center">●●</td></tr>
</table>

### 33. Concurrency — Threading

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>33.1</b></td><td>Concurrency vs Parallelism</td><td>theory</td><td>Confusing them leads to the wrong tool</td><td align="center">●●●</td></tr>
<tr><td><b>33.2</b></td><td>Processes vs Threads</td><td>the real difference, and when each applies</td><td>Decides cost, isolation and speed</td><td align="center">●●●</td></tr>
<tr><td><b>33.3</b></td><td>The GIL Explained</td><td>why threads do not speed up CPU work</td><td>Explains why threads fail to speed things up</td><td align="center">●●●</td></tr>
<tr><td><b>33.4</b></td><td>The <code>threading</code> Module</td><td>starting, joining, and managing threads</td><td>Overlap waiting time instead of adding it</td><td align="center">●●●</td></tr>
<tr><td><b>33.5</b></td><td>Locks, RLocks, Semaphores, Events</td><td>coordinating threads safely</td><td>Without them, shared data corrupts silently</td><td align="center">●●●</td></tr>
<tr><td><b>33.6</b></td><td>Race Conditions and Deadlocks</td><td>the two classic threading bugs</td><td>The bugs that appear only under load</td><td align="center">●●●</td></tr>
<tr><td><b>33.7</b></td><td><code>queue</code> for Thread Communication</td><td>passing work between threads safely</td><td>Safe hand-off without manual locking</td><td align="center">●●●</td></tr>
<tr><td><b>33.8</b></td><td><code>concurrent.futures.ThreadPoolExecutor</code></td><td>the high-level way to run threads</td><td>Less code and fewer mistakes</td><td align="center">●●●</td></tr>
</table>

### 34. Concurrency — Multiprocessing

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>34.1</b></td><td>The <code>multiprocessing</code> Module</td><td>true parallelism, at a cost</td><td>The way to actually use every core</td><td align="center">●●●</td></tr>
<tr><td><b>34.2</b></td><td>Process Pools</td><td>spreading work across CPU cores</td><td>Parallel work in a few lines</td><td align="center">●●●</td></tr>
<tr><td><b>34.3</b></td><td>Inter-Process Communication</td><td>Pipes, Queues</td><td>Processes cannot share memory directly</td><td align="center">●●●</td></tr>
<tr><td><b>34.4</b></td><td>Shared Memory</td><td>sharing memory instead of copying</td><td>Avoids copying large datasets</td><td align="center">●●●</td></tr>
<tr><td><b>34.5</b></td><td><code>ProcessPoolExecutor</code></td><td>the high-level way to run processes</td><td>One interface for threads or processes</td><td align="center">●●●</td></tr>
<tr><td><b>34.6</b></td><td>Choosing Threads vs Processes vs Async</td><td>a decision guide you can actually use</td><td>The decision that determines performance</td><td align="center">●●●</td></tr>
</table>

### 35. Asynchronous Programming

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>35.1</b></td><td>Async Theory and the Event Loop</td><td>how one thread does many things at once</td><td>Explains why async is not threads</td><td align="center">●●●</td></tr>
<tr><td><b>35.2</b></td><td><code>async</code> / <code>await</code> Syntax</td><td>the two keywords that drive it all</td><td>The whole model rests on these two words</td><td align="center">●●●</td></tr>
<tr><td><b>35.3</b></td><td>Coroutines and Tasks</td><td>scheduling work, and waiting for it</td><td>Running work concurrently, not just later</td><td align="center">●●●</td></tr>
<tr><td><b>35.4</b></td><td><code>asyncio.gather</code>, <code>wait</code>, <code>TaskGroup</code></td><td>running many things concurrently</td><td>Thousands of requests from one thread</td><td align="center">●●●</td></tr>
<tr><td><b>35.5</b></td><td>Async Iterators and Generators</td><td><code>async for</code> and <code>yield</code> together</td><td>Streaming data as it arrives</td><td align="center">●●●</td></tr>
<tr><td><b>35.6</b></td><td>Async Context Managers</td><td><code>async with</code></td><td>Async connections still need cleanup</td><td align="center">●●●</td></tr>
<tr><td><b>35.7</b></td><td>Timeouts and Cancellation</td><td>giving up on work that takes too long</td><td>Prevents one slow call hanging everything</td><td align="center">●●●</td></tr>
<tr><td><b>35.8</b></td><td>Mixing Sync and Async Code</td><td>the traps at the boundary</td><td>Where most async bugs originate</td><td align="center">●●●</td></tr>
<tr><td><b>35.9</b></td><td>Practical Async I/O</td><td>files and network, without blocking</td><td>Where async delivers its real payoff</td><td align="center">●●●</td></tr>
</table>

### 36. Testing

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>36.1</b></td><td>Why Test — Theory and Test Types</td><td>unit, integration, end-to-end, and what to test</td><td>Testing the wrong layer wastes effort</td><td align="center">●●●</td></tr>
<tr><td><b>36.2</b></td><td><code>unittest</code> Basics</td><td>the testing framework in the standard library</td><td>Available everywhere, no install needed</td><td align="center">●●●</td></tr>
<tr><td><b>36.3</b></td><td>Assertions and Test Fixtures</td><td>checking results, and setting up test data</td><td>Clear failures and no repeated setup</td><td align="center">●●●</td></tr>
<tr><td><b>36.4</b></td><td><code>pytest</code> Basics</td><td>the framework most projects actually use</td><td>Less ceremony, better failure output</td><td align="center">●●●</td></tr>
<tr><td><b>36.5</b></td><td><code>pytest</code> Fixtures</td><td>reusable setup, done properly</td><td>Reusable setup without inheritance</td><td align="center">●●●</td></tr>
<tr><td><b>36.6</b></td><td>Parametrized Tests</td><td>one test, many inputs</td><td>Dozens of cases from one test</td><td align="center">●●●</td></tr>
<tr><td><b>36.7</b></td><td>Mocking</td><td><code>unittest.mock</code>, <code>monkeypatch</code></td><td>Test without calling real services</td><td align="center">●●●</td></tr>
<tr><td><b>36.8</b></td><td>Test Coverage</td><td>measuring what your tests actually reach</td><td>Shows which paths are untested</td><td align="center">●●●</td></tr>
<tr><td><b>36.9</b></td><td><code>doctest</code></td><td>tests that live inside your docstrings</td><td>Documentation that cannot go stale</td><td align="center">●●●</td></tr>
<tr><td><b>36.10</b></td><td>The TDD Workflow</td><td>write the test first, then the code</td><td>Design pressure, not just verification</td><td align="center">●●●</td></tr>
</table>

### 37. Debugging, Logging, Profiling

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>37.1</b></td><td>Reading Tracebacks</td><td>reading an error from the bottom up</td><td>The fastest route to the actual cause</td><td align="center">●●●</td></tr>
<tr><td><b>37.2</b></td><td>Debugging with <code>print</code> vs a Debugger</td><td>when each one is the right tool</td><td>Knowing when each is the right tool</td><td align="center">●●●</td></tr>
<tr><td><b>37.3</b></td><td><code>pdb</code> / <code>breakpoint()</code></td><td>stepping through code line by line</td><td>Inspect live state instead of guessing</td><td align="center">●●●</td></tr>
<tr><td><b>37.4</b></td><td>The VS Code Debugger</td><td>breakpoints, watches, and the call stack</td><td>Debugging without editing your code</td><td align="center">●●●</td></tr>
<tr><td><b>37.5</b></td><td><code>logging</code> Deep Dive</td><td>levels, handlers, formatters, config</td><td>How you diagnose systems already running</td><td align="center">●●●</td></tr>
<tr><td><b>37.6</b></td><td>Profiling</td><td><code>timeit</code>, <code>cProfile</code>, memory</td><td>The bottleneck is rarely where you think</td><td align="center">●●●</td></tr>
<tr><td><b>37.7</b></td><td>Optimization Strategies</td><td>measure first, then optimise</td><td>Stops you optimising the wrong thing</td><td align="center">●●●</td></tr>
<tr><td><b>37.8</b></td><td>Big-O Basics for Python Data Structures</td><td>why the right data structure beats clever code</td><td>Explains why code slows as data grows</td><td align="center">●●●</td></tr>
</table>

### 38. Working with Data Formats and APIs

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>38.1</b></td><td>JSON Deep Dive</td><td>nested data, custom encoders, common errors</td><td>The format most APIs speak</td><td align="center">●●●</td></tr>
<tr><td><b>38.2</b></td><td>CSV Deep Dive</td><td>delimiters, quoting, headers, dialects</td><td>Real files are messier than they look</td><td align="center">●●●</td></tr>
<tr><td><b>38.3</b></td><td>XML and YAML</td><td>when you meet them, and how to handle them</td><td>Configuration and legacy systems</td><td align="center">●●●</td></tr>
<tr><td><b>38.4</b></td><td>HTTP Basics</td><td>requests, responses, status codes, headers</td><td>Needed to debug any network call</td><td align="center">●●●</td></tr>
<tr><td><b>38.5</b></td><td><code>urllib</code> and <code>requests</code></td><td>fetching data over the network</td><td>How Python reaches the wider internet</td><td align="center">●●●</td></tr>
<tr><td><b>38.6</b></td><td>Consuming REST APIs</td><td>authentication, pagination, error handling</td><td>The most common integration task</td><td align="center">●●●</td></tr>
<tr><td><b>38.7</b></td><td>Web Scraping Basics (<code>BeautifulSoup</code>) and Ethics</td><td>parsing HTML, and scraping responsibly</td><td>Getting data that has no API</td><td align="center">●●●</td></tr>
</table>

### 39. Databases

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>39.1</b></td><td>Database Theory and SQL Refresher</td><td>tables, rows, keys, and the queries you need</td><td>Files stop scaling surprisingly early</td><td align="center">●●●</td></tr>
<tr><td><b>39.2</b></td><td>The <code>sqlite3</code> Module</td><td>a real database with no server to install</td><td>A real database with zero setup</td><td align="center">●●●</td></tr>
<tr><td><b>39.3</b></td><td>CRUD Operations</td><td>create, read, update, delete</td><td>The four operations behind every app</td><td align="center">●●●</td></tr>
<tr><td><b>39.4</b></td><td>Parameterized Queries and SQL Injection</td><td>the single most important security habit here</td><td>The most exploited web vulnerability</td><td align="center">●●●</td></tr>
<tr><td><b>39.5</b></td><td>Transactions</td><td>all-or-nothing changes</td><td>Prevents half-finished changes</td><td align="center">●●●</td></tr>
<tr><td><b>39.6</b></td><td>ORM Introduction</td><td>SQLAlchemy basics</td><td>How most production Python talks to a database</td><td align="center">●●●</td></tr>
</table>

### 40. Project Structure and Packaging

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>40.1</b></td><td>Project Layout Conventions</td><td><code>src</code> layout</td><td>Prevents import problems later</td><td align="center">●●●</td></tr>
<tr><td><b>40.2</b></td><td><code>requirements.txt</code> vs <code>pyproject.toml</code></td><td>declaring what your project needs</td><td>Reproducible installs for everyone</td><td align="center">●●●</td></tr>
<tr><td><b>40.3</b></td><td>Dependency Management Tools</td><td><code>pip-tools</code>, <code>poetry</code>, <code>uv</code></td><td>Stops works-on-my-machine failures</td><td align="center">●●●</td></tr>
<tr><td><b>40.4</b></td><td>Building a Distributable Package</td><td>turning your code into something installable</td><td>Sharing code beyond one folder</td><td align="center">●●●</td></tr>
<tr><td><b>40.5</b></td><td>Publishing to PyPI</td><td>sharing your package with the world</td><td>Anyone can `pip install` your work</td><td align="center">●●●</td></tr>
<tr><td><b>40.6</b></td><td>Entry Points and CLI Tools</td><td>making your package runnable as a command</td><td>A real command, not a script path</td><td align="center">●●●</td></tr>
<tr><td><b>40.7</b></td><td>Semantic Versioning</td><td>what the numbers in <code>1.4.2</code> actually promise</td><td>Tells users what an upgrade will break</td><td align="center">●●●</td></tr>
</table>

### 41. Code Quality and Tooling

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>41.1</b></td><td>PEP 8 Deep Dive</td><td>naming, spacing, imports, line length</td><td>The style every reviewer expects</td><td align="center">●●●</td></tr>
<tr><td><b>41.2</b></td><td>Linters</td><td><code>ruff</code>, <code>flake8</code>, <code>pylint</code></td><td>Catches bugs before your tests do</td><td align="center">●●●</td></tr>
<tr><td><b>41.3</b></td><td>Formatters</td><td><code>black</code>, <code>ruff format</code></td><td>Removes style from code review entirely</td><td align="center">●●●</td></tr>
<tr><td><b>41.4</b></td><td>Pre-commit Hooks</td><td>running checks automatically before each commit</td><td>Broken code never reaches the repository</td><td align="center">●●●</td></tr>
<tr><td><b>41.5</b></td><td>Docstring Standards and <code>sphinx</code> / <code>mkdocs</code></td><td>writing docs people will actually read</td><td>Unused code might as well not exist</td><td align="center">●●●</td></tr>
<tr><td><b>41.6</b></td><td>Code Smells and Refactoring</td><td>recognising bad code, and improving it safely</td><td>Changing code safely without breaking it</td><td align="center">●●●</td></tr>
<tr><td><b>41.7</b></td><td>Clean Code Principles</td><td>naming, function size, and single responsibility</td><td>The difference between working and maintainable</td><td align="center">●●●</td></tr>
</table>

### 42. Security Basics

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>42.1</b></td><td>Input Validation</td><td>never trust what comes in from outside</td><td>The root of most vulnerabilities</td><td align="center">●●●</td></tr>
<tr><td><b>42.2</b></td><td>Secrets Management</td><td><code>.env</code>, environment variables</td><td>Leaked credentials are a common breach cause</td><td align="center">●●●</td></tr>
<tr><td><b>42.3</b></td><td>Hashing and Passwords</td><td>storing passwords so a leak is survivable</td><td>Plain-text passwords turn a leak into a disaster</td><td align="center">●●●</td></tr>
<tr><td><b>42.4</b></td><td>Common Python Vulnerabilities</td><td><code>eval</code>, <code>pickle</code>, path traversal</td><td>Specific traps that appear in real code</td><td align="center">●●●</td></tr>
<tr><td><b>42.5</b></td><td>Dependency Security</td><td>auditing what your dependencies bring with them</td><td>Your dependencies are your attack surface</td><td align="center">●●●</td></tr>
</table>

### 43. Advanced Internals

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>43.1</b></td><td>Bytecode and <code>dis</code></td><td>seeing the instructions your code compiles to</td><td>See exactly what your code costs</td><td align="center">●●●</td></tr>
<tr><td><b>43.2</b></td><td>Memory Management Deep Dive</td><td>reference counting, and the object model</td><td>Explains memory use and object behaviour</td><td align="center">●●●</td></tr>
<tr><td><b>43.3</b></td><td>The <code>gc</code> Module and Circular References</td><td>the collector that catches what counting misses</td><td>Explains leaks that counting misses</td><td align="center">●●●</td></tr>
<tr><td><b>43.4</b></td><td><code>weakref</code></td><td>references that do not keep an object alive</td><td>Caches that do not prevent cleanup</td><td align="center">●●●</td></tr>
<tr><td><b>43.5</b></td><td>Interning and the Small Integer Cache</td><td>why <code>a is b</code> is sometimes surprisingly <code>True</code></td><td>Explains surprising `is` comparisons</td><td align="center">●●●</td></tr>
<tr><td><b>43.6</b></td><td><code>sys</code> Internals</td><td>recursion limits, sizes, and interpreter internals</td><td>Tuning limits and inspecting the runtime</td><td align="center">●●●</td></tr>
<tr><td><b>43.7</b></td><td>C Extensions and <code>ctypes</code> Introduction</td><td>calling C code from Python</td><td>How the fast libraries actually work</td><td align="center">●●●</td></tr>
</table>

### 44. Projects

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>44.1</b></td><td>Beginner: CLI Calculator / Number Game</td><td>input, conditionals, loops, functions</td><td>Your first complete program</td><td align="center">●●●</td></tr>
<tr><td><b>44.2</b></td><td>Beginner: Text File Word Counter</td><td>file reading, dictionaries, sorting</td><td>Real file handling and data summarising</td><td align="center">●●●</td></tr>
<tr><td><b>44.3</b></td><td>Intermediate: To-Do CLI with JSON Storage</td><td>persistence, JSON, and a real command-line interface</td><td>Data that survives restarting the program</td><td align="center">●●●</td></tr>
<tr><td><b>44.4</b></td><td>Intermediate: API Data Fetcher</td><td>HTTP, JSON parsing, error handling</td><td>Working with live external data</td><td align="center">●●●</td></tr>
<tr><td><b>44.5</b></td><td>OOP: Bank / Library Management System</td><td>classes, inheritance, encapsulation</td><td>Where OOP finally pays off</td><td align="center">●●●</td></tr>
<tr><td><b>44.6</b></td><td>Database: Contact Book with SQLite</td><td>SQL, CRUD, transactions</td><td>Persistent, queryable storage</td><td align="center">●●●</td></tr>
<tr><td><b>44.7</b></td><td>Async: Concurrent Downloader</td><td><code>asyncio</code>, concurrency, timing</td><td>Concurrency with a measurable speedup</td><td align="center">●●●</td></tr>
<tr><td><b>44.8</b></td><td>Capstone: Packaged CLI Tool with Tests</td><td>packaging, testing, documentation, publishing</td><td>Everything together, shipped properly</td><td align="center">●●●</td></tr>
</table>

### 45. Appendix

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Topic</th><th align="left" width="34%">Covers</th><th align="left" width="27%">Why it matters</th><th align="center" width="6%">Level</th></tr>
<tr><td><b>45.1</b></td><td>Complete Built-in Functions Reference</td><td>every built-in, with a one-line description</td><td>Discover functions you did not know existed</td><td align="center">●●●</td></tr>
<tr><td><b>45.2</b></td><td>Complete Keyword Reference</td><td>every keyword, with a one-line description</td><td>The complete vocabulary of the language</td><td align="center">●●●</td></tr>
<tr><td><b>45.3</b></td><td>Dunder Method Cheat Sheet</td><td>every dunder, grouped by purpose</td><td>The fastest way to find the right one</td><td align="center">●●●</td></tr>
<tr><td><b>45.4</b></td><td>Exception Hierarchy Chart</td><td>the full tree, as a diagram</td><td>Shows you what to catch</td><td align="center">●●●</td></tr>
<tr><td><b>45.5</b></td><td>Glossary</td><td>every term in this course, defined</td><td>One place for every term used here</td><td align="center">●●●</td></tr>
<tr><td><b>45.6</b></td><td>Further Resources</td><td>books, docs, and where to go next</td><td>Where to go after this course</td><td align="center">●●●</td></tr>
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
