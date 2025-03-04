# Designing Web Applications Part 3 - HSC Software Engineering Revision Notes

## 1. Contribution of Back-End Development to Web Applications
Back-end development is essential for **data processing, business logic, and communication between the client (front-end) and the server**. A well-designed back-end ensures **security, scalability, and efficiency** of web applications.

### Key Functions of Back-End Development
- **Handles User Authentication** (e.g., login systems)
- **Processes Business Logic** (e.g., calculations, transactions)
- **Manages Databases** (e.g., storing user data)
- **Provides APIs for Front-End Communication**

*Example:* Simple Flask back-end handling user login:
```python
from flask import Flask, request, jsonify
app = Flask(__name__)

@app.route('/login', methods=['POST'])
def login():
    data = request.json
    if data['username'] == 'admin' and data['password'] == 'password':
        return jsonify({'message': 'Login successful'})
    return jsonify({'message': 'Invalid credentials'})

if __name__ == '__main__':
    app.run(debug=True)
```

### How the Back-End and Front-End Can Exist Separately
Modern web applications often separate the front-end and back-end using **microservices** and **RESTful APIs**. This separation improves **scalability, maintainability, and performance**.

#### Simple Web App Infrastructure:
```
  User ---> Browser (Front-End) ---> API Server (Back-End) ---> Database
```
A **front-end** (React, Vue.js, or a mobile app) interacts with a **back-end API** (Flask, Node.js) that processes requests and retrieves data from a **database** (MySQL, MongoDB).

#### Example of a Microservices Approach:
```
              +-------------------+
              |  Front-End (UI)   |
              +-------------------+
                        |
        ---------------------------------
        |               |               |
 +--------------+ +--------------+ +--------------+
 |  Auth API   | |  Data API   | |  Payment API |
 +--------------+ +--------------+ +--------------+
        |               |               |
 +--------------+ +--------------+ +--------------+
 |  User DB    | |  Products DB | |  Payments DB |
 +--------------+ +--------------+ +--------------+
```
This setup allows different teams to work on **independent services**, making it easier to scale and maintain applications.

---

## 2. The Back-End Process for Managing a Web Request
When a user interacts with a web application (e.g., submitting a form), a series of **back-end processes** handle the request.

### 1. Role of Webserver Software
- Web servers (**Apache, Nginx, Gunicorn**) process **HTTP requests**.
- They **route requests** to appropriate back-end services and return responses to the client.

### 2. Web Framework
- Web frameworks (**Flask, Django, Express.js**) simplify back-end development.
- Provide **routing, templating, and middleware** support.
- *Example:* Flask routes a request:
  ```python
  from flask import Flask
  app = Flask(__name__)
  
  @app.route("/")
  def home():
      return "Hello, World!"
  
  if __name__ == "__main__":
      app.run(debug=True)
  ```

### 3. Objects and Libraries
- **Objects** store structured data (e.g., user details, posts).
- **Libraries** extend functionality (e.g., `requests` for API calls in Python).
- *Example:* Using a library to fetch data:
  ```python
  import requests
  response = requests.get("https://api.example.com/data")
  print(response.json())
  ```

### 4. Databases
- Store and retrieve data efficiently.
- Use **SQL (MySQL, PostgreSQL)** or **NoSQL (MongoDB, Firebase)**.
- *Example:* Querying a database in SQLite3:
  ```python
  import sqlite3
  conn = sqlite3.connect('data.db')
  cursor = conn.cursor()
  cursor.execute("SELECT * FROM users")
  print(cursor.fetchall())
  conn.close()
  ```

---

## 3. Developing a Web Application with Shell Scripts
Shell scripts help automate **file management and text processing**.

### Create Directories and Files
```bash
mkdir my_web_app
cd my_web_app
mkdir static templates
touch app.py database.db
```

### Search for Text in a File
```bash
grep "ERROR" logs.txt  # Finds lines containing 'ERROR'
```

---

## 4. Applying SQL Queries in a Web-Based Database
SQL allows back-end applications to **store, filter, and retrieve data** efficiently.

### Selecting Fields
```sql
SELECT username, email FROM users;
```

### Incorporating `GROUP BY`
```sql
SELECT role, COUNT(*) FROM users GROUP BY role;
```

### Common SQL Queries
- **Insert Data:**
  ```sql
  INSERT INTO users (name, email) VALUES ('Alice', 'alice@example.com');
  ```
- **Update Data:**
  ```sql
  UPDATE users SET email='new@example.com' WHERE name='Alice';
  ```
- **Delete Data:**
  ```sql
  DELETE FROM users WHERE name='Alice';
  ```

### Constraints Using `WHERE`
```sql
SELECT * FROM users WHERE age > 18;
```

### Table Joins
```sql
SELECT users.name, orders.product FROM users
JOIN orders ON users.id = orders.user_id;
```

---

## 5. Comparing Object-Relational Mapping (ORM) and SQL
ORM allows developers to interact with a database using **objects instead of raw SQL queries**.

### SQL Approach
```python
import sqlite3
conn = sqlite3.connect('database.db')
cursor = conn.cursor()
cursor.execute("SELECT * FROM users")
users = cursor.fetchall()
conn.close()
```

### ORM Approach (Using Flask SQLAlchemy)
```python
from flask_sqlalchemy import SQLAlchemy

db = SQLAlchemy()
class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(100))

users = User.query.all()
```

### Pros and Cons
| Feature | SQL | ORM |
|---------|-----|-----|
| Performance | Faster | Slightly slower |
| Complexity | Requires manual queries | Easier with object handling |
| Flexibility | Full SQL control | Abstracts database logic |

---

## 6. Collaboration Between Front-End and Back-End Developers
Effective collaboration ensures **efficient and maintainable** web solutions.

### How Collaboration Improves Development
- **API Documentation:** Clearly defines how front-end communicates with back-end.
- **Version Control (Git):** Tracks changes across both teams.
- **CI/CD Pipelines:** Automates testing and deployment.

### Example Workflow
1. **Front-End Developer:** Requests API endpoints for user authentication.
2. **Back-End Developer:** Builds the API and shares documentation.
3. **Testing:** Ensures data is passed correctly between front-end and back-end.
