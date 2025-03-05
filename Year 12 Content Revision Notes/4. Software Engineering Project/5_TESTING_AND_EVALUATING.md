# Testing and Evaluating - HSC Software Engineering Revision Notes

## 1. Applying Methodologies to Test and Evaluate Code
Testing is a **crucial part of software engineering** to ensure code functions correctly, efficiently, and securely. Different testing methodologies help identify errors and improve software reliability.

### **Common Testing Methodologies**
| **Methodology** | **Purpose** | **Example** |
|----------------|------------|-------------|
| **Unit Testing** | Tests individual functions or components | Ensuring a function correctly adds two numbers |
| **Integration Testing** | Tests how different parts of the system work together | Checking if the login system correctly accesses the user database |
| **System Testing** | Tests the entire software in a real-world scenario | Running an e-commerce site end-to-end from browsing to checkout |
| **Acceptance Testing** | Ensures the software meets business and user requirements | Verifying if an online booking system meets client expectations |

### **Example: Unit Testing in Python (Using `unittest`)**
```python
import unittest

def add(x, y):
    return x + y

class TestMathFunctions(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)
        self.assertEqual(add(-1, 1), 0)

if __name__ == '__main__':
    unittest.main()
```

---

## 2. Using a Language-Dependent Code Optimisation Technique
Code optimisation improves **performance, speed, and memory efficiency**. Techniques vary by programming language.

### **Example: Optimising Python Code Using List Comprehensions**
Inefficient code using a loop:
```python
numbers = [1, 2, 3, 4, 5]
squared = []
for num in numbers:
    squared.append(num ** 2)
```
Optimised code using list comprehensions:
```python
squared = [num ** 2 for num in numbers]
```
- **Faster execution**
- **Less memory usage**

---

## 3. Analysing and Responding to Feedback
Feedback helps improve software functionality, usability, and performance.

### **Methods of Collecting Feedback**
- **User Feedback Forms** – Gather input from real users.
- **Bug Reports & Logs** – Track errors in production.
- **Performance Metrics** – Monitor system speed and load times.

### **Example: User Feedback Implementation (HTML Form)**
```html
<form action="/submit-feedback" method="post">
    <label for="feedback">Your Feedback:</label>
    <textarea id="feedback" name="feedback"></textarea>
    <button type="submit">Submit</button>
</form>
```

---

## 4. Evaluating the Effectiveness of a Software Engineering Solution
A software solution must be tested against **functionality, performance, and usability** to determine its effectiveness.

### **Developing a Report to Synthesise Feedback**
A software evaluation report should include:
1. **Summary of Findings** – Key strengths and weaknesses.
2. **User Feedback Summary** – Common issues reported.
3. **Performance Data** – Response times, memory usage.
4. **Action Plan** – Proposed improvements.

### **Developing a Test Plan**
A structured test plan ensures **thorough testing** of software components.

#### **Example Test Plan Table**
| **Test Case** | **Input** | **Expected Output** | **Actual Output** | **Pass/Fail** |
|--------------|----------|-------------------|-----------------|------------|
| Login Test | Valid username/password | User logs in | User logs in | Pass |
| Login Test | Invalid password | Error message | No error shown | Fail |
| Payment Processing | Valid card details | Payment successful | Payment failed | Fail |

### **Testing Data Based on Path and Boundary Testing**
- **Path Testing:** Tests different execution paths.
  - Example: Checking if a user can **log in with a valid password and logout correctly**.
- **Boundary Testing:** Tests **edge cases**.
  - Example: Ensuring **password fields reject inputs shorter than 8 characters**.

### **Manual Testing**
Manual testing involves human testers interacting with the software to identify bugs, usability issues, and inconsistencies that automated tests might miss.

#### **Types of Manual Testing**
- **Exploratory Testing** – Testers explore the software without predefined test cases.
- **Ad-hoc Testing** – Unstructured testing without a formal plan.
- **Usability Testing** – Evaluating the user-friendliness of the application.
- **Regression Testing** – Manually rechecking fixed issues to ensure they don't reappear.

#### **Example Manual Testing Checklist for a Web Application**
- ✅ Verify all buttons and links work correctly.
- ✅ Ensure the login system properly handles valid and invalid inputs.
- ✅ Check for broken images or incorrect layouts.
- ✅ Test responsiveness on different devices and browsers.

### **Comparing Actual Output with Expected Output**
- If the actual output matches expectations, the test **passes**.
- If there’s a mismatch, **debugging is required**.

#### **Example: Debugging an Unexpected Output in Python**
```python
def divide(a, b):
    return a / b  # Might cause division by zero error

try:
    result = divide(10, 0)
except ZeroDivisionError:
    result = "Error: Division by zero is not allowed"
print(result)
```

---

## 5. Congratulations!
You made it to the end of the HSC Software Engineering Year 12 content! Be proud of yourself for sticking with it, it's not an easy subject. A lot of these concepts were introduced to me in my first couple years of University back when I was a wee student like you. I wouldn't have even called myself remotely competent at this stuff until after my first year working as a software engineer in 2019. I think I would have struggled trying to perfect all of this in Years 11 and 12. So if that's what you're striving for, you have my respect. You're a badass. Keep at it, and who knows - maybe one day you'll be my boss. Remember to be kind to others, and most importantly, remember to be kind to yourself. The HSC is not the be all and end all. All the best to you.
