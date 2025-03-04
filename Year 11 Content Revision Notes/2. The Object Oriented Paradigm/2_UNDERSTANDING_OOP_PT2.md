# Understanding Object-Oriented Programming (OOP) Part 2 - HSC Software Engineering Revision Notes

## 1. The Process of Design in OOP Development
Object-Oriented Programming (OOP) follows structured design principles to create **modular, reusable, and scalable** software solutions.

### **1.1 Task Definition**
- The **first step** in OOP design is to clearly define the **problem** and **expected outcome**.
- This includes:
  - Identifying **key functionalities**.
  - Listing required **objects, attributes, and behaviors**.
- *Example:* In a **library system**, tasks might include **borrowing books, returning books, and managing user accounts**.

### **1.2 Top-Down vs. Bottom-Up Design**
| **Approach** | **Description** | **Example** |
|-------------|----------------|-------------|
| **Top-Down** | Starts with a high-level **overview** and breaks it down into smaller components. | Define the entire **library system**, then create separate modules for books, users, and transactions. |
| **Bottom-Up** | Starts by developing **smaller components (classes)** and integrating them into a larger system. | Create **Book**, **User**, and **Loan** classes first, then combine them into a system. |

### **1.3 Facade Pattern**
- A design pattern that **hides complex system details** behind a **simplified interface**.
- Improves **code readability and maintainability**.
- *Example:* A **Banking System API** where a user calls `withdraw_money()` without needing to handle authentication, transaction processing, and database updates separately.

#### **Python Example Using the Facade Pattern**
```python
class Account:
    def __init__(self, balance):
        self.balance = balance

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            return f"Withdrawal successful! Remaining balance: {self.balance}"
        return "Insufficient funds"

class Bank:
    def __init__(self):
        self.account = Account(1000)
    
    def withdraw_money(self, amount):
        return self.account.withdraw(amount)

# Simplified interface for user
my_bank = Bank()
print(my_bank.withdraw_money(200))  # Output: Withdrawal successful! Remaining balance: 800
```

### **1.4 Agility in OOP Development**
- **Agility** means adapting the design as new requirements emerge.
- Allows **incremental development** and **continuous improvement**.
- Common agile methodologies:
  - **Scrum** (work in sprints, frequent feedback)
  - **Kanban** (visualize workflow, reduce bottlenecks)
- *Example:* An online store might first release a **basic shopping cart feature** and later integrate **AI-powered recommendations**.

---

## 2. Assessing the Effectiveness of OOP Code Implementing an Algorithm
Effective OOP code should be:
✅ **Correct** – Produces expected results.
✅ **Efficient** – Uses minimal resources (CPU, memory).
✅ **Readable** – Easy to understand and maintain.
✅ **Scalable** – Can handle more features in the future.

#### **Example: Optimizing a Search Algorithm Using OOP**
```python
class Search:
    def __init__(self, data):
        self.data = sorted(data)  # Sorting improves efficiency
    
    def binary_search(self, target):
        left, right = 0, len(self.data) - 1
        while left <= right:
            mid = (left + right) // 2
            if self.data[mid] == target:
                return f"Found at index {mid}"
            elif self.data[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
        return "Not found"

numbers = Search([10, 2, 8, 5, 3])
print(numbers.binary_search(8))  # Output: Found at index 2
```

---

## 3. Investigating Message Passing Between Objects in OOP
Message passing allows **objects to interact** by calling each other's methods.

### **Example: Message Passing Between Objects**
```python
class User:
    def __init__(self, name):
        self.name = name
    
    def greet(self):
        return f"Hello, {self.name}!"

class ChatBot:
    def __init__(self):
        self.user = None
    
    def register_user(self, user):
        self.user = user
    
    def start_conversation(self):
        if self.user:
            return self.user.greet()
        return "No user registered."

user1 = User("Alice")
bot = ChatBot()
bot.register_user(user1)
print(bot.start_conversation())  # Output: Hello, Alice!
```
- The **ChatBot object sends a message** to the **User object** by calling `greet()`.
- Objects communicate through **method calls**.

---

## 4. Code Optimization in Software Engineering
Code optimization improves **efficiency, speed, and memory usage**.

### **Common Code Optimization Techniques**
| **Optimization** | **Description** |
|-----------------|----------------|
| **Loop Unrolling** | Reduces loop overhead by executing multiple iterations at once. |
| **Using Built-in Functions** | Faster than manually implementing algorithms. |
| **Memory Management** | Reducing memory usage (e.g., using generators instead of lists). |

#### **Example: Optimized vs. Unoptimized Code**
```python
# Unoptimized: Uses a loop to sum numbers
sum_total = 0
for i in range(1, 1001):
    sum_total += i

# Optimized: Uses built-in sum function
sum_total = sum(range(1, 1001))
```

---

## 5. Features of OOP That Support Collaborative Development

Object-Oriented Programming (OOP) enhances team-based software development by promoting structured, reusable, and modular code. This makes collaboration more efficient and scalable.

### 5.1 Consistency Through Class-Based Design

- OOP enforces a predictable structure by using classes and objects.
- Developers can quickly understand and extend the code without disrupting existing functionality.
- **Example:** If a team follows an OOP class hierarchy, all developers know where specific functionality (e.g., authentication, data storage) is located.

```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

    def start_engine(self):
        return "Engine started"

class Car(Vehicle):  # Consistent structure for all vehicle types
    def honk(self):
        return "Honk Honk!"
```

Any developer working on trucks or motorcycles can extend this system without modifying the core `Vehicle` class.

### 5.2 Code Readability and Maintainability

- OOP enforces code separation through encapsulation, making large projects easier to manage.
- Class structures allow different teams to work on different parts of a system without conflicts.
- **Example:** A database team can manage a `DatabaseHandler` class while the UI team focuses on a `UserInterface` class.

```python
class DatabaseHandler:
    def connect(self):
        return "Connecting to database"

class UserInterface:
    def display(self):
        return "Showing UI"
```

**Benefit:** Teams work independently but their code integrates seamlessly.

### 5.3 Version Control and Object Modularity

- Encapsulation and modular classes ensure smaller, independent code changes in team environments.
- Each developer can work on separate classes without modifying others, reducing merge conflicts in Git.
- **Example:** A feature like "User Authentication" can be built as an independent class and tested separately.

```python
class Authenticator:
    def login(self, username, password):
        return f"Logging in {username}"

    def logout(self):
        return "Logging out"
```

The front-end and back-end teams only need to interact with the `Authenticator` API, ensuring clear role separation.

### 5.4 Code Commenting and Documentation in OOP

- Docstrings and comments help teams understand class structures without needing deep code analysis.
- Consistent commenting standards ensure all developers follow the same documentation approach.

```python
class PaymentProcessor:
    """
    Handles payment transactions securely.
    """

    def process_payment(self, amount):
        """
        Processes a payment.
        :param amount: The amount to be processed.
        :return: Confirmation message.
        """
        return f"Processing payment of ${amount}"
```

**Benefit:** Future developers can extend or debug this class without confusion.

### 5.5 Collaboration Through Interfaces and Inheritance

- Teams can agree on class structures before writing code.
- Interfaces and abstract classes define consistent behaviors across multiple developers.
- **Example:** A shared `Animal` interface ensures all subclasses implement `make_sound()`, regardless of the developer.

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "Bark!"

class Cat(Animal):
    def make_sound(self):
        return "Meow!"
```

**Benefit:** Different teams can work on `Dog` and `Cat` without breaking the base structure.
