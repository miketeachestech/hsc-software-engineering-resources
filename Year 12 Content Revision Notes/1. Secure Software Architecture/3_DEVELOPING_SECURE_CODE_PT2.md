# Developing Secure Code Part 2 - HSC Software Engineering Revision Notes

## 1. Strategies for Managing Secure Programming Code
Software developers use various strategies to ensure that programming code remains secure and free from vulnerabilities.

### Code Review
- **Peer review** of code to detect security issues before deployment.
- Helps identify **logic errors, security flaws, and inefficiencies**.
- *Example:* A developer submits a pull request in GitHub, where another team member reviews and suggests improvements before merging.

### Static Application Security Testing (SAST)
- Analyzes source code **without executing it**.
- Detects vulnerabilities like **hardcoded credentials, SQL injection risks, and buffer overflows**.
- *Example:* A SAST tool like SonarQube scans code for insecure functions before it is compiled.

### Dynamic Application Security Testing (DAST)
- Tests a running application for security vulnerabilities.
- Simulates real-world attacks, identifying flaws **during execution**.
- *Example:* A web application is tested for XSS attacks while actively serving users.

### Vulnerability Assessment
- Systematic review of software to identify weaknesses.
- Often involves **automated tools and manual testing**.
- *Example:* Running an automated scan using tools like Nessus to find outdated libraries.

### Penetration Testing
- Ethical hacking to simulate attacks and uncover security gaps.
- Helps prevent **unauthorised access, data breaches, and exploitation**.
- *Example:* A security team hires a penetration tester to attempt breaking into their application.

---

## 2. Defensive Data Input Handling Practices
To prevent malicious input, developers must apply **strict input handling techniques**.

### Input Validation
- Ensures **only expected data formats** are accepted.
- Prevents SQL injection, XSS, and buffer overflow attacks.
- *Example:* A login form checks if the email is in a valid format before sending it to the server.

### Input Sanitisation
- **Cleans user input** to remove harmful characters.
- Helps prevent injection attacks.
- *Example:* A web application removes `<script>` tags from user comments to block XSS exploits.

### Error Handling
- Prevents **leakage of sensitive system information**.
- Uses **generic error messages** instead of exposing system details.
- *Example:* Displaying “Invalid username or password” instead of “User not found” to prevent user enumeration attacks.

---

## 3. Secure API Development
APIs must be designed to **prevent unauthorised access** and **reduce vulnerabilities**.

- **Use authentication and authorisation** (e.g., OAuth, JWT).
- **Validate API inputs** to avoid injection attacks.
- **Rate-limit requests** to prevent denial-of-service attacks.
- *Example:* An API key and OAuth token are required to access a payment gateway securely.

---

## 4. Code Optimisation for Security and Efficiency
Secure code should also be efficient to enhance user experience.

### Memory Management
- Prevents **memory leaks and buffer overflows**.
- Uses **garbage collection** where applicable.
- *Example:* A C++ program frees unused memory with `delete` to prevent memory bloat.

### Session Management
- Ensures user sessions are secure and **expire after inactivity**.
- Uses **secure cookies and tokens**.
- *Example:* A banking website logs users out after 10 minutes of inactivity.

### Exception Management
- Prevents **crashes and error-based attacks**.
- Uses **structured exception handling**.
- *Example:* A Python API wraps file operations in `try-except` to handle unexpected failures gracefully.

---

## 5. Securing User Action Controls
Preventing common security vulnerabilities requires strict access controls.

### Broken Authentication and Session Management
- Ensures **passwords are stored securely using hashing**.
- Uses **MFA and session expiration policies**.
- *Example:* Users must verify identity with an SMS code before accessing sensitive account details.

### Cross-Site Scripting (XSS) and Cross-Site Request Forgery (CSRF)
- **XSS:** Prevents malicious scripts from executing in a user's browser.
- **CSRF:** Prevents unauthorised actions from being performed on behalf of a user.
- *Example:* A banking website uses CSRF tokens to ensure transactions are initiated by a legitimate user.

### Invalid Forwarding and Redirecting
- Prevents **redirect attacks** that send users to malicious sites.
- Uses **allowlists** for permitted redirections.
- *Example:* A login page redirects only to pre-approved domains.

### Race Conditions
- Prevents **exploiting timing issues in code execution**.
- Uses **locking mechanisms** in concurrent programming.
- *Example:* A banking app ensures two users cannot withdraw from the same account at the same time due to transaction locking.

---

## 6. Protecting User Files and Hardware
Secure coding also involves **preventing file-based and hardware-level attacks**.

### File Attacks
- Prevent **path traversal attacks** (e.g., `../../etc/passwd`).
- Use **restricted file permissions**.
- *Example:* A web server blocks user access to sensitive system directories.

### Side Channel Attacks
- Prevents **leaking sensitive information through hardware vulnerabilities**.
- Uses **constant-time cryptographic operations** to avoid timing attacks.
- *Example:* A cryptographic system ensures encryption execution time does not depend on input values.