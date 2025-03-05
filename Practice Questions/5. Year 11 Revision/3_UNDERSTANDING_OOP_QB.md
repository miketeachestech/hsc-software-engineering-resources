# **Practice Questions: Object-Oriented Programming (OOP)**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the **main advantage** of encapsulation in OOP?  
   - A) It allows direct access to an object's attributes.  
   - B) It hides internal details, protecting data from unintended modification.  
   - C) It makes all class attributes publicly accessible.  
   - D) It eliminates the need for methods in a class.  

**2.** *(1 mark)* What principle of OOP allows a subclass to **reuse** methods and attributes from a parent class?  
   - A) Encapsulation  
   - B) Polymorphism  
   - C) Inheritance  
   - D) Abstraction  

**3.** *(1 mark)* Which of the following statements about **polymorphism** is true?  
   - A) It allows objects of different classes to respond to the same method call in different ways.  
   - B) It restricts method overloading in OOP.  
   - C) It prevents the use of multiple classes in a program.  
   - D) It is only used in procedural programming.  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the **difference between procedural programming and object-oriented programming (OOP)**. Provide an example of when OOP is preferred.

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

**6.** *(3 marks)* What are **abstract classes and interfaces** in OOP? Provide an example of when each should be used.

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a Python class `Car` that includes:
   - Attributes `brand` and `speed`
   - A method `accelerate()` that increases speed by 10.
   - A method `brake()` that decreases speed by 5 but ensures speed does not go below 0.
   - An example of creating an object and calling its methods.

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