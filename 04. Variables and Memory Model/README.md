# Chapter 04 — Variables and Memory Model

This is the chapter that explains the bugs that look like magic.

Why did my list change when I only touched a copy? Why does this function keep remembering things between calls? Why is `0.1 + 0.2` not `0.3`, and why does `a is b` sometimes lie? Almost every one of those questions traces back to one idea: **a variable is a label pointing at an object, not a box holding a value.**

Get this chapter right and a whole category of confusion disappears permanently.

**By the end you will be able to:**

- Explain why `a = b` copies nothing
- Predict whether a function's caller will see a change
- Say which types are mutable and why it matters for dict keys
- Explain when `+=` differs from `= +`
- Describe how memory is reclaimed, and what reference counting cannot free
- Use unpacking to remove temporary variables and index arithmetic

---

## The one idea

```
    NAME              REFERENCE           OBJECT
    ────              ─────────           ──────
    scores    ──────────────────────>    [90, 85, 77]
                                          id: 4382910
                                          type: list
```

Assignment binds a **name** to an **object**. It never copies. Many names can point at one object, and every one of them is a route through which that object can change.

<table width="100%">
<tr><th align="left" width="7%">#</th><th align="left" width="28%">Notebook</th><th align="left" width="30%">Core idea</th><th align="left" width="35%">Proved by</th></tr>
<tr><td><b>04.1</b></td><td><code>variables_and_assignment</code></td><td>Names are labels, not boxes</td><td><code>id()</code> across rebinding; the swap bytecode</td></tr>
<tr><td><b>04.2</b></td><td><code>names_objects_references</code></td><td>Pass by assignment</td><td><code>sys.getrefcount</code> rising and falling live</td></tr>
<tr><td><b>04.3</b></td><td><code>id_type_and_identity</code></td><td><code>is</code> is an id comparison</td><td>Small-int cache boundary found at runtime</td></tr>
<tr><td><b>04.4</b></td><td><code>mutable_vs_immutable</code></td><td>Identity survives mutation</td><td>A mutability tester run across nine types</td></tr>
<tr><td><b>04.5</b></td><td><code>reference_semantics_and_aliasing</code></td><td>Aliases are invisible until mutation</td><td>Five routes to one object, all changing together</td></tr>
<tr><td><b>04.6</b></td><td><code>garbage_collection</code></td><td>Refcounting plus a cycle collector</td><td><code>__del__</code> firing; a cycle surviving until <code>gc.collect()</code></td></tr>
<tr><td><b>04.7</b></td><td><code>constants_and_naming</code></td><td>Python has no constants</td><td><code>Final</code> rebound at runtime without complaint</td></tr>
<tr><td><b>04.8</b></td><td><code>multiple_assignment</code></td><td>The right side evaluates first</td><td><code>index, values[index] = 2, 99</code> landing at index 0</td></tr>
<tr><td><b>—</b></td><td><code>exercises</code></td><td>Practice</td><td>Eight predict-the-output traps</td></tr>
</table>

---

## Quick reference

### The rule that predicts everything

> A change is visible through every alias **if and only if** you **mutated** the object rather than **rebound** the name.

<table width="100%">
<tr><th align="left" width="34%">Inside a function</th><th align="left" width="20%">Caller sees it?</th><th align="left" width="46%">Why</th></tr>
<tr><td><code>items.append(4)</code></td><td><b>Yes</b></td><td>Mutates the shared object</td></tr>
<tr><td><code>items[0] = 9</code></td><td><b>Yes</b></td><td>Mutates the shared object</td></tr>
<tr><td><code>items = [9]</code></td><td><b>No</b></td><td>Rebinds the local name only</td></tr>
<tr><td><code>items += [4]</code></td><td><b>Yes</b> (mutable)</td><td><code>__iadd__</code> mutates in place</td></tr>
<tr><td><code>items = items + [4]</code></td><td><b>No</b></td><td><code>__add__</code> builds a new object</td></tr>
</table>

Python is neither pass-by-value nor pass-by-reference. It is **pass by assignment** — the parameter becomes another name for the caller's object.

### Mutable vs immutable

<table width="100%">
<tr><th align="left" width="50%">Immutable</th><th align="left" width="50%">Mutable</th></tr>
<tr><td><code>int</code>, <code>float</code>, <code>complex</code>, <code>bool</code></td><td><code>list</code></td></tr>
<tr><td><code>str</code>, <code>bytes</code></td><td><code>dict</code></td></tr>
<tr><td><code>tuple</code></td><td><code>set</code></td></tr>
<tr><td><code>frozenset</code></td><td><code>bytearray</code></td></tr>
<tr><td><code>None</code></td><td>most custom classes</td></tr>
</table>

The collections come in pairs: `list`/`tuple`, `set`/`frozenset`, `bytearray`/`bytes`.

**Immutability is shallow.** A tuple's slots are fixed, but a list inside it can still change — which also makes that tuple unhashable.

### `is` vs `==`

<table width="100%">
<tr><th align="left" width="16%">Operator</th><th align="left" width="34%">Asks</th><th align="left" width="50%">Use for</th></tr>
<tr><td><code>==</code></td><td>Same <b>value</b>?</td><td>Almost everything; a class can define it</td></tr>
<tr><td><code>is</code></td><td>Same <b>object</b>?</td><td><code>None</code>, <code>True</code>, <code>False</code>, genuine identity checks</td></tr>
</table>

