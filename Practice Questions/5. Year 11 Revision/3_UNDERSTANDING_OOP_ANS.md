# **Answers: Object-Oriented Programming (OOP)**

## **Multiple Choice Questions**

**1.** *(1 mark)*  
- Correct Answer: **B) It hides internal details, protecting data from unintended modification.**  
- **1 mark** awarded for correctly selecting the answer.  

**2.** *(1 mark)*  
- Correct Answer: **C) Inheritance**  
- **1 mark** awarded for correctly selecting the answer.  

**3.** *(1 mark)*  
- Correct Answer: **A) It allows objects of different classes to respond to the same method call in different ways.**  
- **1 mark** awarded for correctly selecting the answer.  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the **difference between procedural programming and object-oriented programming (OOP)**. Provide an example of when OOP is preferred.
- **1 mark** for explaining that **procedural programming** follows a **step-by-step approach** using functions and procedures.
- **1 mark** for explaining that **OOP structures code using objects and classes**, promoting modularity and reusability.
- **1 mark** for providing an example where **OOP is preferred** (e.g., large applications like a banking system where multiple components need to interact).  

**5.** *(3 marks)* Identify the **error(s) in the following Python class implementation** and suggest a fix:
```python
class Animal:
    def __init__(self, name):
        name = name  # Error here

    def make_sound(self):
        return "Some sound"

my_pet = Animal("Buddy")
print(my_pet.name)  # This will cause an error
```
- **1 mark** for identifying that `name = name` does not properly assign the attribute.
- **1 mark** for explaining that `self.name = name` is needed to store the name within the object.
- **1 mark** for providing the correct fix:
```python
class Animal:
    def __init__(self, name):
        self.name = name  # Corrected

    def make_sound(self):
        return "Some sound"

my_pet = Animal("Buddy")
print(my_pet.name)  # Output: Buddy
```

**6.** *(3 marks)* What are **abstract classes and interfaces** in OOP? Provide an example of when each should be used.
- **1 mark** for defining **abstract classes** as **classes that cannot be instantiated** and are used as blueprints for other classes.
- **1 mark** for defining **interfaces** as contracts that enforce methods in derived classes.
- **1 mark** for providing an example where abstract classes define common behavior (e.g., an `Animal` class), and interfaces enforce consistency (e.g., `Flyable` interface for birds and planes).

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a Python class `Car` that includes:
```python
class Car:
    def __init__(self, brand, speed=0):
        self.brand = brand
        self.speed = speed

    def accelerate(self):
        self.speed += 10

    def brake(self):
        self.speed = max(0, self.speed - 5)  # Ensures speed does not go below 0

# Example usage
my_car = Car("Toyota")
my_car.accelerate()
print(my_car.speed)  # Output: 10
my_car.brake()
print(my_car.speed)  # Output: 5
```
- **1 mark** for correctly defining attributes `brand` and `speed`.
- **1 mark** for implementing `accelerate()` correctly.
- **1 mark** for implementing `brake()` ensuring speed doesn’t go negative.
- **1 mark** for demonstrating object creation and method calls.

**8.** *(4 marks)* The following Python code **contains a bug related to inheritance**. Identify and fix the issue.
```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

class Car(Vehicle):
    def __init__(self, brand, model):
        self.model = model  # Error: Missing something important

my_car = Car("Toyota", "Corolla")
print(my_car.brand, my_car.model)  # This will cause an error
```
**Bug:** The `Car` class does not properly call the parent class `Vehicle` constructor.

**Fixed Version:**
```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

class Car(Vehicle):
    def __init__(self, brand, model):
        super().__init__(brand)  # Correctly call parent constructor
        self.model = model

my_car = Car("Toyota", "Corolla")
print(my_car.brand, my_car.model)  # Output: Toyota Corolla
```
- **1 mark** for identifying the missing `super().__init__(brand)`.
- **1 mark** for explaining that the parent constructor must be explicitly called.
- **1 mark** for correcting the issue.
- **1 mark** for correctly demonstrating object creation and output.

**9.** *(4 marks)* Convert the following Python **class relationships into a UML class diagram**:
```python
class Animal:
    def make_sound(self):
        return "Some generic sound"

class Dog(Animal):
    def make_sound(self):
        return "Bark"

class Cat(Animal):
    def make_sound(self):
        return "Meow"
```
### **UML Representation:**
```
+----------------+
| Animal        |
+----------------+
| +make_sound() |
+----------------+
       ▲
       │
 +-----------+-----------+
 |                       |
+--------+       +--------+
| Dog    |       | Cat    |
+--------+       +--------+
| +make_sound() | | +make_sound() |
+--------+       +--------+
```
- **1 mark** for representing `Animal` as a parent class.
- **1 mark** for correctly showing `Dog` and `Cat` as subclasses.
- **1 mark** for including the `make_sound()` method in all classes.
- **1 mark** for using correct UML notation.