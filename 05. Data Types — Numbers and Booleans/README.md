# Chapter 05 — Data Types: Numbers and Booleans

```python
>>> 0.1 + 0.2
0.30000000000000004
```

That is not a bug. It is the correct, inevitable result of storing decimal fractions in binary — and it is the single most consequential thing in this chapter. Understanding it takes ten minutes and prevents a career of confusing financial bugs.

Numbers are where "obviously correct" code quietly produces wrong answers.

**By the end you will be able to:**

- Explain why Python integers never overflow
- Explain exactly why `0.1 + 0.2 != 0.3`, and which decimals *are* exact
- Compare floats correctly, and never write `==` between them again
- Choose between `float`, `Decimal`, `Fraction` and integer minor units for money
- List every falsy value, and know when `if x:` is the wrong check
- Convert untrusted input safely, validating range as well as type

---

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="28%">Notebook</th><th align="left" width="30%">Core idea</th><th align="left" width="35%">Proved by</th></tr>
<tr><td><b>05.1</b></td><td><code>integers</code></td><td>Arbitrary precision, no overflow</td><td>Factorials staying exact past 64 bits</td></tr>
<tr><td><b>05.2</b></td><td><code>floats_and_precision</code></td><td>Floats are binary fractions</td><td>Raw IEEE 754 bits via <code>struct</code>; exact fractions</td></tr>
<tr><td><b>05.3</b></td><td><code>complex_numbers</code></td><td>Built into the core</td><td>An ASCII Mandelbrot set</td></tr>
<tr><td><b>05.4</b></td><td><code>decimal_and_fraction</code></td><td>Exact decimal and rational maths</td><td>An invoice priced both ways, side by side</td></tr>
<tr><td><b>05.5</b></td><td><code>booleans_and_truthiness</code></td><td><code>bool</code> is an <code>int</code></td><td><code>{1: 'a', True: 'b'}</code> collapsing to one key</td></tr>
<tr><td><b>05.6</b></td><td><code>none_type</code></td><td><code>None</code> is a singleton</td><td><code>items = items.sort()</code> destroying a list</td></tr>
<tr><td><b>05.7</b></td><td><code>type_conversion</code></td><td>Strong typing, explicit casts</td><td>A conversion table across 12 awkward inputs</td></tr>
<tr><td><b>05.8</b></td><td><code>math_module</code></td><td>Precision-preserving functions</td><td><code>hypot</code> succeeding where naive <code>sqrt</code> overflows</td></tr>
<tr><td><b>—</b></td><td><code>exercises</code></td><td>Practice</td><td>Eight predict-the-output traps plus float forensics</td></tr>
</table>

---

## Quick reference

### The numeric types

<table width="100%">
<tr><th align="left" width="16%">Type</th><th align="left" width="26%">Stores</th><th align="left" width="26%">Exact for</th><th align="left" width="32%">Use for</th></tr>
<tr><td><code>int</code></td><td>Unlimited digits</td><td>All whole numbers</td><td>Counting, money as paise/cents</td></tr>
<tr><td><code>float</code></td><td>IEEE 754 binary</td><td>Powers of two only</td><td>Measurement, science, graphics</td></tr>
<tr><td><code>Decimal</code></td><td>Decimal digits</td><td>Any decimal</td><td><b>Money</b>, tax, percentages</td></tr>
<tr><td><code>Fraction</code></td><td>Numerator/denominator</td><td>Any rational</td><td>Exact ratios, probability</td></tr>
<tr><td><code>complex</code></td><td>Two floats</td><td>—</td><td>Signal processing, engineering</td></tr>
</table>

### Why `0.1 + 0.2` fails

A 64-bit float is 1 sign bit, 11 exponent bits, 52 mantissa bits — about 15–17 significant digits.

One tenth in binary is `0.0001100110011...` repeating forever, exactly as one third repeats in decimal. The mantissa truncates it, so `0.1` is stored as slightly *more* than 0.1. Two such errors add up to something visible.

**Exact:** `0.5`, `0.25`, `0.125`, `0.75` — denominators that are powers of two.
**Not exact:** `0.1`, `0.2`, `0.3` and almost everything else.

```python
# Never
if a == b:

# Always
if math.isclose(a, b, rel_tol=1e-9, abs_tol=1e-9):
```

Pass `abs_tol` whenever either value might be zero — relative tolerance alone fails there.

### Division

<table width="100%">
<tr><th align="left" width="18%">Operator</th><th align="left" width="30%">Does</th><th align="left" width="24%">Example</th><th align="left" width="28%">Returns</th></tr>
<tr><td><code>/</code></td><td>True division</td><td><code>10 / 5</code></td><td><code>2.0</code> — <b>always a float</b></td></tr>
<tr><td><code>//</code></td><td>Floor division</td><td><code>-7 // 2</code></td><td><code>-4</code> — towards −∞</td></tr>
<tr><td><code>%</code></td><td>Remainder</td><td><code>-7 % 2</code></td><td><code>1</code> — sign of the <b>divisor</b></td></tr>
<tr><td><code>int()</code></td><td>Truncation</td><td><code>int(-3.9)</code></td><td><code>-3</code> — towards <b>zero</b></td></tr>
</table>

