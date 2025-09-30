# Dictionaries

- Dictionaries are used to store data values in **key:value pairs**.  
- A dictionary is a collection that is **ordered**, **changeable**, or **mutable** and does not allow **duplicate** keys.  
- Dictionary items are printed in key:value pairs and can be referred to by using the key name.  
- Dictionaries are **changeable**, meaning that we can **change, add, or remove** items after the dictionary has been created.  
- Dictionaries can't have two items with the same key.  
- A dictionary can be **nested** and can contain another dictionary.  

Example:  

| **Key** | **Values**   |
|---------|--------------|
| 'name'  | 'John'       |
| 'age'   | 25           |
| 'city'  | 'New York'   |

---

## Dictionary Access and Functions

### Dictionary Creation Example

```python
dict = {'name': 'Asma', 'age': 20, 'city': 'Pune'}
print(dict)
````

**Output:**

```
`{'name': 'Asma', 'age': 20, 'city': 'Pune'}`

* The dictionary is enclosed in curly brackets `{ }`.
* Each key is separated from its value by a **colon ( : )**, and **commas ( , )** are used to separate the items.
```

---

### Accessing Values by Key

```python
print(dict['name'])
print(dict['age'])
```

**Output:**

```
Asma
20
```

---

### `keys()` function

* Returns all keys of the dictionary.

```python
dict.keys()
```

**Output:**

```
`dict_keys(['name', 'age', 'city'])`
```

---

### `values()` function

* Returns all values of the dictionary.

```python
dict.values()
```

**Output:**

```
`dict_values(['Asma', 20, 'Pune'])`
```

---

### `items()` function

* Returns both keys & values as pairs.

```python
dict.items()
```

**Output:**

```
`dict_items([('name', 'Asma'), ('age', 20), ('city', 'Pune')])`
```

---

## Dictionary Manipulation Methods

### Adding a New Key:Value Pair

```python
dict['Phno'] = "1003568901"
dict
```

**Output:**

```
`{'name': 'Asma', 'age': 20, 'city': 'Pune', 'Phno': '1003568901'}`
```

### Updating an Existing Value

```python
dict['Phno'] = '1234'
dict
```

**Output:**

```
`{'name': 'Asma', 'age': 20, 'city': 'Pune', 'Phno': '1234'}`
```

---

### `pop()` function

* Deletes both key & value of a given key.

```python
dict.pop('Phno')
dict
```

**Output:**

```
'1234'
{'name': 'Asma', 'age': 20, 'city': 'Pune'}
```

---

### `popitem()` function

* Removes the **last inserted element**.

```python
dict.popitem()
dict
```

**Output:**

```
('city', 'Pune')
{'name': 'Asma', 'age': 20}
```

---

## Specialized Dictionary Functions

### `get()` function

- The `get()` function is used to **safely access values** in a dictionary.  
- It **checks if a key is valid or not**.  



### Direct Key Access vs `get()`

- If we directly access a key using `dict["name"]`, it:  
  - Returns the value if the key exists.  
  - Raises an **error** if the key does not exist.  

Example:  

```python
dict = {"name": "Asma", "age": 20}

print(dict["name"])   # ✅ Works, key exists
print(dict["city"])   # ❌ Raises KeyError
````



### Using `get()`

* The `get()` function provides a safer way to check if a key exists.
* It **doesn't raise an error** if the key is not found in the dictionary.
* Instead, it returns `None` (or a default value if provided).

Example:

```python
dict = {"name": "Asma", "age": 20}

print(dict.get("name"))   # ✅ Returns 'Asma'
print(dict.get("city"))   # ✅ Returns None (no error)
```



### Providing a Default Value

* We can also specify a default value if the key is missing.

```python
dict = {"name": "Asma", "age": 20}

print(dict.get("city", "Not Found"))   # Returns 'Not Found'
```

---

### `fromkeys()` function

- If we want to create a dictionary only with **keys** and assign values as empty,  
  we **cannot** do it directly like this:

```python
# ❌ Invalid syntax
dict = {'name': }
````

* This will give a **SyntaxError**.

### Using `fromkeys()`

* For empty values, we use the **`fromkeys()`** function.
* It returns a **new dictionary** with a sequence of items as keys, and all values are assigned with `None` by default.

### Example:

```python
keys = {'a', 'b', 'c'}
x = dict.fromkeys(keys)
print(x)
```

**Output:**

```
{'a': None, 'b': None, 'c': None}
```

### Assigning Values Later

* We can update any key’s value after creation.

```python
x['a'] = 'apple'
print(x)
```

**Output:**

```
{'a': 'apple', 'b': None, 'c': None}
```

---

## Membership Operator (`in` or `not in`)

* Used to verify if a **key** exists in a dictionary.
* Returns a **boolean value**.

```python
dict = {'name': 'Asma', 'age': 20}
print(25 in dict)
```

**Output:**

```
`False`
```

Adding an item and re-checking:

```python
dict[25] = 100
print(dict)
print(25 in dict)
```

**Output:**

```
{'name': 'Asma', 'age': 20, 25: 100}
True
```

---

## `dict()` function

* Used to create a dictionary directly.

```python
x = dict(family='music', type='pop', year=2025)
x
```

**Output:**

```
`{'family': 'music', 'type': 'pop', 'year': 2025}`
```

```python
x['name'] = 'Asma'
x
```

**Output:**

```
`{'family': 'music', 'type': 'pop', 'year': 2025, 'name': 'Asma'}`
```

---
[🔙 Back to Index](README.md)
