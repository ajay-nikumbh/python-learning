# Chapter 06 — Operators

**343 numbered examples.** This is where the example density steps up — operators have enough surface area to drill properly, and every one of them has behaviour that surprises people at least once.

`2 + 3 * 4` is `14`, everyone knows. But `-2 ** 2` is `-4`, `1 & 2 == 2` is `1`, `x or 10` silently breaks when `x` is `0`, and `items += [x]` inside a function modifies the caller's list. Those are the ones that cost real debugging time.

**By the end you will be able to:**

- Explain `-7 // 2`, `-7 % 2` and `int(-7/2)` without looking them up
- Use chained comparisons and explain the single-evaluation guarantee
- Predict what `and` and `or` return — which is not a boolean
- Say when `+=` differs from `= +`, and why it matters inside functions
- Pack flags into an integer with bitwise operators
- Bracket the three precedence traps before they bite
- Know when the walrus operator earns its place

---

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="26%">Notebook</th><th align="left" width="9%">Examples</th><th align="left" width="58%">Core idea</th></tr>
<tr><td><b>06.1</b></td><td><code>arithmetic_operators</code></td><td align="center">45</td><td>Seven operators as dunder calls; floor division towards −∞</td></tr>
<tr><td><b>06.2</b></td><td><code>comparison_and_chaining</code></td><td align="center">45</td><td><code>1 &lt; x &lt; 10</code> evaluates <code>x</code> once — proved with a counter</td></tr>
<tr><td><b>06.3</b></td><td><code>logical_operators</code></td><td align="center">37</td><td><code>and</code>/<code>or</code> return operands; short-circuiting is guaranteed</td></tr>
<tr><td><b>06.4</b></td><td><code>assignment_operators</code></td><td align="center">35</td><td><code>+=</code> mutates, <code>= +</code> rebinds — aliases tell them apart</td></tr>
<tr><td><b>06.5</b></td><td><code>bitwise_operators</code></td><td align="center">35</td><td>Flag sets built by hand, then with <code>enum.Flag</code></td></tr>
<tr><td><b>06.6</b></td><td><code>identity_and_membership</code></td><td align="center">35</td><td><code>in</code> is O(1) on sets, O(n) on lists — benchmarked live</td></tr>
<tr><td><b>06.7</b></td><td><code>precedence_and_associativity</code></td><td align="center">30</td><td>The full 18-level table and the three traps</td></tr>
<tr><td><b>06.8</b></td><td><code>walrus_operator</code></td><td align="center">31</td><td><code>while (chunk := read())</code> — the pattern it was added for</td></tr>
<tr><td><b>—</b></td><td><code>exercises</code></td><td align="center">50</td><td>20 rapid-fire predictions, 4 real bugs, 10 precedence drills</td></tr>
</table>

---

## Quick reference

### Arithmetic

<table width="100%">
<tr><th align="left" width="14%">Operator</th><th align="left" width="30%">Does</th><th align="left" width="26%">Watch out for</th><th align="left" width="30%">Example</th></tr>
<tr><td><code>/</code></td><td>True division</td><td><b>Always</b> a float</td><td><code>10 / 5</code> → <code>2.0</code></td></tr>
<tr><td><code>//</code></td><td>Floor division</td><td>Rounds towards −∞</td><td><code>-7 // 2</code> → <code>-4</code></td></tr>
<tr><td><code>%</code></td><td>Remainder</td><td>Sign of the <b>divisor</b></td><td><code>-7 % 2</code> → <code>1</code></td></tr>
<tr><td><code>**</code></td><td>Power</td><td><b>Right</b>-associative</td><td><code>2**3**2</code> → <code>512</code></td></tr>
</table>

`(a // b) * b + (a % b) == a` always holds. `%` taking the divisor's sign is what makes `-3 % 12 == 9` correct for clocks and indices.

### Comparison and chaining

```python
18 <= age < 65        # expands to (18 <= age) and (age < 65)
                      # but evaluates `age` ONLY ONCE
```

That matters for expensive calls, iterators and anything with side effects.

Traps: `a != b != c` does **not** mean "all distinct" — use `len({a,b,c}) == 3`. And `value is None is True` is `False` even when `value` is `None`.

### Logic

<table width="100%">
<tr><th align="left" width="20%">Expression</th><th align="left" width="44%">Returns</th><th align="left" width="36%">Example</th></tr>
<tr><td><code>a or b</code></td><td>First <b>truthy</b> operand, else the last</td><td><code>'' or 'x'</code> → <code>'x'</code></td></tr>
<tr><td><code>a and b</code></td><td>First <b>falsy</b> operand, else the last</td><td><code>1 and 0</code> → <code>0</code></td></tr>
<tr><td><code>not a</code></td><td>A real <code>bool</code> — the only one</td><td><code>not []</code> → <code>True</code></td></tr>
</table>

**Short-circuiting is guaranteed**, which is what makes guards safe:

```python
if user is not None and user.active:    # second half never runs if None
```

**The `or`-default trap:** `limit or 10` replaces `0` too. Use `10 if limit is None else limit`.

### Assignment

```python
items += [4]          # __iadd__ → mutates in place → aliases SEE it
items = items + [4]   # __add__  → new object       → aliases do not
```

