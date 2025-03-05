# **Answers: Programming Fundamentals (Part 1)**

## **Multiple Choice Questions**

**1.** *(1 mark)*  
- Correct Answer: **C) It chooses between different execution paths based on conditions**  
- **1 mark** awarded for correctly selecting the answer.  

**2.** *(1 mark)*  
- Correct Answer: **C) Object-Oriented Programming (OOP)**  
- **1 mark** awarded for correctly selecting the answer.  

**3.** *(1 mark)*  
- Correct Answer: **B) Merge Sort**  
- **1 mark** awarded for correctly selecting the answer.  

**4.** *(1 mark)*  
- Correct Answer: **B) To model the structure of a system, including attributes and relationships**  
- **1 mark** awarded for correctly selecting the answer.  

**5.** *(1 mark)*  
- Correct Answer: **C) The interactions between objects over time**  
- **1 mark** awarded for correctly selecting the answer.  

---

## **Short Answer Questions**

**6.** *(3 marks)* Identify and explain the **error(s) in the following Python function**, and suggest a fix.
```python
 def add_numbers(a, b):
    sum = a + b
    print(sum)
    return sum

 print(add_numbers(5))
```
- **1 mark** for identifying that `add_numbers(5)` is missing a second argument.
- **1 mark** for explaining that Python will raise a `TypeError` because `b` is required but missing.
- **1 mark** for providing a correct fix:
```python
print(add_numbers(5, 3))  # Adding a second argument
```

**7.** *(3 marks)* Explain how **iteration (loops)** improves efficiency in algorithms. Provide an example using Python.
- **1 mark** for stating that iteration **reduces repetitive code** and improves efficiency.
- **1 mark** for explaining that **loops allow processing large datasets without manual repetition**.
- **1 mark** for providing an example (e.g., a loop to sum numbers in a list):
```python
numbers = [1, 2, 3, 4, 5]
total = 0
for num in numbers:
    total += num
print(total)  # Output: 15
```

**8.** *(3 marks)* Given the following pseudocode, describe its **purpose and expected output**:
```
BEGIN
    INPUT num
    WHILE num > 0 DO
        PRINT num
        num ← num - 1
    END WHILE
END
```
- **1 mark** for explaining that the pseudocode **counts down from a given number to 1**.
- **1 mark** for describing that the `WHILE` loop **executes until `num` is no longer greater than 0**.
- **1 mark** for providing an expected output example (if `num` is 5):
```
5
4
3
2
1
```

**9.** *(3 marks)* What are the key elements of a **UML class diagram**? Provide an example.
- **1 mark** for explaining that a UML class diagram consists of **classes, attributes, and methods**.
- **1 mark** for stating that relationships between classes (e.g., inheritance, association) are represented.
- **1 mark** for providing an example of a class diagram (e.g., `User` class with `name`, `email`, and `login()` method).

---

## **Code-Based Questions**

**10.** *(4 marks)* Write a **Python function using recursion** to calculate the factorial of a number. Provide an example of its usage.
```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```
- **1 mark** for correctly defining the base case (`if n == 0, return 1`).
- **1 mark** for correctly calling the function recursively (`n * factorial(n - 1)`).
- **1 mark** for using a return statement instead of print inside the function.
- **1 mark** for demonstrating an example call and expected output.

**11.** *(4 marks)* The following code aims to **find the largest number** in a list. However, it contains a bug. Identify and fix the issue.
```python
 def find_largest(lst):
    largest = 0
    for num in lst:
        if num > largest:
            largest = num
    return largest

 numbers = [-5, -1, -9, -3]
 print(find_largest(numbers))
```
**Bug:** The code initializes `largest = 0`, which may be greater than negative numbers in `lst`.

**Fixed Version:**
```python
def find_largest(lst):
    largest = lst[0]  # Initialize with first element
    for num in lst:
        if num > largest:
            largest = num
    return largest

numbers = [-5, -1, -9, -3]
print(find_largest(numbers))  # Output: -1
```
- **1 mark** for identifying the incorrect initialization (`largest = 0`).
- **1 mark** for explaining the impact on negative numbers.
- **1 mark** for correcting the initialization (`largest = lst[0]`).
- **1 mark** for providing a correct example execution and expected output.

**12.** *(4 marks)* Convert the following **Python code into a UML sequence diagram representation**.
```python
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True
```
- **1 mark** for representing the function call from a user or main program.
- **1 mark** for illustrating the loop checking divisibility of `n`.
- **1 mark** for including a return message (`True` or `False`).
- **1 mark** for proper UML sequence diagram notation.
