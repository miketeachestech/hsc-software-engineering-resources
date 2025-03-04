# Designing Web Applications Part 1 - HSC Software Engineering Revision Notes

## 1. The Role of the World Wide Web Consortium (W3C) in Web Development
The **World Wide Web Consortium (W3C)** is an international organisation that develops standards to ensure that the web remains **accessible, secure, and compatible** across devices and platforms.

### Web Accessibility Initiative (WAI)
- Aims to make the web usable for people with **disabilities**.
- Provides **guidelines** such as the **Web Content Accessibility Guidelines (WCAG)** to help developers create accessible web applications.
- Accessibility features include:
  - **Keyboard navigation** (ensuring users can navigate without a mouse).
  - **Alt text for images** (providing descriptions for screen readers).
  - **ARIA roles** (improving accessibility for interactive elements).
- *Example:* Adding `alt` attributes to images for screen readers:
  ```html
  <img src="logo.png" alt="Company Logo">
  ```

### Internationalisation
- Ensures that web applications work **across multiple languages and cultural contexts**.
- Covers **right-to-left (RTL) text support**, local date/time formats, and currency symbols.
- *Example:* Setting language attributes in HTML:
  ```html
  <html lang="fr"> <!-- This sets the language to French -->
  ```

### Web Security
- Defines standards for **secure web communication and authentication**.
- Enforces best practices for **data encryption, user authentication, and protection against vulnerabilities**.
- *Example:* W3C supports **Content Security Policy (CSP)** to prevent cross-site scripting (XSS) attacks:
  ```html
  <meta http-equiv="Content-Security-Policy" content="default-src 'self'">
  ```

### Privacy
- Establishes protocols to **protect user data and prevent tracking without consent**.
- Encourages transparency in **data collection, cookie usage, and user tracking**.
- *Example:* Using a privacy-friendly cookie notice:
  ```html
  <script>
    if (!localStorage.getItem('cookieConsent')) {
      alert('This site uses cookies for better user experience.');
      localStorage.setItem('cookieConsent', true);
    }
  </script>
  ```

### Machine-Readable Data
- Promotes **semantic web technologies** that allow machines to understand and process data efficiently.
- Includes **RDF (Resource Description Framework)** and **JSON-LD (JavaScript Object Notation for Linked Data)**.
- *Example:* Using JSON-LD for structured data:
  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "Example Company",
    "url": "https://example.com"
  }
  </script>
  ```

---

## 2. Elements of a Web Development System
A web application consists of **three main components**: client-side programming, server-side programming, and database management.

### Client-Side (Front-End) Web Programming
- The part of a web application that runs in the user’s **browser**.
- Uses **HTML (structure), CSS (styling), and JavaScript (functionality)**.
- Often incorporates **frameworks** like React, Vue.js, or Angular.
- *Example:* A simple form validation in JavaScript:
  ```html
  <form onsubmit="return validateForm()">
    <input type="text" id="name" required>
    <button type="submit">Submit</button>
  </form>
  <script>
    function validateForm() {
      let name = document.getElementById("name").value;
      if (name === "") {
        alert("Name cannot be empty");
        return false;
      }
      return true;
    }
  </script>
  ```

### Server-Side (Back-End) Web Programming
- The part of the application that runs on a **server** and processes user requests.
- Uses programming languages like **Python (Flask, Django), JavaScript (Node.js), PHP, Ruby, or Java (Spring Boot)**.
- Handles **business logic, authentication, and communication with databases**.
- *Example:* A simple Flask route:
  ```python
  from flask import Flask, render_template
  
  app = Flask(__name__)
  
  @app.route('/')
  def home():
      return render_template('index.html')
  
  if __name__ == '__main__':
      app.run(debug=True)
  ```

### Interfacing with Databases
- Databases store and manage **user data, content, and application settings**.
- **SQL Databases** (e.g., MySQL, PostgreSQL): Structured storage using tables and relationships.
- **NoSQL Databases** (e.g., MongoDB, Firebase): Flexible storage for unstructured data.
- *Example:* Fetching records in Flask with SQLite3:
  ```python
  import sqlite3
  
  def get_users():
      connection = sqlite3.connect('database.db')
      cursor = connection.cursor()
      cursor.execute("SELECT * FROM users")
      users = cursor.fetchall()
      connection.close()
      return users
  
  users = get_users()
  for user in users:
      print(user)
  ```

---

## 3. The Influence of Web Browsers on Web Development
Web browsers play a critical role in how web applications function and render. Different browsers may interpret code differently, leading to **compatibility challenges**.

### Browser Rendering and Compatibility
- Each browser uses a **different rendering engine**:
  - **Google Chrome:** Blink
  - **Mozilla Firefox:** Gecko
  - **Apple Safari:** WebKit
  - **Microsoft Edge:** Blink (previously EdgeHTML)
- Developers must ensure their websites **work consistently across all browsers**.

### Developer (Dev) Tools
- Web browsers provide built-in **developer tools** to inspect and debug websites.
- Features include:
  - **Inspecting HTML and CSS** (Elements tab)
  - **Monitoring network requests** (Network tab)
  - **Debugging JavaScript errors** (Console tab)

---

## 4. Cascading Style Sheets (CSS) and Its Impact on Web Applications
CSS controls the **visual design and layout** of web applications, ensuring a consistent and responsive user experience.

### Consistency of Appearance
- CSS ensures a **uniform design** across all web pages.
- Styles can be reused with **external stylesheets**, reducing redundancy.

### Flexibility with Browsers and Display Devices
- CSS enables **responsive design**, making websites adaptable to different screen sizes.
- Uses **media queries** to adjust layouts dynamically.

### CSS Maintenance Tools
- **Preprocessors** (e.g., SASS, LESS) allow for **variables, nesting, and mixins** to simplify CSS management.
- **CSS frameworks** (e.g., Bootstrap, Tailwind CSS) provide **pre-designed components** for faster development.