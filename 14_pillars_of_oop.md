# 🧱 Pillars of Object-Oriented Programming (OOPs) in Python

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **objects** that contain **data (attributes)** and **methods (functions)**.  
Python is an object-oriented language that supports all OOP principles.

---

## 🗂️ Table of Contents
1. [Introduction](#introduction)
2. [1️⃣ Inheritance](#1️⃣-inheritance)
   - [Single / Simple Inheritance](#single--simple-inheritance)
   - [Multilevel Inheritance](#multilevel-inheritance)
   - [Multiple Inheritance](#multiple-inheritance)
   - [Hierarchical Inheritance](#hierarchical-inheritance)
   - [Hybrid Inheritance](#hybrid-inheritance)
3. [2️⃣ Polymorphism](#2️⃣-polymorphism)
   - [Overriding (Run-Time Polymorphism)](#overriding-run-time-polymorphism)
   - [Overloading (Compile-Time Polymorphism)](#overloading-compile-time-polymorphism)
4. [3️⃣ Encapsulation](#3️⃣-encapsulation)
5. [4️⃣ Data Abstraction](#4️⃣-data-abstraction)
6. [📊 Summary](#📊-summary)
7. [📗 OOPs Mini Projects](#💻-oop-project-collection-in-python)

---

## 🧩 Introduction

The **four main pillars** of OOP are:

| Pillar | Description |
|--------|--------------|
| **Inheritance** | Acquiring properties and behavior from another class |
| **Polymorphism** | Using one interface with multiple implementations |
| **Encapsulation** | Binding data and methods together while restricting direct access |
| **Data Abstraction** | Hiding implementation details and exposing only necessary features |

---

## 1️⃣ Inheritance

**Definition:**  
Inheritance allows a class (child or derived class) to acquire attributes and methods from another class (parent or base class).

### 🧠 Types of Inheritance in Python

| Type | Description |
|------|--------------|
| **Single** | Child inherits from one parent |
| **Multilevel** | Chain of inheritance (Grandparent → Parent → Child) |
| **Multiple** | Child inherits from multiple parents |
| **Hierarchical** | Multiple children inherit from a single parent |
| **Hybrid** | Combination of multiple inheritance types |

---

### 🧩 Single / Simple Inheritance

```python
class Parent:
    broadband = "Amazon"
    broadband2 = "Flipkart"

class Child(Parent):
    prod1 = "Online Store"
    prod2 = "Ecommerce website"

obj = Child()
print(obj.broadband)    # Output: Amazon
print(obj.broadband2)   # Output: Flipkart
print(obj.prod1)        # Output: Online Store
print(obj.prod2)        # Output: Ecommerce website
````

---

### 🧱 Multilevel Inheritance

```python
class classA:
    x = "apple"

class classB(classA):
    y = "banana"

class classC(classB):
    z = "orange"

obj = classC()
print(obj.x)  # Output: apple
print(obj.y)  # Output: banana
print(obj.z)  # Output: orange
```

---

### 🔗 Multiple Inheritance

```python
class classA:
    x = 100

class classB:
    y = 200

class classC(classA, classB):
    z = 300

obj = classC()
print(obj.x)  # Output: 100
print(obj.y)  # Output: 200
print(obj.z)  # Output: 300
```

> 💡 **Note:** In multiple inheritance, Python uses the **Method Resolution Order (MRO)** to determine which parent class is used first when resolving attributes or methods.

---

### 🌿 Hierarchical Inheritance

```python
class classA:
    broadband = "Amazon"
    broadband2 = "Flipkart"

class classB(classA):
    prod1 = "Online Store"
    prod2 = "Ecommerce website"

class classC(classA):
    popularity = 100

obj1 = classB()
print(obj1.broadband)
print(obj1.prod1)

obj2 = classC()
print(obj2.broadband)
print(obj2.popularity)
```

---

### 🧬 Hybrid Inheritance

Hybrid inheritance is a combination of more than one type of inheritance (for example, combining **Multiple** and **Multilevel Inheritance**).

> ⚠️ **Note:** In hybrid inheritance, ambiguity can occur if a child class inherits from multiple parent classes having the same method names.
> Python handles this using **Method Resolution Order (MRO)**.

#### ✅ Example: Hybrid Inheritance in Python

```python
# Single inheritance + Multiple inheritance combined

# Base class
class ClassA:
    def featureA(self):
        print("Feature A from ClassA")

# Derived from ClassA (Multilevel inheritance)
class ClassB(ClassA):
    def featureB(self):
        print("Feature B from ClassB")

# Another independent base class
class ClassC:
    def featureC(self):
        print("Feature C from ClassC")

# Derived from ClassB and ClassC (Hybrid = Multilevel + Multiple)
class ClassD(ClassB, ClassC):
    def featureD(self):
        print("Feature D from ClassD")

# Create object of ClassD
obj = ClassD()
obj.featureA()  # From ClassA
obj.featureB()  # From ClassB
obj.featureC()  # From ClassC
obj.featureD()  # From ClassD
```

**Output:**

```
Feature A from ClassA
Feature B from ClassB
Feature C from ClassC
Feature D from ClassD
```

---

## 2️⃣ Polymorphism

**Polymorphism** means *“many forms.”*
It allows a single function, method, or operator to behave differently based on the context.

---

### ⚙️ Overriding (Run-Time Polymorphism)

* Same method name and parameters in both parent and child classes.
* Dynamic — resolved at **runtime**.
* Enables extending or modifying parent behavior.

```python
class Animal:
    def sound(self):
        print("Animals make sounds")

class Dog(Animal):
    def sound(self):
        print("Dog barks")

puppy = Dog()
puppy.sound()  # Output: Dog barks
```

---

### ⚡ Overloading (Compile-Time Polymorphism)

Python does **not support** method overloading directly.
However, we can achieve similar behavior using:

* Default arguments
* Variable arguments (`*args`, `**kwargs`)
* `functools.singledispatch`

#### Example 1: Default Argument

```python
class Greeting:
    def hello(self, name=None):
        if name:
            print("Hello " + name)
        else:
            print("Hello")

obj = Greeting()
obj.hello()       # Output: Hello
obj.hello("Asma") # Output: Hello Asma
```

#### Example 2: Using *args

```python
def model(*args):
    if len(args) == 1:
        print(args[0])
    elif len(args) == 2:
        print(args[0] + args[1])

model(10)      # Output: 10
model(10, 20)  # Output: 30
```

---

### 🔍 Comparison Between Overriding and Overloading

| Feature        | Overriding (Run-Time) | Overloading (Compile-Time)         |
| -------------- | --------------------- | ---------------------------------- |
| Method Name    | Same                  | Same                               |
| Arguments      | Same                  | Different                          |
| Inheritance    | Required              | Not required                       |
| Execution Time | Runtime               | Compile time (simulated in Python) |
| Type           | Dynamic Polymorphism  | Static Polymorphism                |

---

## 3️⃣ Encapsulation

Encapsulation binds **data (variables)** and **methods (functions)** together and restricts direct access to the internal data of an object.

### 🔒 Access Modifiers in Python

| Type      | Declaration   | Accessibility                          |
| --------- | ------------- | -------------------------------------- |
| Public    | No underscore | Accessible everywhere                  |
| Protected | `_variable`   | Accessible within class and subclasses |
| Private   | `__variable`  | Accessible only inside the class       |

---

### 💰 Example: Bank Account

```python
class BankAccount:
    def __init__(self, accNo, balance):
        self.__accountNumber = accNo  # private
        self.__balance = balance      # private

    def get_balance(self):
        return self.__balance

    def deposit(self, amount):
        self.__balance += amount
        print("Deposited:", amount)
        print("Updated balance:", self.__balance)

    def withdrawal(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
            print("Withdrawn:", amount)
            print("Remaining balance:", self.__balance)
        else:
            print("Insufficient funds")

obj = BankAccount(123456789, 1000)
print("Current balance:", obj.get_balance())
obj.deposit(500)
obj.withdrawal(200)
```

---

## 4️⃣ Data Abstraction

**Abstraction** means hiding internal implementation details and exposing only the essential features.

### 🧰 Example Using `abc` Module

```python
from abc import ABC, abstractmethod

class AbstractVehicle(ABC):
    @abstractmethod
    def start(self):
        pass

    @abstractmethod
    def stop(self):
        pass

class Car(AbstractVehicle):
    def start(self):
        print("Car engine started.")

    def stop(self):
        print("Car engine stopped.")

car = Car()
car.start()  # Output: Car engine started.
car.stop()   # Output: Car engine stopped.
```

> ⚠️ **Note:**
>
> * Abstract classes **cannot be instantiated**.
> * Child classes must implement **all abstract methods**.

---

## 📊 Summary

| Pillar            | Concept                             | Purpose          |
| ----------------- | ----------------------------------- | ---------------- |
| **Inheritance**   | Reusing code from existing classes  | Code Reusability |
| **Polymorphism**  | Same interface, different behaviors | Flexibility      |
| **Encapsulation** | Restricting direct access to data   | Data Protection  |
| **Abstraction**   | Hiding implementation details       | Simplification   |

---

## 💻 OOP Project Collection in Python

Explore these **Object-Oriented Programming (OOP)** mini-projects implemented in Python.  
Each notebook demonstrates one or more key OOP concepts such as Inheritance, Encapsulation, Polymorphism, Abstraction, and Composition.

| No. | Project Title | Concepts Covered | Notebook Link | Open in Colab |
|-----|----------------|------------------|----------------|----------------|
| 1️⃣ | **Library Management System** | Encapsulation, Inheritance, Polymorphism, Abstraction | [View Notebook](./Notebook/OOP_Project_Library_Management_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Library_Management_System.ipynb) |
| 2️⃣ | **Student Management System** | Inheritance, Abstraction, Composition | [View Notebook](./Notebook/OOP_Project_Student_Management_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Student_Management_System.ipynb) |
| 3️⃣ | **Online Shopping Cart** | Composition, Encapsulation, Polymorphism | [View Notebook](./Notebook/OOP_Project_Online_Shopping_Cart.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Online_Shopping_Cart.ipynb) |
| 4️⃣ | **Employee Payroll System** | Inheritance, Polymorphism, Encapsulation | [View Notebook](./Notebook/OOP_Project_Employee_Payroll_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Employee_Payroll_System.ipynb) |
| 5️⃣ | **Vehicle Rental System** | Inheritance, Abstraction, Method Overriding | [View Notebook](./Notebook/OOP_Project_Vehicle_Rental_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Vehicle_Rental_System.ipynb) |
| 6️⃣ | **School Grading System** | Inheritance, Composition, Polymorphism | [View Notebook](./Notebook/OOP_Project_School_Grading_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_School_Grading_System.ipynb) |
| 7️⃣ | **Hospital Management System** | Inheritance, Abstraction, Polymorphism, Encapsulation | [View Notebook](./Notebook/OOP_Project_Hospital_Management_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Hospital_Management_System.ipynb) |
| 8️⃣ | **Hotel Booking System** | Encapsulation, Composition, Inheritance | [View Notebook](./Notebook/OOP_Project_Hotel_Booking_System.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/OOP_Project_Hotel_Booking_System.ipynb) |
| 9️⃣ | **ATM System (Interactive Project)** | Encapsulation, Polymorphism, Exception Handling | [View Notebook](./Notebook/ATM_Project.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/Notebook/ATM_Project.ipynb) |
 

---
[🔙 Back to Index](README.md)
