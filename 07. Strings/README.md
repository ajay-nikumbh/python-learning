# Chapter 07 — Strings

**248 examples, each in its own cell, graded Easy → Medium → Hard.**

Text is what most programs actually handle. This chapter goes from "what is a string" to the Unicode model that causes most text bugs — but you can stop at the end of any Easy section and still have learned something useful.

## How to work through this

Every notebook is split into three sections:

<table width="100%">
<tr><th align="left" width="16%">Section</th><th align="left" width="84%">What it is for</th></tr>
<tr><td><b>Easy</b></td><td>The basics, one small idea per cell. Start here. If this is enough for today, stop here — nothing later depends on finishing the rest now.</td></tr>
<tr><td><b>Medium</b></td><td>Everyday working knowledge. This is where most real code lives.</td></tr>
<tr><td><b>Hard</b></td><td>The corners that cause bugs, plus performance. Come back to these when the earlier sections feel comfortable.</td></tr>
</table>

**By the end you will be able to:**

- Index and slice text confidently, including negative positions
- Explain why `text.upper()` alone does nothing
- Use f-strings with alignment, number formatting and the `=` debug suffix
- Reach for the right method out of the ~45 available
- Build strings efficiently instead of with `+=` in a loop
- Explain why `len("café")` and `len("café".encode())` differ

---

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Notebook</th><th align="left" width="9%">Examples</th><th align="left" width="58%">Covers</th></tr>
<tr><td><b>07.1</b></td><td><code>string_literals</code></td><td align="center">33</td><td>Quote styles, triple quotes, escapes, raw strings</td></tr>
<tr><td><b>07.2</b></td><td><code>indexing_and_slicing</code></td><td align="center">31</td><td>Positions, ranges, steps, reversing</td></tr>
<tr><td><b>07.3</b></td><td><code>string_immutability</code></td><td align="center">19</td><td>Why methods return new strings; the <code>join</code> pattern</td></tr>
<tr><td><b>07.4</b></td><td><code>string_methods</code></td><td align="center">35</td><td>All seven method families, and their sharp edges</td></tr>
<tr><td><b>07.5</b></td><td><code>f_strings</code></td><td align="center">31</td><td>Embedding values, formatting, the <code>=</code> debug suffix</td></tr>
<tr><td><b>07.6</b></td><td><code>older_formatting_and_spec</code></td><td align="center">22</td><td><code>.format()</code>, <code>%</code>, and the full format mini-language</td></tr>
<tr><td><b>07.7</b></td><td><code>unicode_and_encoding</code></td><td align="center">26</td><td><code>str</code> vs <code>bytes</code>, UTF-8, normalisation</td></tr>
<tr><td><b>07.8</b></td><td><code>performance_and_textwrap</code></td><td align="center">19</td><td>Why <code>join</code> beats <code>+=</code>; paragraph formatting</td></tr>
<tr><td><b>—</b></td><td><code>exercises</code></td><td align="center">32</td><td>Predict, fix and build — also graded</td></tr>
</table>

---

## Quick reference

### Indexing and slicing

```
  P    y    t    h    o    n
  0    1    2    3    4    5      from the start
 -6   -5   -4   -3   -2   -1      from the end
```

<table width="100%">
<tr><th align="left" width="26%">Expression</th><th align="left" width="30%">Gives</th><th align="left" width="44%">Note</th></tr>
<tr><td><code>text[0]</code></td><td>First character</td><td>Raises <code>IndexError</code> if out of range</td></tr>
<tr><td><code>text[-1]</code></td><td>Last character</td><td>Negative counts from the end</td></tr>
<tr><td><code>text[a:b]</code></td><td>From <code>a</code> up to <b>not including</b> <code>b</code></td><td>Length is <code>b - a</code></td></tr>
<tr><td><code>text[:b]</code></td><td>From the beginning</td><td></td></tr>
<tr><td><code>text[a:]</code></td><td>To the end</td><td></td></tr>
<tr><td><code>text[::-1]</code></td><td>Reversed</td><td>Step of −1</td></tr>
<tr><td><code>text[::2]</code></td><td>Every other character</td><td></td></tr>
</table>

**Slicing out of range does not raise** — it clamps silently. Indexing does.

### Immutability

```python
text.upper()          # computes a new string, throws it away
text = text.upper()   # keeps it
```

Every string method returns a **new string**. To change one character:

```python
word = word[:i] + "X" + word[i + 1:]
```

### The method families

