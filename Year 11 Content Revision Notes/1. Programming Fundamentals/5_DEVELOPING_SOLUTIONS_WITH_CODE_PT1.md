# Developing Solutions with Code Part 1 - HSC Software Engineering Revision Notes

## 1. Applying Computational Thinking and Programming to Develop a Software Solution
Software development requires **converting algorithms into code** and using **control structures, data structures, modules, and subprograms** to create efficient solutions.

### **1.1 Converting an Algorithm into Code**
Algorithms are **step-by-step instructions** that must be written in a programming language for execution.

#### **Example: Converting Pseudocode to Python**
**Pseudocode:**
```
BEGIN
    INPUT number
    IF number MOD 2 == 0 THEN
        PRINT "Even"
    ELSE
        PRINT "Odd"
    ENDIF
END
```

**Python Code:**
```python
number = int(input("Enter a number: "))
if number % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

### **1.2 Using Control Structures**
Control structures **control the flow of execution** in a program.

#### **1.2.1 Selection (Decision-Making)**
```python
age = int(input("Enter your age: "))
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

#### **1.2.2 Iteration (Loops)**
```python
for i in range(5):
    print("Iteration", i)
```

#### **1.2.3 Repetition (While Loops)**
```python
count = 0
while count < 3:
    print("Counting:", count)
    count += 1
```

---

### **1.3 Using Data Structures**
Data structures help **store and organize data efficiently**.

#### **Example: Using a Dictionary to Store Student Scores**
```python
students = {"Alice": 85, "Bob": 92, "Charlie": 78}
print(students["Bob"])  # Output: 92
```

---

### **1.4 Using Standard Modules**
Standard modules provide **prebuilt functionality** to enhance software development.

#### **Example: Using the `math` Module**
```python
import math
print(math.sqrt(25))  # Output: 5.0
```

---

### **1.5 Creating Relevant Subprograms with Parameter Passing**
Functions allow **code reuse** and **parameter passing** enables dynamic input.

#### **Example: Function with Parameter Passing**
```python
def greet(name):
    print("Hello, " + name + "!")

greet("Alice")  # Output: Hello, Alice!
```

---

## 2. Implementing Data Structures for Data Storage
Data structures store **large amounts of data efficiently**.

### **2.1 Single and Multidimensional Arrays**
Arrays store **multiple values of the same data type**.

#### **Example: Single-Dimensional Array**
```python
numbers = [10, 20, 30, 40]
print(numbers[2])  # Output: 30
```

#### **Example: Multidimensional Array (Matrix Representation)**
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
print(matrix[1][2])  # Output: 6
```

---

### **2.2 Lists**
Lists are **dynamic** data structures that allow flexible data storage.
```python
fruits = ["Apple", "Banana", "Cherry"]
fruits.append("Orange")
print(fruits)  # Output: ['Apple', 'Banana', 'Cherry', 'Orange']
```

---

### **2.3 Trees**
Trees represent **hierarchical data** (e.g., file systems, AI decision trees).

#### **Example: Binary Tree Representation**
```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

tree = Node(10)
tree.left = Node(5)
tree.right = Node(15)
```

---

### **2.4 Stacks**
A **stack** follows the **LIFO (Last-In, First-Out)** principle.

```python
stack = []
stack.append("First")
stack.append("Second")
print(stack.pop())  # Output: Second
```

---

### **2.5 Hash Tables**
Hash tables provide **fast data lookup** using key-value pairs.

```python
hash_table = {"name": "Alice", "age": 25}
print(hash_table["name"])  # Output: Alice
```

---

## 3. Comparing Waterfall and Agile Project Management Models in Software Development
Software projects use **different management models** to ensure successful development.

| **Aspect** | **Waterfall Model** | **Agile Model** |
|------------|----------------|----------------|
| **Development Process** | Linear, step-by-step | Iterative, adaptive |
| **Flexibility** | Fixed; difficult to change requirements | Highly flexible; easy to adjust requirements |
| **Testing** | Done after development | Continuous testing throughout development |
| **User Involvement** | Limited until the end | High; feedback is given regularly |
| **Best Used For** | Large projects with well-defined requirements | Projects needing fast updates and user feedback |

---

### **Waterfall Model Workflow**
```
1. Requirements → 2. Design → 3. Implementation → 4. Testing → 5. Deployment → 6. Maintenance
```

### **Agile Model Workflow**
```
1. Plan → 2. Develop → 3. Test → 4. Review → 5. Iterate (repeat process)
```

### **Example: Applying Agile in Software Development**
- Developers release **small updates** instead of waiting for the entire project to be complete.
- User feedback is collected every **sprint (2-4 weeks)** and changes are made accordingly.
- Agile ceremonies like backlog grooming and retrospectives take place. 