# **Practice Questions: Programming Fundamentals (Part 1)**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the primary function of a **selection statement** in an algorithm?  
   - A) It executes instructions sequentially without decision-making  
   - B) It repeats a set of instructions indefinitely  
   - C) It chooses between different execution paths based on conditions  
   - D) It defines a function without parameters  

**2.** *(1 mark)* Which programming paradigm focuses on **objects, classes, and inheritance**?  
   - A) Functional programming  
   - B) Procedural programming  
   - C) Object-Oriented Programming (OOP)  
   - D) Declarative programming  

**3.** *(1 mark)* Which of the following sorting algorithms follows the **divide and conquer** approach?  
   - A) Bubble Sort  
   - B) Merge Sort  
   - C) Selection Sort  
   - D) Insertion Sort  

**4.** *(1 mark)* What is the primary purpose of a **UML class diagram**?  
   - A) To show the sequence of interactions in a system  
   - B) To model the structure of a system, including attributes and relationships  
   - C) To represent the database schema of an application  
   - D) To list test cases for a software component  

**5.** *(1 mark)* What do **UML sequence diagrams** represent?  
   - A) The flow of logic in an algorithm  
   - B) The relationships between different system components  
   - C) The interactions between objects over time  
   - D) The way data is stored in a relational database  

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

**7.** *(3 marks)* Explain how **iteration (loops)** improves efficiency in algorithms. Provide an example using Python.

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

**9.** *(3 marks)* What are the key elements of a **UML class diagram**? Provide an example.

---

## **Code-Based Questions**

**10.** *(4 marks)* Write a **Python function using recursion** to calculate the factorial of a number. Provide an example of its usage.

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