<table width="100%">
<tr><th align="left" width="18%">Family</th><th align="left" width="46%">Methods</th><th align="left" width="36%">For</th></tr>
<tr><td><b>Case</b></td><td><code>upper lower capitalize title casefold</code></td><td>Capitalisation</td></tr>
<tr><td><b>Whitespace</b></td><td><code>strip lstrip rstrip</code></td><td>Cleaning input</td></tr>
<tr><td><b>Search</b></td><td><code>find index count startswith endswith</code></td><td>Locating text</td></tr>
<tr><td><b>Split/join</b></td><td><code>split join splitlines partition</code></td><td>Breaking up, rebuilding</td></tr>
<tr><td><b>Replace</b></td><td><code>replace removeprefix removesuffix translate</code></td><td>Changing content</td></tr>
<tr><td><b>Test</b></td><td><code>isdigit isalpha isspace isalnum</code></td><td>Validating</td></tr>
<tr><td><b>Pad</b></td><td><code>ljust rjust center zfill</code></td><td>Aligning output</td></tr>
</table>

**Three sharp edges:**

- `"example.txt".strip(".txt")` removes *characters*, not a suffix → use `removesuffix()`
- `split()` collapses runs of whitespace; `split(" ")` does not
- `find()` returns `-1` when absent; `index()` raises

### f-strings

```python
f"{name} is {age}"              # embed any expression
f"{price:.2f}"                  # 2 decimal places
f"{population:,}"               # thousands separators
f"{name:<10}"                   # left-align in 10 columns
f"{number:05d}"                 # zero-pad
f"{count=}"                     # prints "count=42" — great for debugging
f"{text!r}"                     # use repr(), showing quotes
f"{value:.{places}f}"           # nested variable precision
```

Format spec order: `[[fill]align][sign][#][0][width][,][.precision][type]`

**Never build SQL or shell commands with an f-string.** Use parameterised queries.

### Building strings

```python
# Slow — O(n²), copies everything each time
result = ""
for part in parts:
    result += part

# Fast — measures once, allocates once
result = "".join(parts)
```

The rule only matters inside loops. For two or three pieces, `+` is fine.

### Unicode

<table width="100%">
<tr><th align="left" width="18%">Type</th><th align="left" width="34%">Holds</th><th align="left" width="48%">Convert with</th></tr>
<tr><td><code>str</code></td><td>Characters</td><td><code>.encode("utf-8")</code> → bytes</td></tr>
<tr><td><code>bytes</code></td><td>Numbers 0–255</td><td><code>.decode("utf-8")</code> → str</td></tr>
</table>

- UTF-8 uses **1–4 bytes per character**, so `len(text)` ≠ `len(text.encode())`
- **Always pass `encoding="utf-8"`** when opening files — the default is platform-dependent
- `é` can be **one character or two** (`e` + combining accent) — normalise with `unicodedata.normalize("NFC", text)` before comparing user input

---

## Key Terms

<table width="100%">
<tr><th align="left" width="26%">Term</th><th align="left" width="42%">Meaning</th><th align="left" width="32%">Where</th></tr>
<tr><td><b>Literal</b></td><td>Text written directly in source</td><td>07.1</td></tr>
<tr><td><b>Escape sequence</b></td><td><code>\\n</code>, <code>\\t</code>, <code>\\\\</code></td><td>07.1</td></tr>
<tr><td><b>Raw string</b></td><td><code>r"..."</code> — escapes off</td><td>07.1 — paths, regex</td></tr>
<tr><td><b>Index</b></td><td>Position of one character</td><td>07.2 — starts at 0</td></tr>
<tr><td><b>Slice</b></td><td>A range of characters</td><td>07.2 — stop excluded</td></tr>
<tr><td><b>Immutable</b></td><td>Cannot be changed in place</td><td>07.3</td></tr>
<tr><td><b>Interning</b></td><td>Reusing one object for equal literals</td><td>07.3 — why <code>is</code> is unreliable</td></tr>
<tr><td><b>f-string</b></td><td>Text with embedded expressions</td><td>07.5</td></tr>
<tr><td><b>Format spec</b></td><td>The part after the colon</td><td>07.6</td></tr>
<tr><td><b>Code point</b></td><td>The number for a character</td><td>07.7 — <code>ord()</code></td></tr>
<tr><td><b>Encoding</b></td><td>Rule converting str to bytes</td><td>07.7 — use UTF-8</td></tr>
<tr><td><b>Mojibake</b></td><td>Text decoded with the wrong encoding</td><td>07.7</td></tr>
<tr><td><b>Normalisation</b></td><td>Canonical form for comparison</td><td>07.7 — NFC</td></tr>
</table>

---

## Next

**Chapter 08 — Input, Output and Basic I/O.** `print()` in depth, reading and validating user input, command-line arguments, and formatted console output.
