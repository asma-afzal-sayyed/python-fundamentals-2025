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
`{'name': 'Asma', 'age': 20, 'city': 'Pune'}`

* The dictionary is enclosed in curly brackets `{ }`.
* Each key is separated from its value by a **colon ( : )**, and **commas ( , )** are used to separate the items.

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
`dict_keys(['name', 'age', 'city'])`

---

### `values()` function

* Returns all values of the dictionary.

```python
dict.values()
```

**Output:**
`dict_values(['Asma', 20, 'Pune'])`

---

### `items()` function

* Returns both keys & values as pairs.

```python
dict.items()
```

**Output:**
`dict_items([('name', 'Asma'), ('age', 20), ('city', 'Pune')])`

---

## Dictionary Manipulation Methods

### Adding a New Key:Value Pair

```python
dict['Phno'] = "1003568901"
dict
```

**Output:**
`{'name': 'Asma', 'age': 20, 'city': 'Pune', 'Phno': '1003568901'}`

---

### Updating an Existing Value

```python
dict['Phno'] = '1234'
dict
```

**Output:**
`{'name': 'Asma', 'age': 20, 'city': 'Pune', 'Phno': '1234'}`

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

* Checks if a key exists safely without raising an error.

```python
dict.get('name')
```

**Output:**
`Asma`

```python
dict.get('city')
```

**Output:**
`None`

---

### `fromkeys()` function

* Creates a new dictionary from given keys with default value `None`.

```python
key = {'a', 'b', 'c'}
x = dict.fromkeys(key)
print(x)
```

**Output:**
`{'a': None, 'b': None, 'c': None}`

* Assigning values later:

```python
x['a'] = 'apple'
x
```

**Output:**
`{'a': 'apple', 'b': None, 'c': None}`

---

## Membership Operator (`in` or `not in`)

* Used to verify if a **key** exists in a dictionary.
* Returns a **boolean value**.

```python
dict = {'name': 'Asma', 'age': 20}
print(25 in dict)
```

**Output:**
`False`

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
`{'family': 'music', 'type': 'pop', 'year': 2025}`

```python
x['name'] = 'Asma'
x
```

**Output:**
`{'family': 'music', 'type': 'pop', 'year': 2025, 'name': 'Asma'}`

---
[🔙 Back to Index](README.md)
