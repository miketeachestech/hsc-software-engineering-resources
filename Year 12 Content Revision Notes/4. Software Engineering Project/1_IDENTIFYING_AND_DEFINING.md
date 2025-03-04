# Identifying and Defining - HSC Software Engineering Revision Notes

## 1. Defining and Analyzing the Requirements of a Problem
When developing software, it is essential to first **identify the problem** and analyze what is needed to create an effective solution. This involves understanding **user needs, technical constraints, and business goals**.

### **Demonstrating Need(s) or Opportunities**
- Understanding **why the software is needed**.
- Identifying **gaps in existing solutions** or **new opportunities** for improvement.
- *Example:* A local business struggles with **manual appointment scheduling**, presenting an opportunity to build an **automated booking system**.

### **Assessing Scheduling and Financial Feasibility**
- Determining **time constraints** for development.
- Evaluating **costs for development, hosting, and maintenance**.
- *Example:* A startup may only have a **3-month timeline and a limited budget**, requiring an **MVP (Minimum Viable Product)** approach.

### **Generating Requirements (Functionality and Performance)**
- Defining **core features** the software must have (e.g., login system, reporting dashboard).
- Establishing **performance expectations** (e.g., loading times under 2 seconds).
- *Example:* An e-commerce site must support **500 concurrent users and secure payments**.

### **Defining Data Structures and Data Types**
- Identifying how data will be **stored, processed, and accessed**.
- Selecting **appropriate data types** for efficiency.
- *Example:* A user database may have:
  ```sql
  CREATE TABLE Users (
      user_id INT PRIMARY KEY,
      name VARCHAR(100),
      email VARCHAR(255),
      signup_date DATE
  );
  ```

### **Defining Boundaries**
- Setting **limits** on what the software will and won’t do.
- Preventing **scope creep** (uncontrolled expansion of project goals).
- *Example:* A mobile app for fitness tracking **will not include meal planning features** in its initial release.

---

## 2. Tools for Developing Ideas and Generating Solutions
Once requirements are defined, developers use various tools to **brainstorm, design, and validate solutions**.

### **Brainstorming, Mind-Mapping, and Storyboards**
- **Brainstorming:** Generates ideas for potential solutions.
- **Mind-Mapping:** Visually connects different aspects of the project.
- **Storyboards:** Outline **user flows and interface design**.
- *Example:* A storyboard might map out a **user's journey from login to checkout** in an online store.

### **Data Dictionaries (Selecting Appropriate Data Types)**
- **Data dictionaries document the structure of databases**.
- They define **tables, attributes, data types, and constraints**.
- *Example:* A simplified dictionary entry:
  ```
  Field: Order_ID | Type: INT | Description: Unique identifier for an order
  ```

### **Algorithm Design**
- Creating **logical steps** to solve a problem.
- Can be expressed in **pseudocode or flowcharts**.
- *Example:* Sorting a list in ascending order using a bubble sort algorithm:
  ```python
  def bubble_sort(arr):
      for i in range(len(arr)):
          for j in range(0, len(arr) - i - 1):
              if arr[j] > arr[j + 1]:
                  arr[j], arr[j + 1] = arr[j + 1], arr[j]
      return arr
  ```

### **Code Generation**
- Writing the **initial structure of the software**.
- Using **frameworks** to speed up development (e.g., Flask for Python web apps).
- Instead of having to write everything in raw Python, the framework offers you a simple abstraction.
- *Example:* Generating a simple Flask API:
  ```python
  from flask import Flask
  app = Flask(__name__)

  @app.route('/')
  def home():
      return "Hello, World!"

  if __name__ == '__main__':
      app.run(debug=True)
  ```

### **Testing and Debugging**
- Ensuring the software **works correctly** before release.
- Using **unit tests, integration tests, and manual testing**.
- *Example:* Writing a simple unit test:
  ```python
  import unittest
  
  def add(a, b):
      return a + b
  
  class TestMath(unittest.TestCase):
      def test_add(self):
          self.assertEqual(add(2, 3), 5)
  
  if __name__ == '__main__':
      unittest.main()
  ```

### **Installation and Maintenance**
- **Installation:** Deploying the software for end-users.
- **Maintenance:** Updating and fixing bugs **post-launch**.
- *Example:* Releasing a **security patch** after detecting a vulnerability.

---

## 3. Investigating Software Implementation Methods
Different projects use different strategies to **deploy new software**. Choosing the right method depends on **risk tolerance, project complexity, and user impact**.

### **Direct Implementation**
- The old system is **immediately replaced** with the new system.
- **Fast but risky**—if there are problems, the system might fail.
- *Example:* A hospital upgrades its patient management system overnight.

### **Phased Implementation**
- The new system is **introduced in stages**.
- **Lower risk**, as changes are tested gradually.
- *Example:* An online banking app releases new features **one at a time**.

### **Parallel Implementation**
- The old and new systems **run side by side** until the new system is fully tested.
- **Safest but most expensive**—requires maintaining two systems.
- *Example:* A company runs both a **legacy accounting system and a new cloud-based system** for several months.

### **Pilot Implementation**
- The new system is **tested in one location or with a small group** before full deployment.
- **Allows for early feedback and fixes** before full release.
- *Example:* A university tests its **new grading system** with one faculty before expanding it campus-wide.