# Designing Algorithms Part 2 - HSC Software Engineering Revision Notes

## 1. Analyzing the Logic and Structure of Written Algorithms
Understanding how algorithms work is essential for **debugging, improving efficiency, and integrating different components of software**. This includes identifying **inputs, outputs, purpose, and connections to subroutines**.

### **1.1 Determining Inputs and Outputs**
- **Inputs:** Data that the algorithm receives to process.
- **Outputs:** The result after execution.
- **Example:** A simple function to calculate the area of a rectangle.

#### **Pseudocode Example**
```
BEGIN
    INPUT length, width
    area ← length * width
    PRINT area
END
```

#### **Python Code Example**
```python
def calculate_area(length, width):
    return length * width

print(calculate_area(5, 10))  # Output: 50
```
- **Inputs:** `length`, `width`
- **Output:** `area`

---

### **1.2 Determining the Purpose of the Algorithm**
To determine what an algorithm does:
1. Identify the **input data**.
2. Follow the **sequence of operations**.
3. Check what **output is produced**.

#### **Example: Identifying an Algorithm's Purpose**
```python
def mystery_function(n):
    if n <= 1:
        return 1
    return n * mystery_function(n - 1)
```
- **Observation:** The function calls itself (`mystery_function(n - 1)`).
- **Conclusion:** This is a **factorial algorithm**.

---

### **1.3 Desk Checking and Peer Checking**
- **Desk Checking**: Manually tracing an algorithm step by step to verify correctness.
- **Peer Checking**: Reviewing another programmer's code to catch errors and inefficiencies.

#### **Desk Checking Example (Tracing a Loop)**
Algorithm:
```python
for i in range(3):
    print(i * 2)
```
Step-by-step execution:
| **Iteration** | **i** | **Output (`i * 2`)** |
|-------------|------|-----------------|
| 1st        | 0    | 0               |
| 2nd        | 1    | 2               |
| 3rd        | 2    | 4               |

Expected Output:
```
0
2
4
```

---

### **1.4 Determining Connections to Other Subroutines or Functions**
- **Algorithms often call subroutines (functions)** to improve **code organization and reuse**.
- **Example:** A program that calculates a discount based on user type:

#### **Python Example with Subroutines**
```python
def get_discount(user_type):
    if user_type == "student":
        return 0.2  # 20% discount
    elif user_type == "senior":
        return 0.3  # 30% discount
    return 0  # No discount

def calculate_price(price, user_type):
    discount = get_discount(user_type)
    return price - (price * discount)

print(calculate_price(100, "student"))  # Output: 80.0
```
- **`calculate_price()`** calls `get_discount()` to determine the appropriate discount.
- **Function reusability** reduces redundant code.

---

## 2. Identifying Procedures and Functions in an Algorithm
- **Procedures**: Perform actions **without returning values**.
- **Functions**: Perform actions **and return values**.

#### **Example: Procedure vs. Function**
```python
def print_message():  # Procedure
    print("Hello, World!")

print_message()  # Prints message but returns nothing


def add_numbers(a, b):  # Function
    return a + b

result = add_numbers(5, 10)  # Returns 15
print(result)
```

| **Feature**      | **Procedure** (`print_message()`) | **Function** (`add_numbers()`) |
|-----------------|--------------------------------|----------------------|
| Returns a value? | ❌ No                         | ✅ Yes               |
| Used for?       | Actions like printing        | Calculations        |

---

## 3. Experimenting with Programming Paradigms
Different programming paradigms affect **how algorithms are structured and executed**.

### **3.1 Object-Oriented Programming (OOP)**
- Organizes code into **classes and objects**.
- Focuses on **reusability and modularity**.
- **Example:** A `Car` class in Python:
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def honk(self):
        return "Beep Beep!"

my_car = Car("Toyota", "Corolla")
print(my_car.honk())  # Output: Beep Beep!
```

---

### **3.2 Imperative Programming**
- Focuses on **step-by-step execution**.
- Uses **variables, loops, and conditionals**.
- **Example:**
```python
sum = 0
for i in range(1, 6):
    sum += i
print(sum)  # Output: 15 (sum of 1 to 5)
```

---

### **3.3 Logic Programming**
- **Uses facts and rules** to define logic-based solutions.
- **Example:** Defining family relationships in Prolog (used in AI development):
```prolog
parent(john, mary).
parent(mary, alice).
grandparent(X, Y) :- parent(X, Z), parent(Z, Y).
```
- The query `grandparent(john, alice).` would return **true**.

---

### **3.4 Functional Programming**
- Uses **pure functions with no side effects**.
- **Example:** Using `map()` in Python to apply a function to a list:
```python
def square(x):
    return x * x

numbers = [1, 2, 3, 4]
squared_numbers = list(map(square, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16]
```
