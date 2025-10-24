# Loops

### `for` loop

- A **`for` loop** is used for iterating over a sequence (that is either a list, a tuple, a dictionary, or a string).
- This is less like the `for` keyword in other programming languages, and works more like an **iterator method** as found in other object-oriented programming languages.
- With the `for` loop we can execute a set of statements once for each item in a list, tuple, set, etc.
- The `for` loop does not require an indexing variable to be set beforehand.

### Syntax of `for` loop

```python
for variable in sequence:
    # block of code
else:
    # optional block (executes if the loop finishes without `break`)
```

---

**Example 1: Iterating over a string using `range(len())`**

```python
name = "Asma"
for i in range(len(name)):
    print(i, name[i])
````

**Output:**

```
0 A
1 S
2 M
3 a
```

**Example 2: Iterating directly over a string**

```python
name = "Asma"
for i in name:
    print(i)
```

**Output:**

```
A
S
m
a
```

---

### `range()` function

* It is helpful to think of the **`range` object** as an ordered list.
* To loop through a set of code a specified number of times, we can use the **`range()` function**.
* The `range()` function returns a sequence of numbers, starting from **0** by default, and increments by **1** (by default), and ends at a specified number.

**Example: Using `range()`**

```python
for i in range(10):
    print(i)
```

**Output:**

```
0
1
2
3
4
5
6
7
8
9
```

---

### `while` loop

* The **`while` loop** is used to execute a set of statements as long as the condition is true.
* **Note:** Remember to **increment** `i`, or else the loop will continue forever.
* The `while` loop requires relevant variables to be ready, in this example we need to define an indexing variable, `i`, which we set to **0**.
* `while` is the keyword for `while` loop.
* In these loops, we can't use `range()`.

**Syntax:**

```python
while (condition):
    statement
    statement
else:
    execute statement
    increment/decrement
```

**Example:**

```python
i = 0
j = 11
while i < j:
    print(i)
    i = i + 1
```

**Output:**

```
0
1
2
3
4
5
6
7
8
9
10
```

## 📓 Jupyter Notebook
You can view the runnable code in the notebook:  
[**Conditions in Python**](./Notebook/Loops_in_Python.ipynb)

Or run it directly in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asma-afzal-sayyed/python-fundamentals-2025/blob/main/Notebook/Loops_in_Python.ipynb)

---
[🔙 Back to Index](README.md)
