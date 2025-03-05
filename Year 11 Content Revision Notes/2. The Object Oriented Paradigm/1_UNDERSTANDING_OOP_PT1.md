# Understanding Object-Oriented Programming (OOP) Part 1 - HSC Software Engineering Revision Notes

## 1. Key Features of Object-Oriented Programming (OOP)
Object-Oriented Programming (OOP) is a **programming paradigm** that organizes code into **objects** and **classes** to promote modularity, reusability, and scalability.

### **1.1 Objects and Classes**
- **Objects**: Instances of a **class** that contain data (attributes) and behavior (methods).
- **Classes**: Blueprints for creating objects.

#### **Example: Defining a Class and Creating an Object**
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand  # Attribute
        self.model = model  # Attribute

    def honk(self):
        return "Beep Beep!"

# Creating an object (instance of Car)
my_car = Car("Toyota", "Corolla")
print(my_car.honk())  # Output: Beep Beep!
```

---

### **1.2 Encapsulation**
- **Encapsulation** protects object data by restricting direct access.
- Uses **getter and setter methods** to control attribute access.

#### **Example: Encapsulation Using Private Variables**
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute
    
    def get_balance(self):  # Getter method
        return self.__balance
    
    def deposit(self, amount):  # Setter method
        if amount > 0:
            self.__balance += amount
            return "Deposit Successful"
        return "Invalid Amount"

account = BankAccount(1000)
print(account.get_balance())  # Output: 1000
print(account.deposit(500))  # Output: Deposit Successful
```

---

### **1.3 Abstraction**
- **Hides complex implementation details** and exposes only necessary features.
- Makes code **simpler and easier to use**.

#### **Example: Abstraction Using a Base Class**
```python
from abc import ABC, abstractmethod

class Animal(ABC):  # Abstract class
    @abstractmethod
    def make_sound(self):
        pass  # Must be implemented in subclasses

class Dog(Animal):
    def make_sound(self):
        return "Bark!"

my_dog = Dog()
print(my_dog.make_sound())  # Output: Bark!
```

---

### **1.4 Inheritance**
- **Allows a class to inherit properties and methods from another class**.
- Promotes **code reuse and reduces duplication**.

#### **Example: Inheriting from a Parent Class**
```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand
    
    def start_engine(self):
        return "Engine started"

class Car(Vehicle):  # Car inherits from Vehicle
    def honk(self):
        return "Honk Honk!"

my_car = Car("Honda")
print(my_car.start_engine())  # Output: Engine started
print(my_car.honk())  # Output: Honk Honk!
```

---

### **1.5 Generalisation**
- **Creating a broad class** that can be extended into **more specific classes**.
- Helps organize objects **logically in a hierarchy**.

#### **Example: Generalisation in a School System**
```
+-----------------+
| Person         |
+-----------------+
| name           |
| age            |
| get_details()  |
+-----------------+
       |
       +------------+------------+
       |                         |
+----------------+      +----------------+
| Student        |      | Teacher        |
+----------------+      +----------------+
| student_id     |      | subject        |
| get_grades()   |      | teach()        |
+----------------+      +----------------+
```

---

### **1.6 Polymorphism**
- **Different objects can use the same method name** but behave differently.
- Reduces complexity by allowing **multiple behaviors for the same function**.

#### **Example: Polymorphism in Action**
```python
class Bird:
    def make_sound(self):
        return "Some generic bird sound"

class Sparrow(Bird):
    def make_sound(self):
        return "Chirp!"

class Duck(Bird):
    def make_sound(self):
        return "Quack!"

animals = [Sparrow(), Duck(), Bird()]
for animal in animals:
    print(animal.make_sound())
```
**Output:**
```
Chirp!
Quack!
Some generic bird sound
```

---

## 2. Comparing Procedural Programming vs. Object-Oriented Programming

| **Feature** | **Procedural Programming** | **Object-Oriented Programming** |
|------------|--------------------------|-----------------------------|
| **Structure** | Uses functions to process data | Uses objects and classes |
| **Data Handling** | Variables and functions are separate | Data is encapsulated in objects |
| **Code Reusability** | Code must be rewritten for different programs | Uses inheritance and polymorphism to reuse code |
| **Scalability** | Harder to manage large programs | Easier to scale using modular classes |
| **Example Use Cases** | Simple scripts, calculations, small utilities | Large applications, game development, GUI applications |

### **Example: Procedural vs. OOP Implementation**

#### **Procedural Approach**
```python
def area_of_rectangle(length, width):
    return length * width

print(area_of_rectangle(5, 10))  # Output: 50
```

#### **Object-Oriented Approach**
```python
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width
    
    def area(self):
        return self.length * self.width

rect = Rectangle(5, 10)
print(rect.area())  # Output: 50
```

---

## 3. Use data flow diagrams, structure charts and class diagrams to represent a system

Check out NESA's "Terms and Examples" document (see the NESA Resources folder) for examples of diagrams and notations.

---

## **Summary**
- ✅ **OOP organizes code into reusable classes and objects**.
- ✅ **Encapsulation, inheritance, and polymorphism improve code efficiency**.
- ✅ **Procedural programming is simpler but less scalable for large projects**.
- ✅ **OOP is widely used in modern software development for building large, maintainable applications**.