Inside a function, `+=` on a list parameter **modifies the caller's data**. And `t[1] += [4]` on a tuple both mutates the inner list *and* raises `TypeError`.

### Bitwise

<table width="100%">
<tr><th align="left" width="16%">Operator</th><th align="left" width="36%">Rule</th><th align="left" width="48%">Flag use</th></tr>
<tr><td><code>&</code></td><td>1 when <b>both</b> bits are 1</td><td><code>if (flags & READ):</code> — test</td></tr>
<tr><td><code>\|</code></td><td>1 when <b>either</b> is 1</td><td><code>flags \|= WRITE</code> — add</td></tr>
<tr><td><code>^</code></td><td>1 when they <b>differ</b></td><td><code>flags ^= READ</code> — toggle</td></tr>
<tr><td><code>~</code></td><td>Inverts — always <code>-(x+1)</code></td><td><code>flags &= ~WRITE</code> — remove</td></tr>
<tr><td><code>&lt;&lt;</code> <code>&gt;&gt;</code></td><td><code>x * 2**n</code> / <code>x // 2**n</code></td><td>Extracting packed bytes</td></tr>
</table>

Prefer **`enum.Flag`** in real code. And `&` is **not** `and` — no short-circuiting, different result.

### Identity and membership

<table width="100%">
<tr><th align="left" width="20%">Operator</th><th align="left" width="34%">Asks</th><th align="left" width="46%">Use for</th></tr>
<tr><td><code>is</code></td><td>Same object? (<code>id(a) == id(b)</code>)</td><td><b>Only</b> <code>None</code>, <code>True</code>, <code>False</code>, sentinels</td></tr>
<tr><td><code>in</code></td><td>Value present?</td><td>Dicts search <b>keys</b>; strings search <b>substrings</b></td></tr>
</table>

`in` is **O(1)** on sets and dicts, **O(n)** on lists and tuples — thousands of times faster at scale. It checks identity *before* equality, which is why `nan in [nan]` is `True`.

### The three precedence traps

<table width="100%">
<tr><th align="left" width="28%">You write</th><th align="left" width="34%">Python reads</th><th align="left" width="38%">Fix</th></tr>
<tr><td><code>-2 ** 2</code></td><td><code>-(2 ** 2)</code> → <code>-4</code></td><td><code>(-2) ** 2</code></td></tr>
<tr><td><code>flags & F == F</code></td><td><code>flags & (F == F)</code></td><td><code>(flags & F) == F</code></td></tr>
<tr><td><code>not a == b</code></td><td><code>not (a == b)</code></td><td><code>a != b</code></td></tr>
</table>

Tightest to loosest: `**` → unary → `* /` → `+ -` → `<< >>` → `&` → `^` → `|` → comparisons → `not` → `and` → `or` → `:=`.

**Bracket anything not instantly obvious.** Brackets cost nothing.

### Walrus

```python
while (chunk := read()) != "":     # the pattern it was added for
    process(chunk)
```

Use it to remove **duplication**, not merely a line. It cannot assign to attributes or subscripts, and the name **leaks out** of a comprehension.

---

## Key Terms

<table width="100%">
<tr><th align="left" width="26%">Term</th><th align="left" width="44%">Meaning</th><th align="left" width="30%">Where</th></tr>
<tr><td><b>Dunder method</b></td><td>What an operator actually calls</td><td>06.1 — <code>__add__</code></td></tr>
<tr><td><b>Reflected operation</b></td><td><code>__radd__</code> when the left operand cannot cope</td><td>06.1</td></tr>
<tr><td><b>Type promotion</b></td><td>Widening <code>int → float → complex</code></td><td>06.1</td></tr>
<tr><td><b>Chaining</b></td><td><code>a &lt; b &lt; c</code> with single evaluation</td><td>06.2</td></tr>
<tr><td><b>Lexicographic</b></td><td>Element-by-element comparison</td><td>06.2</td></tr>
<tr><td><b>Short-circuiting</b></td><td>Skipping the second operand</td><td>06.3 — guaranteed</td></tr>
<tr><td><b>Guard pattern</b></td><td><code>x is not None and x.attr</code></td><td>06.3</td></tr>
<tr><td><b>Augmented assignment</b></td><td><code>+=</code> and friends</td><td>06.4</td></tr>
<tr><td><b><code>__iadd__</code></b></td><td>The method that makes <code>+=</code> mutate</td><td>06.4</td></tr>
<tr><td><b>Two's complement</b></td><td>Why <code>~x == -(x+1)</code></td><td>06.5</td></tr>
<tr><td><b>Mask</b></td><td><code>& 0xFF</code> to isolate bits</td><td>06.5</td></tr>
<tr><td><b>Interning</b></td><td>Cached objects making <code>is</code> unreliable</td><td>06.6</td></tr>
<tr><td><b>Associativity</b></td><td>Order when precedence ties</td><td>06.7</td></tr>
<tr><td><b>Assignment expression</b></td><td><code>:=</code> — assigns and evaluates</td><td>06.8</td></tr>
</table>

---

## Next

**Chapter 07 — Strings.** Indexing and slicing, the complete method set, f-strings and the format mini-language, escape sequences, and the Unicode model that causes most text bugs.
