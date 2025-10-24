# Conditions

### Comparison Operators

- Less than (`<`)
- Greater than (`>`)
- Less than or equal to (`<=`)
- Greater than or equal to (`>=`)
- Equal to (`==`)
- Not equal to (`!=`)

---

### Branching (Decision Making)

- Decision making is required when we want to execute a code only if a certain condition is satisfied. The `if/elif/else` statement is used in Python for decision making.

- An `else` statement can be combined with an `if` statement.  
It contains the block of code that executes if the conditional expression in the `if` statement resolves to `0` or a **False** value. The `else` statement is optional, and there can be at most one `else` statement following it.

- The **`elif`** statement allows you to check multiple expressions for **True** and execute a block of code as soon as one of the conditions evaluates to **True**. Like `else`, it is optional.  

- Operators always return a **boolean** value.

```python
val = 1.618
print(val > 20)
```

**Output:**

```
>> False
```

---

### 1. `if` statement

```python
age = 4
if (age > 5):
    print("You can go to primary school.")
```

In an `if` statement, if the condition is **True**, it executes the `print` statement; otherwise, it does nothing.

---

### 2. `if-else` statement

```python
age = 5
if (age > 5):
    print("You can go to primary school.")
else:
    print("You are a kid")
```

Here, if the condition is **True**, it executes the `if` block; otherwise, it executes the `else` block.

---

### 3. `if-elif-else` statement

First it checks the `if` condition, then `elif`, then `else`. You can use any number of `elif` statements.

```python
age = 5
if (age > 5):
    print("You can go to primary school")
elif (age == 5):
    print("You can go to kindergarten")
else:
    print("You are a kid")
```

**Output:**

```
>> You can go to kindergarten.
```

---

### Example of `if-elif-else` condition

```python
user = int(input("Enter any value from 0 to 6:"))
if user == 0:
    print("Sunday")
elif user == 1:
    print("Monday")
elif user == 2:
    print("Tuesday")
elif user == 3:
    print("Wednesday")
elif user == 4:
    print("Thursday")
elif user == 5:
    print("Friday")
elif user == 6:
    print("Saturday")
else:
    print("Invalid input")
```

**Output:**

```
>> Enter any value from 0 to 6: 5
Friday
```
---

### Nested `if-else`

Nested `if-else` means having one `if` (or `elif` or `else`) statement inside another. It's useful when you need to check multiple conditions step by step.

### Example:

```python
marks = int(input("Enter your marks:"))
if marks >= 50:
    if marks >= 90:
        print("Grade A")
    elif marks >= 75:
        print("Grade B")
    else:
        print("Grade C")
else:
    print("Fail")
```

## 📓 Jupyter Notebook
You can view the runnable code in the notebook:  
[**Conditions in Python**](./Notebooks/Conditions_in_Python.ipynb)

Or run it directly in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asma-afzal-sayyed/python-fundamentals-2025/blob/main/Notebooks/Conditions_in_Python.ipynb)


---
[🔙 Back to Index](README.md)
