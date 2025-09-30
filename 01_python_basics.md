# Python Basics

## Variable

A **variable** is a named storage that holds a value in a program. Variables allow us to store, modify, and use data throughout the code.  

### Key Points:
- Variables have **names** and **values**.
- The **value** of a variable can change during program execution.
- In Python, you don't need to declare the type explicitly; it is **dynamically typed**.

---

## Naming Rules for Variables

When creating variables in Python, there are certain rules and conventions to follow:

### Rules:
1. Variable names **must start** with a letter (a-z, A-Z) or an underscore (_).
2. The rest of the name can contain **letters, digits (0-9), or underscores**.
3. Variable names are **case-sensitive**.  
   - Example: `age` and `Age` are different variables.
4. **Cannot use Python keywords** as variable names (e.g., `for`, `if`, `class`, etc.).

### Conventions (Good Practices):
- Use **meaningful names** that describe the value (e.g., `student_name` instead of `s`).
- Use **snake_case** for variable names in Python: `my_variable`.
- Avoid using single letters except in loops (`i`, `j`) or temporary values.

### Example:
```python
# Valid variable names
name = "Asma"
_age = 20
student_score = 95

# Invalid variable names
2name = "Asma"      # Cannot start with a number
class = "Python"    # 'class' is a reserved keyword

```

---

## Variable Types

### camelCase
The first word starts with a lowercase letter. Subsequent words begin with an uppercase letter. No spaces or punctuation are used.  
**Example:** `calculateTotalAmount`

### snake_case
All letters are lowercase, and words are separated by an underscore (`_`).  
**Example:** `calculate_total_amount`

### PascalCase
Also known as Upper Camel Case. Every word starts with an uppercase letter. No spaces or punctuation are used between words.  
**Example:** `UserAccountDetails`

---

## Escape Sequences

An escape sequence starts with a backslash (`\`) and allows you to include special characters in strings.

**Common escape sequences:**

- `\'` - Single quote  
- `\"` - Double quote  
- `\\` - Backslash  
- `\n` - New line  
- `\t` - Tab  
- `\r` - Carriage return  
- `\b` - Backspace

---

## Python Operators

### 1. Assignment Operator
`=`  

### 2. Arithmetic Operators
`+`, `-`, `*`, `/`, `//`, `%`, `**`  

**Unary Operators:** `++`, `--` (apply on one single operand)  
**Binary Operators:** `+`, `-`, `*`, `**` (apply on two operands)  

### 3. Comparison / Relational Operators
`<`, `>`, `<=`, `>=`, `==`, `!=`  

### 4. Logical Operators
`AND`, `OR`, `NOT`, `NAND`, `XOR`  

### 5. Identity Operators
`is`, `is not`  

### 6. Membership Operators
`in`, `not in`  

---

## String and Integer Concatenation

Python can't directly concatenate a string and an integer.  

**Example:**

```python
"Asma" + 10
```
**Error:**
```python
TypeError: can only concatenate str (not "int") to str
```

**Explanation:**

* `"Asma"` is a string.
* `10` is an integer.
* Python does not automatically convert between strings and integers for concatenation, so this operation fails.

---

## Using the `eval()` Function

The `eval()` function can be used to **convert a string that represents a number into an integer**.
This allows arithmetic operations to be performed successfully.

---

## Example with `eval()`

```python
# String representing a number
x = "10"

# Integer
y = 10

# Convert string x to integer using eval()
x1 = eval(x)

# Add the two integers
sum1 = x1 + y

# Print the result
print(sum1)
```

**Output:**

```
20
```
## Step-by-Step Explanation

1. `x = "10"`  
   Here, `x` is a string containing the number `"10"`.

2. `y = 10`  
   `y` is an integer.

3. `x1 = eval(x)`  
   The `eval()` function evaluates the string `"10"` as a Python expression and converts it into the integer `10`.

4. `sum1 = x1 + y`  
   Now that both `x1` and `y` are integers, addition is possible.  
   `10 + 10` equals `20`.

5. `print(sum1)`  
   Outputs the result `20`.

---

## ASCII (American Standard Code for Information Interchange)

ASCII is a standard for representing characters as numerical values.

## Checking ASCII Values

```python
print(chr(65))  # Output: A
print(chr(97))  # Output: a
````

* `chr()` function converts an **ASCII value** to its corresponding **character**.
* Example: `65` → `'A'`, `97` → `'a'`.

---

## Checking Data Type

You can check the type of any data in Python using `type()`:

```python
print('Hello world')
print(type("Hello world"))
```

**Output:**

```
Hello world
<class 'str'>
```

* `type()` returns the **class/type** of the data.
* Here, `"Hello world"` is of type `str` (string).



---
[🔙 Back to Index](README.md)

