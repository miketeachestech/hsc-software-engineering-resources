# **Answers: Programming Fundamentals (Part 2)**

## **Multiple Choice Questions**

**1.** *(1 mark)*  
- Correct Answer: **A) It allows both positive and negative numbers to be stored in the same system.**  
- **1 mark** awarded for correctly selecting the answer.  

**2.** *(1 mark)*  
- Correct Answer: **B) Stack**  
- **1 mark** awarded for correctly selecting the answer.  

**3.** *(1 mark)*  
- Correct Answer: **B) To evaluate how software handles extreme input values.**  
- **1 mark** awarded for correctly selecting the answer.  

---

## **Short Answer Questions**

**4.** *(3 marks)* Convert the decimal number **45** into **binary** and **hexadecimal**. Show your working steps.
- **1 mark** for correctly converting **45 to binary**: `45 → 101101₂`
- **1 mark** for correctly converting **45 to hexadecimal**: `45 → 2D₁₆`
- **1 mark** for showing step-by-step working.

**5.** *(3 marks)* What are the **main differences between arrays, linked lists, and hash tables**? Provide an example of when to use each.
- **1 mark** for explaining that **arrays** store elements **in contiguous memory locations** and allow **fast indexing** (e.g., storing a list of student names).
- **1 mark** for stating that **linked lists** store elements **with pointers to the next node**, allowing **efficient insertions and deletions** (e.g., implementing a dynamic menu system).
- **1 mark** for explaining that **hash tables** store **key-value pairs** for **fast lookups** (e.g., storing user login credentials in a dictionary structure).

**6.** *(3 marks)* Identify the **error(s) in the following Python function** and suggest a fix:
```python
 def divide_numbers(a, b):
    return a / b

 print(divide_numbers(10, 0))
```
- **1 mark** for identifying that dividing by zero (`b == 0`) will cause a **runtime error**.
- **1 mark** for suggesting a fix using a **try-except block**.
- **1 mark** for providing a correct fix:
```python
def divide_numbers(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Error: Cannot divide by zero"

print(divide_numbers(10, 0))
```

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a **Python function** that reads a file called `data.txt`, counts the number of lines in the file, and prints the total count.
```python
def count_lines(filename):
    try:
        with open(filename, "r") as file:
            return len(file.readlines())
    except FileNotFoundError:
        return "Error: File not found"

print(count_lines("data.txt"))
```
- **1 mark** for correctly opening the file.
- **1 mark** for reading the lines and counting them.
- **1 mark** for handling exceptions (e.g., file not found).
- **1 mark** for correct output format.

**8.** *(4 marks)* The following code aims to **find the smallest number** in a list, but it contains a bug. Identify and fix the issue.
```python
 def find_smallest(lst):
    smallest = 0
    for num in lst:
        if num < smallest:
            smallest = num
    return smallest

 numbers = [3, 1, 4, 1, 5, 9]
 print(find_smallest(numbers))
```
**Bug:** `smallest = 0` initializes the smallest value incorrectly, which may not be the smallest number in the list.

**Fixed Version:**
```python
def find_smallest(lst):
    smallest = lst[0]  # Initialize with first element
    for num in lst:
        if num < smallest:
            smallest = num
    return smallest

numbers = [3, 1, 4, 1, 5, 9]
print(find_smallest(numbers))  # Output: 1
```
- **1 mark** for identifying incorrect initialization (`smallest = 0`).
- **1 mark** for explaining that **smallest should start as the first list element**.
- **1 mark** for correcting the code (`smallest = lst[0]`).
- **1 mark** for correct output.

**9.** *(4 marks)* Given the following test cases, what type of **testing approach** (unit, integration, system, acceptance) is best suited for each scenario?

| **Test Case** | **Input** | **Expected Output** | **Best Testing Approach** |
|--------------|----------|-------------------|------------------|
| Login System | Correct username/password | User logs in successfully | **Unit Testing** |
| Payment Processing | Valid credit card details | Payment approved | **System Testing** |
| API Integration | Request to external weather API | Correct weather data returned | **Integration Testing** |
| UI Testing | Button click | Navigates to the correct page | **Acceptance Testing** |

- **1 mark** for identifying **unit testing** as checking a small function like login verification.
- **1 mark** for identifying **system testing** as evaluating a full system like payment processing.
- **1 mark** for identifying **integration testing** as testing APIs that interact with external systems.
- **1 mark** for identifying **acceptance testing** as verifying overall UI navigation from an end-user perspective.

