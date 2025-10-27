# Classes And Objects

Python is an **object-oriented programming language**.  
Unlike procedure-oriented programming, where the main emphasis is on functions, object-oriented programming focuses on **objects**.

An **object** is a collection of **data (variables)** and **methods (functions)** that act on that data.  
A **class** is a **blueprint** for creating objects.

---

## 🧩 Key Concepts

- **Class** → Blueprint for creating objects  
- **Object** → Instance of a class  
- **Constructor (`__init__`)** → Initializes object data automatically when an object is created  
- **Destructor (`__del__`)** → Called automatically when an object is deleted or goes out of scope  
- **Method** → Function defined inside a class  
- **`self`** → Refers to the current instance of the class  
- **Encapsulation** → Binding data and functions together  
- **Abstraction** → Hiding internal details and showing only necessary features  

---

## 🧱 Syntax

```python
class ClassName:
    # constructor
    def __init__(self, parameter1, parameter2):
        self.parameter1 = parameter1   # instance variable
        self.parameter2 = parameter2

    # method
    def display(self):
        print("Parameter 1:", self.parameter1)
        print("Parameter 2:", self.parameter2)

# creating an object
obj = ClassName(value1, value2)

# accessing methods and variables
obj.display()
print(obj.parameter1)
````

---

## 🧑‍🎓 Example: Student Class

```python
class Student:
    schoolname = "ABC School"   # class variable

    # constructor
    def __init__(self, name, age):
        self.name = name        # instance variable
        self.age = age
        print("Constructor called — Object created")

    # destructor
    def __del__(self):
        print("Destructor called — Object destroyed")

    def display(self):
        print("Name:", self.name)
        print("Age:", self.age)
        print("School:", Student.schoolname)

# creating an object
obj = Student("Asma", 20)

obj.display()

# deleting the object
del obj
```

**Output:**

```
Constructor called — Object created
Name: Asma
Age: 20
School: ABC School
Destructor called — Object destroyed
```

---

## 🧠 What is `__init__`?

* `__init__` is a **special method** in Python classes.
* It is **automatically executed** when a new object of the class is created.
* It is known as the **constructor** because it **constructs (initializes)** the object’s state (data).
* You can use it to assign default values or set up necessary attributes.

**Example:**

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

c1 = Car("Toyota", "Red")
print(c1.brand)
print(c1.color)
```

**Output:**

```
Toyota
Red
```

---

## 🧹 What is `__del__`?

* `__del__` is another special method, known as the **destructor**.
* It is automatically called **when an object is deleted** or **goes out of scope**.
* It is mainly used for cleanup tasks, like closing files or releasing resources.

**Example:**

```python
class Example:
    def __init__(self):
        print("Object Created")

    def __del__(self):
        print("Object Destroyed")

obj = Example()
del obj
```

**Output:**

```
Object Created
Object Destroyed
```

---

## ⚙️ Types of Variables

| Type                  | Description                        | Example                 |
| --------------------- | ---------------------------------- | ----------------------- |
| **Instance Variable** | Belongs to a specific object       | `self.name`, `self.age` |
| **Class Variable**    | Shared by all objects of the class | `schoolname`            |

---

## ⚙️ Types of Methods

| Type                | Description                           | Decorator        |
| ------------------- | ------------------------------------- | ---------------- |
| **Instance Method** | Works with instance variables         | *(no decorator)* |
| **Class Method**    | Works with class variables            | `@classmethod`   |
| **Static Method**   | Independent of class or instance data | `@staticmethod`  |

**Example:**

```python
class Example:
    class_var = "Hello"

    def __init__(self, value):
        self.value = value

    def instance_method(self):
        print("Instance method:", self.value)

    @classmethod
    def class_method(cls):
        print("Class method:", cls.class_var)

    @staticmethod
    def static_method():
        print("Static method: Utility function")

obj = Example("Python")

obj.instance_method()
Example.class_method()
Example.static_method()
```

---

## 🧮 Mathematical Calculations in Python

For mathematical calculations, we use the `import math` statement,
which includes the **math module** that provides a collection of mathematical functions and constants.

Python’s built-in math functions like addition (`+`), subtraction (`-`), multiplication (`*`), etc., are basic.
But for advanced operations (square roots, trigonometry, logarithms, etc.), you need the **math module**.

---

## Common Math Module Functions

| Function            | Description                    |
| ------------------- | ------------------------------ |
| `math.pi`           | Value of π (pi) constant       |
| `math.sqrt(x)`      | Returns the square root of *x* |
| `math.factorial(x)` | Returns the factorial of *x*   |

---

### Keyboard Shortcuts

* `Alt + 0178` → cm²
* `Alt + 0179` → cm³

---

## ✅ Summary

| Concept                      | Description                                    |
| ---------------------------- | ---------------------------------------------- |
| **Class**                    | Blueprint for creating objects                 |
| **Object**                   | Instance of a class                            |
| **Constructor (`__init__`)** | Called automatically when an object is created |
| **Destructor (`__del__`)**   | Called automatically when an object is deleted |
| **Method**                   | Function defined inside a class                |
| **self**                     | Refers to the instance calling the method      |
| **Class Variable**           | Shared by all objects                          |
| **Instance Variable**        | Unique to each object                          |
| **Encapsulation**            | Data hiding inside a class                     |
| **Abstraction**              | Showing only essential details                 |
| **del**                      | Used to delete objects or attributes           |

---

## 📓 Jupyter Notebook
You can view the runnable code in the notebook:  
[**Class_&_Object in Python**](./Notebook/Class_&_Object_in_Python.ipynb)

Or run it directly in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asma-afzal-sayyed/python-fundamentals-2025/blob/main/Notebook/Class_&_Object_in_Python.ipynb)

---

[🔙 Back to Index](README.md)
