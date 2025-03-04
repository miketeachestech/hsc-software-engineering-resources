# Programming in OOP - HSC Software Engineering Revision Notes

## 1. Designing and Implementing OOP Programs with Branching, Iteration, and Functions
Object-Oriented Programming (OOP) allows developers to write **structured, reusable, and maintainable** code. Programs should include:
- **Branching** (decision-making with `if-else` statements).
- **Iteration** (loops for repeating tasks).
- **Functions** (methods to organize tasks).

### **Example: A Simple Banking System Using OOP**
```python
class BankAccount:
    def __init__(self, name, balance=0):
        self.name = name
        self.balance = balance
    
    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"Deposited ${amount}. New balance: ${self.balance}")
        else:
            print("Invalid deposit amount.")
    
    def withdraw(self, amount):
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew ${amount}. Remaining balance: ${self.balance}")
        else:
            print("Invalid withdrawal amount.")
    
    def check_balance(self):
        return f"Account Balance: ${self.balance}"

# Using the BankAccount class
account = BankAccount("Alice", 500)
account.deposit(200)
account.withdraw(100)
print(account.check_balance())
```
- **Branching:** The `if-else` statements ensure deposits and withdrawals are valid.
- **Iteration:** Loops can be added for multiple transactions.
- **Functions:** The `deposit()`, `withdraw()`, and `check_balance()` methods organize the code.

---

## 2. Implementing and Modifying OOP Code
### **2.1 Clear and Uncluttered Mainline**
- The **main program flow** should be easy to follow.
- **Example:** Avoid clutter by moving logic into **separate functions**.

```python
class Car:
    def __init__(self, brand):
        self.brand = brand
    
    def start_engine(self):
        return "Engine started"

def main():
    my_car = Car("Toyota")
    print(my_car.start_engine())

if __name__ == "__main__":
    main()
```
- **Mainline (`main()`) is separate**, making the program easier to read.

### **2.2 One Logical Task per Subroutine**
- Functions should **do one thing well**.
- **Example:** A `calculate_area()` function should **only calculate area**.

```python
def calculate_area(length, width):
    return length * width
```

### **2.3 Use of Stubs for Testing**
- **Stubs** are **placeholder methods** used for testing before full functionality is added.
- **Example:**
```python
def get_user_input():
    return "Stub: Replace with actual input handling later"

print(get_user_input())
```

### **2.4 Use of Control Structures and Data Structures**
- **Control Structures:**
  - `if-else` for decisions.
  - `for` and `while` loops for iteration.
- **Data Structures:**
  - Lists, dictionaries, and objects.

**Example: Using a Dictionary to Store User Data**
```python
users = {
    "Alice": {"age": 25, "email": "alice@example.com"},
    "Bob": {"age": 30, "email": "bob@example.com"}
}
print(users["Alice"]["email"])  # Output: alice@example.com
```

### **2.5 Ease of Maintenance**
- Use **meaningful variable names** and **consistent formatting**.
- Keep **functions short and focused**.
- **Example:** Rename vague variables.
```python
# Bad
x = 10
def f(a):
    return a * x

# Good
TAX_RATE = 0.10
def calculate_tax(amount):
    return amount * TAX_RATE
```

### **2.6 Version Control and Regular Backup**
- **Version Control (Git)** tracks changes and allows rollback.
```bash
git init
git add .
git commit -m "Initial commit"
git push origin main
```
- **Regular Backup:** Use cloud storage (Google Drive, GitHub, etc.).

---

## 3. Applying Methodologies to Test and Evaluate Code
Testing ensures software is **reliable and free of errors**.

### **3.1 Unit, Subsystem, and System Testing**
| **Testing Type** | **Purpose** | **Example** |
|----------------|------------|-------------|
| **Unit Testing** | Tests **individual functions** | `test_calculate_area()` for a `calculate_area()` function |
| **Subsystem Testing** | Tests **groups of related functions** | Checking a `User` and `Account` class work together |
| **System Testing** | Tests the **entire application** | Ensuring a full banking system runs as expected |

**Example: Unit Testing in Python (`unittest`)**
```python
import unittest

def add(a, b):
    return a + b

class TestMathFunctions(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)
        self.assertEqual(add(-1, 1), 0)

if __name__ == '__main__':
    unittest.main()
```

---

### **3.2 Black, White, and Grey Box Testing**
| **Testing Type** | **Description** |
|---------------|----------------|
| **Black Box Testing** | Tests the software **without looking at the code** (focuses on expected outputs). |
| **White Box Testing** | Examines the **internal code structure** (checks logic, paths, and conditions). |
| **Grey Box Testing** | Combines both, testing some internal logic while focusing on expected results. |

**Example:**
- **Black Box:** User **inputs login details**; expected output: "Login successful".
- **White Box:** Developer **checks the function handling login credentials**.
- **Grey Box:** Tester **uses tools to examine login flow** without accessing the full source code.

---

### **3.3 Quality Assurance (QA) in Software Development**
- **Defining Quality Criteria:**
  - Software must be **bug-free, fast, and user-friendly**.
- **Continuous Testing:**
  - Automated tests run **before deploying updates**.
- **Example: Automated Testing with `pytest`**
```bash
pytest test_script.py
```