`a is b` is exactly `id(a) == id(b)`. It cannot be overridden — which is why `x is None` is the correct idiom.

**Never use `is` to compare values.** CPython caches integers −5 to 256 and interns identifier-like strings, so `is` can be `True` for one literal and `False` for another. Python emits a `SyntaxWarning` if you try.

### Memory management

<table width="100%">
<tr><th align="left" width="28%">Mechanism</th><th align="left" width="24%">Handles</th><th align="left" width="48%">Timing</th></tr>
<tr><td>Reference counting</td><td>Almost everything</td><td><b>Immediate</b> — freed the moment the count hits zero</td></tr>
<tr><td>Cycle collector</td><td>Unreachable cycles</td><td><b>Periodic</b> — not deterministic</td></tr>
</table>

Reference counting cannot free cycles, because each object keeps the other's count above zero. Never rely on `__del__` — use `with` and a context manager.

### The five classic traps

<table width="100%">
<tr><th align="left" width="34%">Trap</th><th align="left" width="32%">Why it happens</th><th align="left" width="34%">Fix</th></tr>
<tr><td><code>def f(x=[])</code></td><td>Default created once, at <code>def</code> time</td><td><code>x=None</code> sentinel</td></tr>
<tr><td><code>members = []</code> on a class</td><td>One list shared by all instances</td><td>Create it in <code>__init__</code></td></tr>
<tr><td><code>[[0] * 3] * 3</code></td><td>Repeats the <b>reference</b>, not the row</td><td><code>[[0] * 3 for _ in range(3)]</code></td></tr>
<tr><td>Removing while iterating</td><td>Indices shift under the loop</td><td>Build a new list, or iterate a copy</td></tr>
<tr><td><code>list(nested)</code> as a "copy"</td><td>Shallow — inner objects still shared</td><td><code>copy.deepcopy()</code></td></tr>
</table>

### Constants

Python has none. Three approaches, in increasing strength:

<table width="100%">
<tr><th align="left" width="30%">Approach</th><th align="left" width="30%">Enforced?</th><th align="left" width="40%">Use when</th></tr>
<tr><td><code>MAX_RETRIES = 3</code></td><td>No — convention only</td><td>Almost always</td></tr>
<tr><td><code>x: Final = 3</code></td><td>Type checker only</td><td>You run mypy</td></tr>
<tr><td><code>class S(Enum)</code></td><td><b>Yes, at runtime</b></td><td>A fixed set of related values</td></tr>
</table>

Prefer immutable values for constants: `tuple` over `list`, `frozenset` over `set`, `MappingProxyType` for a read-only dict.

### Unpacking

```python
a, b = b, a                      # swap - no temporary needed
first, *rest = [1, 2, 3, 4]      # rest is always a list
name, (x, y) = ("origin", (0, 0)) # nested
value, _ = get_pair()            # _ for what you ignore
```

The right-hand side is evaluated **completely first**, which is why the swap works and why `index, values[index] = 2, 99` uses the *old* index.

---

## Key Terms

<table width="100%">
<tr><th align="left" width="24%">Term</th><th align="left" width="44%">Meaning</th><th align="left" width="32%">Where</th></tr>
<tr><td><b>Name</b></td><td>A key in a namespace dictionary</td><td>04.1</td></tr>
<tr><td><b>Object</b></td><td>The thing in memory holding the data</td><td>04.1</td></tr>
<tr><td><b>Reference</b></td><td>The arrow from a name to an object</td><td>04.2</td></tr>
<tr><td><b>Rebinding</b></td><td>Pointing a name at a different object</td><td>04.1 — invisible to aliases</td></tr>
<tr><td><b>Mutation</b></td><td>Changing an object in place</td><td>04.4 — visible to every alias</td></tr>
<tr><td><b>Pass by assignment</b></td><td>How Python passes arguments</td><td>04.2</td></tr>
<tr><td><b>Aliasing</b></td><td>Two or more names for one object</td><td>04.5</td></tr>
<tr><td><b>Identity</b></td><td><code>id(x)</code> — fixed for an object's life</td><td>04.3</td></tr>
<tr><td><b>Interning</b></td><td>Caching immutable values to share them</td><td>04.3 — why <code>is</code> surprises</td></tr>
<tr><td><b>Hashable</b></td><td>Has a stable hash — required for dict keys</td><td>04.4</td></tr>
<tr><td><b>Shallow immutability</b></td><td>Fixed slots, mutable contents</td><td>04.4 — the tuple trap</td></tr>
<tr><td><b>Reference counting</b></td><td>Freeing an object when nothing points at it</td><td>04.6 — immediate</td></tr>
<tr><td><b>Reference cycle</b></td><td>Objects keeping each other alive</td><td>04.6 — needs the collector</td></tr>
<tr><td><b>Extended unpacking</b></td><td><code>first, *rest = items</code></td><td>04.8</td></tr>
</table>

---

## Next

**Chapter 05 — Data Types: Numbers and Booleans.** Arbitrary-precision integers, why `0.1 + 0.2 != 0.3`, when to reach for `Decimal`, truthiness, and why `True` is an `int`.
