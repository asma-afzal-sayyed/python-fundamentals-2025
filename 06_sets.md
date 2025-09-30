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

---
[🔙 Back to Index](README.md)
