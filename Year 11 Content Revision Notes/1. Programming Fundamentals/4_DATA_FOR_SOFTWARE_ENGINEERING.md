# Data for Software Engineering - HSC Software Engineering Revision Notes

## 1. Investigating Number Systems in Computing
Computers use **different number systems** for **data storage, processing, and memory addressing**.

### **1.1 Common Number Systems**
| **Number System** | **Base** | **Uses** |
|------------------|---------|----------|
| **Binary (Base 2)** | 2 | Used in all computer operations (0s and 1s). |
| **Decimal (Base 10)** | 10 | Standard number system for humans. |
| **Hexadecimal (Base 16)** | 16 | Used in color codes, memory addresses, and compact binary representation. |

### **1.2 Example Conversions**
#### **Binary to Decimal**
Binary `1010` → `(1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰) = 10`

#### **Decimal to Binary**
Decimal `13` → Binary `1101`

#### **Hexadecimal to Decimal**
Hex `1F` → `(1 × 16¹) + (15 × 16⁰) = 31`

#### **Binary to Hexadecimal**
Binary `11011011` → Split into `1101` (D) and `1011` (B) → Hex `DB`

---

## 2. Representing Integers Using Two’s Complement
**Two’s complement** is used to represent **negative numbers** in binary.

### **How Two’s Complement Works**
1. **Convert number to binary.**
2. **Invert all bits (flip 0s to 1s and 1s to 0s).**
3. **Add 1 to the inverted bits.**

### **Example: Representing -5 in 8-bit Binary**
1. `5` in binary (8-bit): `00000101`
2. Invert: `11111010`
3. Add 1: `11111011` → **This represents -5** in two’s complement.

---

## 3. Investigating Standard Data Types
Data types determine **how information is stored and processed in memory**.

| **Data Type** | **Description** | **Example** |
|-------------|----------------|------------|
| **Char** | A single character | 'A' |
| **String** | A sequence of characters | "Hello World" |
| **Boolean** | True or False values | `True`, `False` |
| **Real** | A decimal/fractional number | 3.14 |
| **Single Precision Floating Point** | A floating-point number stored in **4 bytes** | 1.2345E+10 |
| **Integer** | A whole number (positive or negative) | -100, 0, 42 |
| **Date and Time** | Stores dates and time values | `2024-03-06 14:30:00` |

### **Example in Python**
```python
char_example = 'A'  # Char
string_example = "Hello World"  # String
boolean_example = True  # Boolean
real_example = 3.14  # Real number
integer_example = 42  # Integer
from datetime import datetime
date_example = datetime.now()  # Date & Time
```

---

## 4. Creating Data Dictionaries
A **data dictionary** documents how data is **structured and stored**, defining field names, data types, and relationships.

### **Example Data Dictionary for a Student Database**
| **Field Name** | **Data Type** | **Description** |
|--------------|-------------|----------------|
| `Student_ID` | Integer | Unique identifier for each student |
| `First_Name` | String | First name of the student |
| `Last_Name` | String | Last name of the student |
| `DOB` | Date | Date of birth |
| `Enrolled` | Boolean | Indicates if student is currently enrolled |

---

## 5. Using Data Structures
Data structures **organize and store data efficiently**.

### **5.1 Arrays**
- **Ordered collection of elements**.
- Used for **storing lists of items**.
- *Example:* List of student names.

#### **Python Example**
```python
students = ["Alice", "Bob", "Charlie"]
print(students[0])  # Output: Alice
```

### **5.2 Records (Tuples in Python, Structs in C)**
- **Stores different types of related data together**.
- *Example:* A student record.

#### **Python Example Using Dictionaries**
```python
student = {"ID": 101, "Name": "Alice", "DOB": "2005-06-01"}
print(student["Name"])  # Output: Alice
```

### **5.3 Trees**
- **Hierarchical data structure with parent-child relationships**.
- Used in **file systems, decision trees, and database indexes**.

#### **Example: Binary Search Tree (BST) Representation**
```
       10
      /  \
     5    15
    / \   /  \
   2   7 12  20
```

#### **Python Example**
```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def insert(root, value):
    if root is None:
        return Node(value)
    if value < root.value:
        root.left = insert(root.left, value)
    else:
        root.right = insert(root.right, value)
    return root
```

### **5.4 Sequential Files**
- **Stores data in a specific order**.
- Used in **logs, configuration files, and databases**.

#### **Example: Writing to a Sequential File in Python**
```python
with open("students.txt", "w") as file:
    file.write("Alice, 2005-06-01\n")
    file.write("Bob, 2006-08-15\n")
```

#### **Example: Reading from a Sequential File in Python**
```python
with open("students.txt", "r") as file:
    for line in file:
        print(line.strip())
```