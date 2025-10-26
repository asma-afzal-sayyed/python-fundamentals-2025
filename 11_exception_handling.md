# Exception Handling

An **exception** is an event that occurs during the execution of a program, disrupting the normal flow of instructions. When a Python script encounters a situation it can't cope with, it raises an exception. An exception is a Python object that represents an error.

When a Python script raises an exception, it must either handle it immediately; otherwise, the program terminates and quits.

If you have some suspicious code that may raise an exception, you can defend your program by placing the code inside a `try:` block. After the `try:` block, include an `except:` statement followed by a block of code that handles the problem as elegantly as possible.

---

## Common Exceptions

- `ZeroDivisionError`
- `NameError`
- `ValueError`
- `EOFError`
- `IndentationError`
- `KeyError`
- `TypeError`

---

## Steps of `try` and `except`

1. **Start with try block:** Python first enters the `try` block and executes the code inside.  
2. **If no error occurs:**  
   - The `except` block is skipped.  
   - Program continues normally after `try`.  
3. **If an error occurs inside `try`:**  
   - Python immediately jumps out of the `try` block.  
   - It looks for a matching `except` block.  
4. **Find matching `except`:**  
   - If a matching `except` block exists, it runs.  
   - If no matching `except` is found, the program crashes.  
5. **After handling:**  
   - Once the `except` block finishes, the program continues with the next lines of code.  

> If an error occurs, any lines after it will not execute unless handled with `try` and `except`.

---

## Specific Exception Types and Handling

### ZeroDivisionError

Occurs when dividing a number by zero.

**Example (Unprotected):**
```python
print(1/0)
# Output: ZeroDivisionError
# No lines after this will be executed
````

**Example (Protected):**

```python
try:
    1/0
except ZeroDivisionError:
    print("It gives ZeroDivisionError")

print('Hello')
# Output:
# It gives ZeroDivisionError
# Hello
```

---

### TypeError

Occurs when performing an invalid operation between incompatible types (e.g., string + int).

**Example (Unprotected):**

```python
x = int(input("Enter any value:"))
y = input("Enter any string value:")
z = x + y
print(z)
# Output: TypeError
```

**Example (Protected):**

```python
x = int(input("Enter number"))
y = input("Enter string")
try:
    z = x + y
    print(z)
except TypeError:
    print("This code gives TypeError")
```

---

### IndexError

Occurs when accessing a list index that is out of range.

**Example (Protected):**

```python
list1 = [10, 20, True, False, 'apple']
try:
    list1[5]
except IndexError:
    print("This code gives IndexError")
```

---

### KeyError

Occurs in dictionaries when the specified key is not found.

**Example (Unprotected):**

```python
dict1 = dict(name="Asma", age=20)
dict1['address']
# Output: KeyError: 'address'
```

**Example (Protected):**

```python
dict1 = dict(name='Asma', age=20)
try:
    dict1['address']
except KeyError:
    print("This code gives a KeyError")
```

---

### NameError

Occurs when using a variable, function, or object that hasn't been defined.

**Example (Unprotected):**

```python
x = 10
print(x)
print(y)
# Output: NameError: name 'y' is not defined
```

**Example (Protected):**

```python
list2 = []
try:
    print(list2 + 2)
except NameError:
    print("It gives a NameError")
```

> Note: This example may actually raise a `TypeError` since adding a list and integer is invalid.

---

## Multiple and Default Except Blocks

### Multiple Except Blocks

Python allows multiple `except` blocks to handle different types of errors separately.

**Example:**

```python
try:
    num1 = int(input("Enter a number:")) 
    num2 = int(input("Enter a 2nd number:"))
    value = num1 / num2
    print("Answer is:", value)
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("You should enter only numbers!")
except:  # Default except
    print("Something went wrong")
```

---

### Default Except

A default `except` block catches all exceptions.

**Example:**

```python
try:
    num = int(input("Enter a number"))
    print(10 / num)
except:
    print("Something went wrong")
```

* If input is `0` → `ZeroDivisionError` is caught
* If input is `'abc'` → `ValueError` is caught
* If no error → `except` block is skipped

---

## The `try-except-else-finally` Structure

### `try-except-else`

* `else` block runs only if no exception occurs.

**Example:**

```python
try:
    num1 = float(input("Enter a number"))
    num2 = float(input("Enter a 2nd number"))
    value = num1 / num2
except ZeroDivisionError:
    print("This code gives ZeroDivisionError") 
except ValueError:
    print("You should enter only numbers!")
except:
    print("Something went wrong")
else:
    print("Division successful! Answer is=", value)
```

---

### `finally` Block

* Runs always, whether an exception occurs or not.

**Full Structure:**

```python
try:
    # code
except SomeError:
    # code runs if exception occurs
else:
    # runs if no exception occurs
finally:
    # runs always
```

* If input is valid → `else` runs, then `finally`.
* If an error occurs → `except` runs, then `finally`.
* `finally` ensures cleanup or final statements always execute.


```

## 📓 Jupyter Notebook
You can view the runnable code in the notebook:  
[**Exception_Handling in Python**](./Notebook/Exception_Handling_in_Python.ipynb)

Or run it directly in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asma-afzal-sayyed/python-fundamentals-2025/blob/main/Notebook/Exception_Handling_in_Python.ipynb)

---
[🔙 Back to Index](README.md)
