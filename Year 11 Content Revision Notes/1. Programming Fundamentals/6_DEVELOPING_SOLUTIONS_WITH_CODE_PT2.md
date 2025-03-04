# Developing Solutions with Code Part 2 - HSC Software Engineering Revision Notes

## 1. Testing and Evaluating Software Solutions
To ensure a software solution is **functional, efficient, and maintainable**, developers must evaluate key aspects such as **functionality, performance, code readability, and documentation quality**.

### **1.1 Key Aspects of Software Evaluation**
| **Aspect**        | **Description** |
|------------------|----------------|
| **Functionality** | Does the software perform as expected? |
| **Performance**   | Is the software fast and efficient? |
| **Readability of Code** | Is the code well-structured and easy to understand? |
| **Quality of Documentation** | Does the software have clear documentation for future developers? |

### **1.2 Example: Evaluating Code Quality**
```python
# Poorly written code (low readability)
def f(x): return x*x + 2*x + 1
print(f(5))

# Improved code (better readability)
def calculate_quadratic(x):
    return (x ** 2) + (2 * x) + 1

print(calculate_quadratic(5))
```
- The second example improves **readability** by using a descriptive function name.

---

## 2. Using Debugging Tools
Debugging tools help programmers **identify and fix errors** more efficiently.

### **2.1 Common Debugging Techniques**
| **Technique** | **Description** |
|--------------|----------------|
| **Breakpoints** | Pauses execution at a specific line to inspect values. |
| **Single Line Stepping** | Executes code **one line at a time** to track logic. |
| **Watches** | Monitors variable values while running the program. |
| **Interfaces Between Functions** | Ensures functions interact correctly by checking input and output values. |
| **Debugging Output Statements** | Uses print statements to track variable values and execution flow. |
| **IDE Debugging Software** | Built-in debugging tools in IDEs like PyCharm, VS Code, and Eclipse. |

### **2.2 Example: Using Debugging Output Statements**
```python
def divide_numbers(a, b):
    print(f"Dividing {a} by {b}")  # Debugging output
    return a / b

print(divide_numbers(10, 2))  # Expected output: 5
```

---

## 3. Determining Suitable Test Data
A **good test plan** includes different types of input data to ensure the software handles all cases correctly.

### **3.1 Types of Test Data**
| **Test Type** | **Description** | **Example** |
|-------------|----------------|-------------|
| **Boundary Values** | Tests limits of valid input ranges. | Inputting `0` when expecting positive values. |
| **Path Coverage** | Ensures all possible paths in code are tested. | Testing both **if** and **else** conditions in an `if-else` statement. |
| **Faulty/Abnormal Data** | Tests incorrect input values to check error handling. | Entering letters into a numeric input field. |

### **3.2 Example: Handling Faulty Data in Python**
```python
try:
    age = int(input("Enter your age: "))  # User inputs "abc"
except ValueError:
    print("Invalid input! Please enter a number.")
```
- The **try-except block** prevents crashes when the user enters non-numeric data.

---

## 4. Common Errors in Software Development
Software bugs fall into **three main categories**: syntax errors, logic errors, and runtime errors.

### **4.1 Types of Errors**
| **Error Type** | **Description** | **Example** |
|--------------|----------------|-------------|
| **Syntax Error** | Code structure is incorrect (e.g., missing a colon). | `print("Hello"` (missing `)`) |
| **Logic Error** | The program runs, but produces the wrong result. | Using `+` instead of `-` in a formula. |
| **Runtime Error** | The program crashes during execution. | Dividing by zero. |

### **4.2 Example: Syntax Error**
```python
# Missing colon (Syntax Error)
if x > 5
    print("x is greater than 5")
```
- **Fix:** Add a colon `:` after `if x > 5:`.

### **4.3 Example: Logic Error**
```python
# Incorrect logic (returns incorrect area)
def rectangle_area(length, width):
    return length + width  # Should be length * width
```
- **Fix:** Replace `+` with `*`.

### **4.4 Example: Runtime Error (Dividing by Zero)**
```python
def divide(a, b):
    return a / b  # Will crash if b == 0

print(divide(10, 0))
```
- **Fix:** Add a condition to check for zero:
```python
def divide_safe(a, b):
    if b == 0:
        return "Error: Cannot divide by zero"
    return a / b
```