`(a // b) * b + (a % b) == a` always holds. `%` taking the divisor's sign is what makes `-3 % 12 == 9` correct for clock arithmetic.

### Money

```python
Decimal("0.1")    # exactly one tenth
Decimal(0.1)      # inherits the float's error — never do this
```

Three defensible approaches: `Decimal` from strings, integer minor units (paise, cents), or a money library. Floats are **not** among them.

### Truthiness

**Falsy:** `False`, `None`, `0`, `0.0`, `0j`, `""`, `[]`, `()`, `{}`, `set()`, `range(0)`.

**Everything else is truthy** — including `"False"`, `"0"`, `[0]`, `" "` and `float("nan")`.

<table width="100%">
<tr><th align="left" width="34%">Check</th><th align="left" width="66%">Use when</th></tr>
<tr><td><code>if x:</code></td><td>Empty and zero should be treated the same</td></tr>
<tr><td><code>if x is not None:</code></td><td><b>0 or "" is a legitimate value</b></td></tr>
</table>

`bool` is a subclass of `int`, so `True == 1`. That makes `sum(flags)` a neat counter — and makes `1` and `True` the same dict key.

### `None`

A **singleton** — one object for the whole program. That is why `x is None` is reliable and `x == None` is not (a class can override `__eq__`; linters flag it as `E711`).

Methods that **mutate in place return `None`**:

```python
items = items.sort()     # items is now None — the classic bug
items.sort()             # correct, sorts in place
items = sorted(items)    # correct, returns a new list
```

### `math` functions worth knowing

<table width="100%">
<tr><th align="left" width="28%">Function</th><th align="left" width="72%">Why it exists</th></tr>
<tr><td><code>math.fsum(values)</code></td><td>Accurate summation — <code>sum()</code> accumulates error</td></tr>
<tr><td><code>math.isqrt(n)</code></td><td>Exact integer square root — <code>int(sqrt(n))</code> is wrong for large n</td></tr>
<tr><td><code>math.hypot(x, y)</code></td><td>Hypotenuse without overflow</td></tr>
<tr><td><code>math.isclose(a, b)</code></td><td>The correct float comparison</td></tr>
<tr><td><code>math.isnan(x)</code></td><td><code>nan != nan</code>, so <code>==</code> cannot work</td></tr>
<tr><td><code>math.expm1</code> / <code>log1p</code></td><td>Accurate near zero</td></tr>
</table>

Prefer `**` over `math.pow()` — the operator keeps integers exact.

### Converting untrusted input

```python
def parse_int(text, default=None):
    try:
        return int(text)
    except (ValueError, TypeError):   # TypeError for None, lists
        return default
```

Validate **range** as well as type — a parsed number can still be nonsense.

---

## Key Terms

<table width="100%">
<tr><th align="left" width="26%">Term</th><th align="left" width="42%">Meaning</th><th align="left" width="32%">Where</th></tr>
<tr><td><b>Arbitrary precision</b></td><td>Integers with no maximum value</td><td>05.1</td></tr>
<tr><td><b>Floor division</b></td><td><code>//</code> — rounds towards −∞</td><td>05.1</td></tr>
<tr><td><b>IEEE 754</b></td><td>The binary floating-point standard</td><td>05.2</td></tr>
<tr><td><b>Mantissa</b></td><td>The 52 significant bits of a float</td><td>05.2</td></tr>
<tr><td><b>Catastrophic cancellation</b></td><td>Precision lost subtracting near-equal values</td><td>05.2</td></tr>
<tr><td><b>Banker's rounding</b></td><td>Halves round to even — Python's default</td><td>05.2</td></tr>
<tr><td><b>NaN</b></td><td>Not a Number — never equal to itself</td><td>05.2</td></tr>
<tr><td><b>Numeric tower</b></td><td><code>Complex → Real → Rational → Integral</code></td><td>05.3</td></tr>
<tr><td><b>Context</b></td><td><code>Decimal</code>'s precision and rounding settings</td><td>05.4</td></tr>
<tr><td><b>quantize</b></td><td>Fixing a <code>Decimal</code> to set decimal places</td><td>05.4</td></tr>
<tr><td><b>Truthiness</b></td><td>How any object behaves in a condition</td><td>05.5</td></tr>
<tr><td><b>Short-circuiting</b></td><td><code>and</code>/<code>or</code> skipping the second operand</td><td>05.5</td></tr>
<tr><td><b>Singleton</b></td><td>A type with exactly one instance</td><td>05.6 — <code>None</code></td></tr>
<tr><td><b>Sentinel</b></td><td>A unique marker for "not supplied"</td><td>05.6</td></tr>
<tr><td><b>Strong typing</b></td><td>No silent conversion between unrelated types</td><td>05.7</td></tr>
</table>

---

## Next

**Chapter 06 — Operators.** Precedence and associativity, chained comparisons, short-circuit evaluation, the bitwise operators, `is` versus `==`, and the walrus operator.
