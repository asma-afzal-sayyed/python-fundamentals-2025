# Strings


- Strings are declared in `""` or `''`.
- Example: `"Hello world"`, `"Python"`, `"Asma"`, etc.
- `"12356"`, `"@#!:%"` → this is also a string.
- Anything declared in single or double quotes is a string.

---

## Positive and Negative Indexing

```python
msg = "hello world"

# Positive indexing (from starting)
print(msg[0])   # h
print(msg[1])   # e

# Negative indexing (from end)
print(msg[-1])  # d
print(msg[-2])  # l
````

---

## Slicing of String

```python
x = "Hello world"

# Slicing
print(x[0:5])   # Hello
print(x[6:])    # world
```

---

## Slicing with Step (Skip / Alternate Value)

Format: `[start : end : step]`

```python
x = "Hello world"

print(x[::2])   # Hlowrd   (skip 1 character)
print(x[::3])   # Hlwl     (skip 2 characters)
```

---

## String Operations

### Functions

There are 3 types of functions:

1. **In-Built function()**
2. **Derived function()**
3. **User-defined function()**

---

## Built-in Functions

```python
msg = "hELLO wORLD"
print(msg)               # hELLO wORLD

msgLower = msg.lower()
print(msgLower)          # hello world

msgUpper = msg.upper()
print(msgUpper)          # HELLO WORLD

msgCapital = msg.capitalize()
print(msgCapital)        # Hello world

msgTitle = msg.title()
print(msgTitle)          # Hello World

msgCase = msg.casefold()
print(msgCase)           # hello world
```

---

## Replace Function

```python
msg = "Hello world"
print(msg)   # Hello world

msg1 = msg.replace("world", "Asma")   # (old, new)
print(msg1)   # Hello Asma
```


---
[🔙 Back to Index](README.md)
