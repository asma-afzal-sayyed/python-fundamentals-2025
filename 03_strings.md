# Strings

Strings are declared in **single** (`' '`) or **double** (`" "`) quotes.  
Anything declared in quotes is considered a **string**.

Example:
```python
msg = "Hello world"
name = 'Python'
person = "Asma"
````

Other examples:

```python
"12356"
"@#$%^&*()"
```

---

## Positive and Negative Indexing

Python allows accessing characters of a string using both **positive indexing (from start)** and **negative indexing (from end)**.

```python
msg = "hello world"

# Positive indexing (from start)
print(msg[0])   # h
print(msg[1])   # e

# Negative indexing (from end)
print(msg[-1])  # d
print(msg[-2])  # l
```

---

## Slicing of String

Slicing is used to extract parts of a string.

```python
x = "Hello world"

print(x[0:5])   # 'Hello'  → from index 0 to 4
print(x[6:])    # 'world'  → from index 6 to end
```

---

## Slicing with Step (Skip / Alternate Values)

Format:

```
[start : end : step]
```

Examples:

```python
x = "Hello world"

print(x[::2])   # 'Hlowrd'  → skips alternate characters
print(x[::3])   # 'Hlwl'    → skips 2 characters each time
```

---

## String Operations

### Functions in Strings

There are 3 types of functions:

1. **In-Built functions** (e.g., `len()`, `max()`, `min()`)
2. **Derived functions** (string-specific methods like `upper()`, `lower()`, `split()`)
3. **User-defined functions** (custom functions made by programmer)


### Built-in Functions

-----

```python
msg = "HELLO WORLD"
print(msg) 
# The output will be the same as the variable.
# >> HELLO WORLD
````

```python
msglower = msg.lower()
print(msglower)
# Converts all characters in the string to lowercase.
# >> hello world
```

```python
msgupper = msg.upper()
print(msgupper)
# Converts all characters in the string to uppercase.
# >> HELLO WORLD
```

```python
msgcapital = msg.capitalize()
print(msgcapital)
# Capitalizes the first character of the string.
# >> Hello world
```

```python
msgtitle = msg.title()
print(msgtitle)
# Capitalizes the first letter of each word in the string.
# >> Hello World
```

```python
msgcase = msg.casefold()
print(msgcase)
# Converts string to lowercase, similar to .lower() but more aggressive.
# >> hello world
```

---

### The `.find()` Method

---

The `.find()` method returns the index of the first occurrence of a substring. If the substring is not found, it returns `-1`.

```python
x = "Hello Asma Sayyed"

# Find the index of the substring "Hi".
print(x.find("Hi"))
# >> -1 
# The substring was not found.

# Find the index of the substring "hello".
print(x.find("hello"))
# >> -1
# The substring "hello" was not found (case-sensitive).

# Find the index of the substring "Asma".
print(x.find("Asma"))
# >> 6
# "Asma" is found starting at index 6.

# Find the index of the first occurrence of "a".
print(x.find("a"))
# >> 9
# "a" is found at index 9.

# Find the index of the substring "ay".
print(x.find("ay"))
# >> 12
# "ay" is found starting at index 12.
```

---

### The `len()` Function

---

The `len()` function returns the length of a string, counting from 1.

```python
# Example:
x = "Hello.Asma"
print(len(x))

# >> 10
# The string "Hello.Asma" has a length of 10 characters.
```

---

### The `.format()` and `.replace()` Methods

---

**Difference between `.format()` and `.replace()`**

* **`.replace()`**: Replaces all occurrences of an old value with a new value.
* **`.format()`**: Replaces a specified placeholder (written in `{}` brackets) with a new value.

---

#### `.format()`

```python
# Example 1:
msg = "Hello {world}"
print(msg.format(world = 'Jadhav'))

# >> Hello Jadhav
# Replaces the placeholder `{world}` with 'Jadhav'.

# Example 2:
print(msg.format(world = 'Asma'))

# >> Hello Asma
# Replaces the placeholder `{world}` with 'Asma'.
```

#### `.replace()`

```python
# Example 1:
x = "Hello world"
print(x.replace('o', "a"))

# >> Hella warld
# Replaces all occurrences of 'o' with 'a'.

# Example 2:
msg1 = msg.replace('world', 'Asma')
print(msg1)

# >> Hello Asma
# Replaces the substring 'world' with 'Asma'.
```


---
[🔙 Back to Index](README.md)
