# Python Basics

## Variable

A **variable** is a named storage that holds a value in a program. Variables allow us to store, modify, and use data throughout the code.  

### Key Points:
- Variables have **names** and **values**.
- The **value** of a variable can change during program execution.
- In Python, you don't need to declare the type explicitly; it is **dynamically typed**.


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


---
[🔙 Back to Index](README.md)
