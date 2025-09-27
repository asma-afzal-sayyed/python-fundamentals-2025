# Tuples


-   **Tuples are immutable lists** and can't be changed in any way once
    it is created.
-   Tuples are defined in the same way as lists.
-   They are enclosed within **parenthesis** and not within square
    braces.
-   Tuples are **ordered, indexed collections of data**. Similar to
    string indices, the first value in the tuple will have the index
    `[0]`, the second value will be `[1]`.
-   **Negative indices** are counted from the end of the tuple, just
    like lists as well as strings.
-   Tuples also have the same structure where **commas separated
    values**.
-   Tuples can store **duplicate values**.
-   Tuples allow you to store several data items, including **string,
    integer, and float** in one variable.

### Tuple Creation

``` python
tup = ()
print(tup)
print(type(tup))
>> <class 'tuple'>
```


### Indexing

``` python
x = (10, 20, 1020, 464)

# Positive indexing
print(x[0]) 
print(x[3])

>> 10
>> 464

# Negative indexing
print(x[-1])
print(x[-3])

>> 464
>> 1020
```

### Concatenation and Repetition

``` python
tup1 = ('Python', 'Hello', 20)
tup2 = (10, 20, 30)

# Concatenation
print(tup1 + tup2)
>> ('Python', 'Hello', 20, 10, 20, 30)

tup = (1, 2, 3, 4)

# Repetition
tup * 2
>> (1, 2, 3, 4, 1, 2, 3, 4)
```

### Built-in Functions

``` python
tup = (1, 2, 3, 4)

# Minimum
min(tup)
>> 1

# Maximum
max(tup)
>> 4

# Sum of tuple
sum(tup)
>> 10
```

### The `tuple(seq)` function

-   It converts a specific sequence (`seq`) to a tuple.

``` python
seq = "Asma"
tuple(seq)

>> ('A', 's', 'm', 'a')
```

### Slicing of Tuple Elements

``` python
X = (10, 10, 11.00, True, 'Asma')

X[:2]
>> (10, 10)

X[2:4]
>> (11.00, True)
```
### Nested indexing/Accessing elements in a nested tuple/list/dictionary
``` python

# Accessing the element 'Asma' inside the list at index 6

X = ('Hello', 'Python', 3.14, True, False, (1, 2, 3), [1, 2, 'Asma'], {'a': 12, 'b': 20})
X[6][2] = 'Asma' 
print(X)

>> ('Hello', 'Python', 3.14, True, False, (1, 2, 3), [1, 2, 'Asma'], {'a': 12, 'b': 20})
```

### Striding Value (Step)

``` python
X = ('Hello', 'Python', 3.14, True, False, (1, 2, 'Asma'), {'a': 12, 'b': 20}) # Assuming X is the previous tuple
X[::2]
>> ('Hello', 3.14, False, {'a': 12, 'b': 20})
```

### Length and Memory Address

``` python
# Assuming X is the tuple from the Slicing section:
# X = ('Hello', 'Python', 3.14, True, False, (1, 2, 3), [1, 2, 'Asma'], {'a': 12, 'b': 20})

# len()
len(X) # count with 1 not 0
>> 8

# id()
we can check **memory address** of tuple by using `id()`.

id(tup1)
>> 2097319736690 # Example memory address
```

### Immutability and Deletion

-   Tuples are **immutable** so we can't do any operation on tuple like
    `pop()`, `del()`, `remove()`, `append()`, `insert()`, `extend()`.
-   We can **delete whole tuple** using `del()` but can't delete one
    element.

``` python
# Assuming X is the large tuple
del(X) # delete whole tuple
```

### Tuple Methods

#### $\star$ `count()`

-   This method returns the **number of times an item occurs** in a
    tuple.

``` python
X = (1, 3, 5, 8, 1, 9, 9, 1)
print(X.count(1))
>> 3
```

#### $\star$ `index()`

-   It returns the **index of the first occurrence** of the specified
    value in a tuple.

``` python
# Using X = (1, 3, 5, 8, 1, 9, 9, 1)
X.index(9)
>> 5
```



---
[🔙 Back to Index](README.md)
