# Functions

In **Python**, a function is a group of related statements that performs a **specific task**. Functions help break our program into smaller and modular chunks. As our program grows larger and larger, functions make it more organized and manageable. Furthermore, it avoids **repetition** and makes the code **reusable**.

---

## Types of Functions

- **Pre-defined functions** (built-in functions)  
- **User-defined functions**

---

## Function Definition and Components

- In Python, a function is defined using the `def` keyword followed by the function name and parentheses `()`. The keyword `def` marks the start of the function header.  
- A **function name** to uniquely identify the function. Function naming follows the same rule of writing identifiers in Python.  
- **Parameters (arguments)** through which we pass values to a function. They are optional.  
- A **colon (:)** to mark the end of the function header.  
- Optional **documentation string (docstring)** to describe what the function does.  
- Statements must have the same **indentation level** (usually 4 spaces or 1 tab).  
- An optional **return statement** to return a value from the function.  

### Types of User-Defined Functions

Functions can be classified based on parameters and return values:

- **Function with parameters** (parameterized function)  
- **Function without parameters** (non-parameterized function)  
- **Function with return value**  
- **Function without return value**

---

## Variables (Local and Global)

- The input to a function is called a **formal parameter**.  
- A variable that is declared **inside** a function is called a **local variable**.  
- The parameter only exists **within the function** (i.e., the point where the function starts and stops).  
- A variable that is declared **outside** a function definition is a **global variable**, and its value is accessible and modifiable throughout the program.  

### Example: Global and Local Variables

```python
a = 10  # (Global variable)

def val():
    x1 = 15  # (Local variable)
    print(x1)
    print(a)

val()
```

**Output:**

```
>> 15
>> 10
````

---

## Parameterized Function with Return Value

### Example 1

```python
def process(x):
    y1 = x - 8
    y2 = x + 8
    y3 = x * 8
    y4 = x / 8
    y5 = x % 8
    return y1, y2, y3, y4, y5

process(8)
# Output: (0, 16, 64, 1.0, 0)

process(10)
# Output: (2, 18, 80, 1.25, 2)
```

### Example 2: Function with Multiple Parameters

```python
def multi(x, y):
    z = 2 * x + 5 * y + 45
    return z

ans = multi(3.14, 1.618)
ans
```

**Output:**

```
>> 59.370000000000005
```

---
[🔙 Back to Index](README.md)
