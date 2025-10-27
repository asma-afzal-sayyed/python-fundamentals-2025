# 🐍 Predefined / Built-in Functions in Python

Python provides **69 built-in functions** that can be used directly without importing any library.

---

## 🔹 1. Type Conversion Functions
Used to convert one data type into another.

| Function | Description |
|-----------|--------------|
| `int()` | Converts value to an integer. |
| `float()` | Converts value to a float (decimal). |
| `tuple()` | Converts an iterable into a tuple. |
| `set()` | Converts an iterable into a set. |
| `bool()` | Converts a value to `True` or `False`. |
| `list()` | Converts an iterable into a list. |
| `dict()` | Creates a dictionary. |
| `chr()` | Returns character from Unicode code. |
| `str()` | Converts a value to a string. |
| `complex()` | Creates a complex number. |
| `bytes()` | Creates an immutable byte sequence. |
| `ascii()` | Returns a readable version of an object using ASCII. |
| `repr()` | Returns a printable string representation of an object. |
| `bin()` | Converts number to binary string. |
| `oct()` | Converts number to octal string. |
| `frozenset()` | Creates an immutable set. |
| `hex()` | Converts number to hexadecimal string. |
| `ord()` | Returns Unicode code of a character. |
| `bytearray()` | Creates a mutable byte sequence. |
| `memoryview()` | Returns a memory view object. |

---

## 🔹 2. Mathematical Functions

| Function | Description |
|-----------|--------------|
| `abs()` | Returns the absolute value. |
| `divmod()` | Returns quotient and remainder as a tuple. |
| `max()` | Returns the largest value. |
| `min()` | Returns the smallest value. |
| `pow()` | Returns power of a number (`x**y`). |
| `round()` | Rounds a number to given decimals. |
| `sum()` | Returns sum of all items in an iterable. |

---

## 🔹 3. Iterables & Iterators

| Function | Description |
|-----------|--------------|
| `len()` | Returns length of an object. |
| `range()` | Returns a sequence of numbers. |
| `iter()` | Returns iterator object. |
| `sorted()` | Returns a sorted list. |
| `next()` | Returns next item from an iterator. |
| `filter()` | Filters elements using a function. |
| `map()` | Applies a function to all items. |
| `all()` | Returns `True` if all elements are true. |
| `reversed()` | Returns reversed iterator. |
| `enumerate()` | Returns index and value pairs. |
| `zip()` | Combines iterables element-wise. |
| `any()` | Returns `True` if any element is true. |

---

## 🔹 4. Object & Class Related

| Function | Description |
|-----------|--------------|
| `classmethod()` | Converts method to a class method. |
| `staticmethod()` | Defines a static method in class. |
| `property()` | Creates a property in class. |
| `type()` | Returns type of an object. |
| `super()` | Refers to parent class. |
| `isinstance()` | Checks if object is instance of a class. |
| `callable()` | Returns `True` if object is callable. |
| `id()` | Returns unique ID of an object. |
| `issubclass()` | Checks if class is subclass of another. |
| `object()` | Creates a base object. |

---

## 🔹 5. Attributes & Reflection (Introspection)

| Function | Description |
|-----------|--------------|
| `getattr()` | Returns attribute value of object. |
| `setattr()` | Sets attribute value. |
| `hasattr()` | Checks if object has an attribute. |
| `delattr()` | Deletes attribute. |
| `vars()` | Returns `__dict__` of an object. |
| `dir()` | Returns all attributes and methods. |
| `locals()` | Returns local symbol dictionary. |
| `globals()` | Returns global symbol dictionary. |

---

## 🔹 6. Input / Output Functions

| Function | Description |
|-----------|--------------|
| `print()` | Displays output on screen. |
| `input()` | Takes input from user. |
| `open()` | Opens file and returns file object. |
| `format()` | Formats string with placeholders. |

---

## 🔹 7. Code Execution & Compilation

| Function | Description |
|-----------|--------------|
| `eval()` | Executes a string expression. |
| `exec()` | Executes Python code dynamically. |
| `compile()` | Compiles source into code object. |
| `help()` | Displays documentation/help. |
| `breakpoint()` | Enters debugger mode. |
| `__import__()` | Imports module by name. |

---

## 🔹 8. Constants & Special Functions

| Function | Description |
|-----------|--------------|
| `hash()` | Returns hash value of an object. |
| `slice()` | Creates a slice object used for slicing sequences. |

---

✅ **Summary:**  
These built-in functions make Python powerful and flexible, allowing you to perform conversions, math operations, object handling, I/O, and dynamic code execution efficiently.

---

📘 **Tip:**  
You can list all built-in functions in Python using:
```python
import builtins
print(dir(builtins))
```

---
[🔙 Back to Index](README.md)
