# Research and Planning Part 2 - HSC Software Engineering Revision Notes

## 1. Applying Project Management to Software Development
Project management ensures that **software projects are completed on time, within budget, and meet quality standards**.

### **Scheduling and Tracking Using a Software Tool (Gantt Charts)**
- **Gantt charts** visually represent project timelines and dependencies.
- Help teams track **task progress, deadlines, and milestones**.
- *Example:* A Gantt chart for a web development project may include tasks like **requirement gathering, coding, testing, and deployment**.

#### **Example Gantt Chart Structure:**
```
| Task            | Start Date | End Date  | Status      |
|-----------------|------------|-----------|-------------|
| Requirements    | Day 1      | Day 5     | Completed   |
| Development     | Day 6      | Day 20    | In Progress |
| Testing         | Day 21     | Day 25    | Not Started |
| Deployment      | Day 26     | Day 30    | Not Started |
```

### **Using Collaboration Tools**
- **Version Control Systems (Git, GitHub, GitLab)** – Track code changes and manage teamwork.
- **Project Management Platforms (Trello, Jira, Asana)** – Organize tasks and assignments.
- **Communication Tools (Slack, Microsoft Teams)** – Facilitate discussions and meetings.
- *Example:* Developers use GitHub for **code reviews and issue tracking**.

---

## 2. Social and Ethical Issues in Project Work
Software development impacts **individuals, teams, and stakeholders**, raising ethical concerns.

### **Working Individually vs. Collaboratively**
- **Individual work**: Allows focus but lacks **feedback and teamwork**.
- **Collaborative work**: Encourages **diverse ideas and faster problem-solving**.
- *Example:* Open-source projects involve multiple developers worldwide working on the same codebase.

### **Responding to Stakeholders**
- Developers must **consider the needs of users, clients, and regulatory bodies**.
- Ethical concerns include **privacy, security, and accessibility**.
- *Example:* A healthcare app must follow **patient data protection laws**.

---

## 3. Communication Issues in Project Work
Effective communication ensures **smooth collaboration and project success**.

### **Involving and Empowering the Client**
- Clients should be **actively involved in development** to ensure their needs are met.
- *Example:* Regular meetings and user testing allow clients to provide feedback.

### **Enabling Feedback**
- Feedback loops help improve software before release.
- Can be collected through **user testing, surveys, or analytics**.
- *Example:* Beta testing apps allow developers to fix **bugs before the official launch**.

### **Negotiating**
- Negotiation is essential for **feature prioritization, deadlines, and budgets**.
- Developers must **balance technical feasibility with client expectations**.
- *Example:* A client wants a feature added, but the team negotiates a later release due to time constraints.

---

## 4. Ensuring Software Engineering Solutions Are Quality Assured
Quality assurance (QA) ensures that software is **reliable, secure, and meets user expectations**.

### **Defining Criteria for Quality**
- **Functionality** – Does the software perform as intended?
- **Performance** – Is it fast and efficient?
- **Security** – Is user data protected?
- *Example:* An e-commerce website must have **fast page loading and secure payment processing**.

### **Continual Checking Process**
- QA is **not just a final step**—testing is done **throughout development**.
- Includes **unit tests, integration tests, and system tests**.
- *Example:* Developers use **automated tests** to detect code errors early.

### **Compliance and Legislative Requirements**
- Software must adhere to **legal and regulatory standards**.
- Examples:
  - **GDPR (General Data Protection Regulation)** – Data privacy compliance.
  - **WCAG (Web Content Accessibility Guidelines)** – Ensuring websites are accessible.
- *Example:* A banking app must follow **financial data protection laws**.

---

## 5. Demonstrating the Use of Modelling Tools
Modelling tools help visualize software structure and behavior.

### **Common Modelling Tools**
- **UML Diagrams (Unified Modeling Language)** – Represents system architecture (e.g. class diagram, sequence diagram).
- **Flowcharts** – Shows logic and processes.
- **Entity-Relationship Diagrams (ERDs)** – Maps database relationships.

---

## 6. The Contribution of Back-End Engineering to Software Development
The back-end is responsible for **handling business logic, processing data, and communicating with the front-end**.

### **Technology Used**
- **Programming Languages:** Python (Flask, Django), JavaScript (Node.js), Java (Spring Boot).
- **Databases:** MySQL, PostgreSQL, MongoDB.
- **APIs:** RESTful APIs allow front-end and back-end communication.

### **Error Handling**
- Prevents software crashes and improves stability.
- Uses **try-except blocks** in Python, `try-catch` in JavaScript.
- *Example:* Handling a failed API request in Python:
  ```python
  try:
      response = requests.get("https://api.example.com/data")
      response.raise_for_status()
  except requests.exceptions.RequestException as e:
      print(f"Error fetching data: {e}")
  ```

### **Interfacing with Front-End**
- Back-end **provides data** to the front-end via **APIs**.
- Uses **JSON or XML** to format responses.
- *Example:* A front-end React app fetches data from a Flask back-end:
  ```python
  from flask import Flask, jsonify

  app = Flask(__name__)

  @app.route('/data')
  def get_data():
      return jsonify({"message": "Hello from the back-end!"})
  
  if __name__ == '__main__':
      app.run(debug=True)
  ```

### **Security Engineering**
- Protects systems from **hacking and data breaches**.
- Uses **encryption, authentication, and secure APIs**.
- *Example:* Implementing **JWT (JSON Web Token) authentication**:
  ```python
  import jwt
  SECRET_KEY = "mysecretkey"
  token = jwt.encode({"user_id": 123}, SECRET_KEY, algorithm="HS256")
  print(token)
  ```