# Lists

## Data Structure (DSA) Overview

A diagram shows a breakdown of Data Structures:

# Data Structures Breakdown

| Category       | Sub-Category | Type     | Examples                                    |
|----------------|--------------|----------|---------------------------------------------|
| **Primitive**  | –            | –        | `int`, `float`, `char`, `double`, `boolean` |
| **Non-Primitive** | **Linear** | **Static**  | `Array` (`list`)                             |
|                |              | **Dynamic** | `Stack` (`LIFO`), `Queue` (`FIFO`), `LinkedList` |
|                | **Non-Linear** | –        | `Tree`, `Graph`, `Hash[table]`              |



---

## List in Python

- **List are ordered.**
- List can contain **any object**.
- List element can be accessed by **index value**.
- Lists are **mutable** data type in python.
- Lists item written within a **`[ ]` square bracket**.

**Example:**

```python
X = []
print(X, type(X))
````

**Output:**

```
[] <class 'list'>
```

---

## List Indexing and Slicing

**Indexing Examples:**

```python
x1 = ['python', 3.147, 50, True, False]
print(x1[0])
print(x1[2])
```

**Output:**

```
>> python
>> 50
```

**Negative Indexing Examples:**

```python
print(x1[-1])
print(x1[-3])
```

**Output:**

```
>> False
>> 50
```

**Slicing of list element:**

```python
x1[1:3]
```

**Output:**

```
>> [3.147, 50]
```

```python
x1[:4] # n-1 = 4-1 = 3 (3 skip)
```

**Output:**

```
>> ['python', 3.147, 50, True]
```

**Task (point out Asma Sayyed from list):**

```python
X = ['py', [[10, 20, 'Python']], [0], [['Ashwini']], ['Aditya']], [[['S', 'Shankarshan']]], ['Asma Sayyed'], ['Hawaldar']]
print(X[3][0][1])
```

**Output:**

```
>> Asma Sayyed
```

---

## List Operations

### Mutability and Deletion

* List is a **mutable** data type, meaning we can add, delete, and update in list.
* List are **LIFO (Last In First Out)** → *Correction: This LIFO definition is for a Stack, not a standard List.*

For deleting elements in a list, there are 2 functions: `del()` and `pop()`.

### 1. `del()`

* Used to **delete whole list** or an **element by index**.

```python
x = ['Hello', True, False, 10, 20, 11.0]
del(x[2])
print(x)
```

**Output:**

```
>> ['Hello', True, 10, 20, 11.0]
```

*Note: `del(x)` would delete the entire list.*

### 2. `pop()`

* Used to **remove one element at a time**.
* It removes the **last element** by default and returns the value.

```python
x = ['Hello', True, False, 10, 20, 50]
x.pop() # It remove last element
```

**Output:**

```
>> 50
```

---

## Adding to a List

Adding in list: [`append`, `extend`, `insert`]

### 1. `append()`

* It adds **one element at a time** at the **last position**.

```python
x = ['Hello', 10, 20, 30]
x.append('Asma')
print(x)
```

**Output:**

```
>> ['Hello', 10, 20, 30, 'Asma']
```

### 2. `extend()`

* Adds **multiple elements at a time**. It takes an iterable (like another list).

```python
x.extend(['Apple', 'banana'])
print(x)
```

**Output:**

```
>> ['Hello', 10, 20, 30, 'Asma', 'Apple', 'banana']
```

### 3. `insert()`

* `insert` takes **two arguments**: the **first is the position** of the element, and the **second is the value**.

```python
x.insert(0, 'Python')
print(x)
```

**Output:**

```
>> ['Python', 'Hello', 10, 20, 30, 'Asma', 'Apple', 'banana']
```

---

## String Method

### `split()`

* **`split()`** converts a **string into a list** (using a specified or default delimiter, usually a space).

```python
X = 'My name is Asma'
X.split()
```

**Output:**

```
>> ['My', 'name', 'is', 'Asma']
```

---
[🔙 Back to Index](README.md)
