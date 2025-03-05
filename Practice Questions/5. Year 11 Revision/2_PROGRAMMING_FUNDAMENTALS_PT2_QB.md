# **Practice Questions: Programming Fundamentals (Part 2)**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the **primary advantage** of using two’s complement for representing negative numbers?  
   - A) It allows both positive and negative numbers to be stored in the same system.  
   - B) It eliminates the need for a sign bit.  
   - C) It makes binary calculations more complex.  
   - D) It prevents integer overflow errors.  

**2.** *(1 mark)* Which **data structure** follows the **LIFO (Last-In, First-Out)** principle?  
   - A) Queue  
   - B) Stack  
   - C) Hash Table  
   - D) Binary Search Tree  

**3.** *(1 mark)* What is the purpose of **boundary testing** in software evaluation?  
   - A) To test the most commonly used features of the software.  
   - B) To evaluate how software handles extreme input values.  
   - C) To check if all user interface elements are functional.  
   - D) To verify network connectivity in a web application.  

---

## **Short Answer Questions**

**4.** *(3 marks)* Convert the decimal number **45** into **binary** and **hexadecimal**. Show your working steps.

**5.** *(3 marks)* What are the **main differences between arrays, linked lists, and hash tables**? Provide an example of when to use each.

**6.** *(3 marks)* Identify the **error(s) in the following Python function** and suggest a fix:
```python
 def divide_numbers(a, b):
    return a / b

 print(divide_numbers(10, 0))
```

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a **Python function** that reads a file called `data.txt`, counts the number of lines in the file, and prints the total count. 

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

**9.** *(4 marks)* Given the following test cases, what type of **testing approach** (unit, integration, system, acceptance) is best suited for each scenario?

| **Test Case** | **Input** | **Expected Output** | **Best Testing Approach** |
|--------------|----------|-------------------|------------------|
| Login System | Correct username/password | User logs in successfully | ? |
| Payment Processing | Valid credit card details | Payment approved | ? |
| API Integration | Request to external weather API | Correct weather data returned | ? |
| UI Testing | Button click | Navigates to the correct page | ? |