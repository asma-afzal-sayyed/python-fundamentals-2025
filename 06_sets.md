# Sets

- Set is one of 4 built-in data types in Python, used to store collections of data, including **tuples, dictionaries, sets**.
- Sets are **unordered**, but you can remove items and add new items.
- Set elements are **unique**; duplicate elements are not allowed.
- A set itself may be modified, but the elements contained in the set must be **immutable type**.
- Sets are used to store multiple items in a single variable.
- You can denote a set with a pair of curly brackets `{}`.

---

### Important Notes
- Both **set** and **dictionary** are denoted by curly brackets `{}`.
- If we create an empty set by writing `{}` only, then it will always give output as a **dictionary**.

```python
x = {}
print(x, type(x))
````

**Output:**

```python
{} <class 'dict'>
```

---

### Creating an Empty Set

If we want to create an empty set, we should create it like this:

```python
x = set()
print(type(x))
```

**Output:**

```python
<class 'set'>
```

---

### Properties of Sets

* A set has **no index value**.
  Example:

  ```python
  set1 = {10}
  print(set1[0])   # ❌ Error
  ```
* We can add **tuple, dictionary, as well as sets** in the set.
  But we **cannot add list** inside the set.
* We cannot add elements using index value in the set because index values do not apply.
* To add an element in a set, we use **`.add()`**.
* If we add the same element again, nothing will happen because the set accepts **no duplicate values**.

Example:

```python
x = {'Hello', 20, False, 'Python', 200}
x.add('Asma')
print(x)
```

**Output (order may vary):**

```python
{'Hello', 20, 'Asma', False, 'Python', 200}
```

Note: `'Asma'` will add **anywhere in the set** because indexing is not allowed.

---

## Set Methods

### 1. `update()`

* `update()` is used to update a set with multiple elements.

```python
x = {6, 7, 8, 9}
print(x)

x.update({6, 7, 8, 'Asma'})
print(x)
```

**Output:**

```python
{8, 9, 6, 7}
{6, 7, 8, 9, 'Asma'}
```

---

### 2. `remove()`

* `remove()` is used to remove an element from the set.

```python
x = {6, 7, 8, 9, 'Asma'}
x.remove('Asma')
print(x)
```

**Output:**

```python
{6, 7, 8, 9}
```

---

### 3. `pop()`

* `pop()` deletes a random element from the set (since sets are unordered).

```python
x = {6, 7, 8, 9}
x.pop()
print(x)
```

**Possible Output:**

```python
{6, 7, 8}
```

*(Note: The removed element may vary as sets are unordered.)*

---

### `discard()`

- `discard()` is used to **remove an element from a set**.  
- `discard()` removes the element if it exists in the set.  
- If the element is **not present**, it does **NOT raise an error** (unlike `remove()` which raises a `KeyError`).  
- Works only on sets.  

**Example 1:**

```python
X = {1, 2, 3, 4, 5, 8}
X.discard(5)
X
# >> {1, 2, 3, 4, 8}
````

**Example 2 (Discarding a non-existent element):**

```python
X.discard(5)  # If we again discard(5) it will not give an error.
# >> {1, 2, 3, 4, 8}
```

---

## Set Logic Operations

Logic Operations apply on sets.

1. **Union** (`|` operator): returns all unique values.

   ```python
   set1 = {'Hello', 3.14, 10, True}
   set2 = {3.14, True, 2025, False}
   set1.union(set2)
   # >> {10, 2025, 3.14, False, True, 'Hello'}
   ```

2. **Intersection** (`&` operator): returns only duplicate values (common elements).

   ```python
   set1 = {'Hello', 3.14, 10, True}
   set2 = {3.14, True, 2025, False}
   print(set1.intersection(set2))
   # >> {True, 3.14}

   # Alternative using the '&' operator
   set2 & set1
   # >> {True, 3.14}
   ```

3. **Difference** (`-` operator): subtract one set from another.

   ```python
   set4 = {'Hello', 3.14, 10, True}
   set5 = {3.14, True, False, 2025}
   print(set4.difference(set5))
   print(set5.difference(set4))

   # >> {'Hello', 10}
   # >> {False, 2025}

   # Alternative using the '-' operator
   set4 - set5
   # >> {'Hello', 10}

   set5 - set4
   # >> {False, 2025}
   ```

4. **Symmetric Difference** (`^` operator): elements present in *either* set, but not in both.

   ```python
   set1 = {'Hello', 3.14, 10, True}
   set2 = {3.14, True, False, 2025}
   set1.symmetric_difference(set2)
   # >> {10, 2025, False, 'Hello'}
   ```

---

## Set Utility Functions

### `clear()`

* Removes all elements in the set and returns an **empty set**.

```python
set = {1, 2, 3, 6}
set.clear()
set
# >> set()  # empty set
```

---

## `issubset()` and `issuperset()`

Both methods always return a **boolean value** (`True` / `False`).

### `issubset()`

* Checks whether **all elements of one set are present in another set**.

```python
A = {1, 2}
B = {1, 2, 3, 4}
print(A.issubset(B))
print(B.issubset(A))

# >> True   # all elements of A present in B.
# >> False  # all elements of B not present in A.
```

> **Note:** `issubset()` → smaller set checking if it is inside a bigger set.

---

### `issuperset()`

* Checks whether a set **contains all elements of another set**.

```python
A = {1, 2}
B = {1, 2, 3, 4}
print(A.issuperset(B))
print(B.issuperset(A))

# >> False  # A does not contain all of B
# >> True   # B contains everything in A
```

> **Note:** `issuperset()` → bigger set checking if it contains a smaller set.

---

## Aggregate Functions

Aggregate functions apply to sets (and other iterable types):

* `min()`, `max()`, `sum()`, `len()`, `average()` (requires calculation).

```python
a = {1, 5, 2, 3, 4, 7}
print("Sum:", sum(a))
print("Minimum:", min(a))
print("Maximum:", max(a))
print("Length:", len(a))
print("Average:", sum(a) / len(a))

# >> Sum: 22
# >> Minimum: 1
# >> Maximum: 7
# >> Length: 6
# >> Average: 3.6666666666666665
```

---
[🔙 Back to Index](README.md)
