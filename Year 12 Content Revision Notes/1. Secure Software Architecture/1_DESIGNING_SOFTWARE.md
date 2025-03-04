# Designing Software - HSC Software Engineering Revision Notes

## 1. Benefits of Developing Secure Software
Developing secure software is essential to protect users, data, and systems from cyber threats. Secure coding practices help prevent vulnerabilities that could be exploited by attackers. Key benefits include:

### Data Protection
- Ensures the **confidentiality, integrity, and availability (CIA)** of data.
- Prevents **unauthorized access, data breaches, and identity theft**.
- Protects sensitive information like **personal data, financial records, and business secrets**.

### Minimising Cyber Attacks and Vulnerabilities
- Reduces the risk of common attacks such as:
  - **SQL Injection** – Malicious SQL queries that manipulate databases.
  - **Cross-Site Scripting (XSS)** – Injecting harmful scripts into web pages.
  - **Denial-of-Service (DoS) Attacks** – Overloading a system to make it unusable.
- Helps maintain **user trust** and **regulatory compliance** (e.g., GDPR, Australian Privacy Act).

---

## 2. Fundamental Software Development Steps for Secure Code
The software development process consists of several key steps that help ensure the security and functionality of a program.

### 1. Requirements Definition
- Identify **functional and non-functional** requirements of the software.
- Define security requirements such as:
  - **Access control policies**
  - **Data encryption needs**
  - **Authentication methods**
  - **Regulatory compliance** (e.g., GDPR, ISO 27001)

### 2. Determining Specifications
- Define technical details such as:
  - **User roles and permissions**
  - **Security constraints**
  - **Performance and reliability expectations**
- Use **formal documentation** such as:
  - **Software Requirement Specification (SRS)**
  - **User Stories (Agile)**
  - **Use Case Diagrams (UML)**

### 3. Design
- Plan how the software will be structured using:
  - **Unified Modeling Language (UML) diagrams**, such as:
    - **Class Diagrams** – Define object-oriented structures.
    - **Data Flow Diagrams (DFD)** – Show how data moves within the system.
    - **Entity-Relationship Diagrams (ERD)** – Represent database relationships.
- Security considerations in design:
  - **Least Privilege Principle** – Users only get access to what they need.
  - **Input Validation** – Prevents injection attacks.
  - **Threat Modelling** – Identifies potential vulnerabilities.

### 4. Development
- Implement code using **secure coding practices**:
  - **Input validation** to prevent malicious inputs.
  - **Error handling** to avoid exposing sensitive system details.
  - **Code modularization** to enhance maintainability and security.
- Use **version control systems (e.g., Git)** to track changes.

### 5. Integration
- Combine different software modules while ensuring:
  - **Secure data transfer** between components.
  - **Authentication and authorization** between services.
  - **Proper API security** (e.g., OAuth, JWT for authentication).

### 6. Testing and Debugging
- Security testing includes:
  - **Static Application Security Testing (SAST)** – Analyzing code for vulnerabilities.
  - **Dynamic Application Security Testing (DAST)** – Testing the running application.
  - **Penetration Testing** – Simulating cyber attacks.
  - **Unit Testing & Integration Testing** – Ensuring individual and combined components work securely.

### 7. Installation
- Ensure **secure deployment** by:
  - Setting up **proper file permissions**.
  - Enabling **firewalls and intrusion detection**.
  - Using **secure configuration settings** (e.g., disabling default credentials).

### 8. Maintenance
- Regular updates to:
  - **Patch security vulnerabilities**.
  - **Improve performance and stability**.
  - **Ensure compatibility with new technologies**.
- Implement **logging and monitoring** to detect and respond to threats.

---

## Summary Table

| **Stage**         | **Key Activities** |
|-------------------|-------------------|
| **Requirements**  | Define security needs, user roles, compliance requirements. |
| **Specifications**| Create use case diagrams, define access control policies. |
| **Design**       | Develop UML diagrams, threat models, encryption plans. |
| **Development**  | Write secure code, use version control (Git), validate input. |
| **Integration**  | Secure data transfer, implement API security. |
| **Testing**      | Perform security audits, penetration testing, debugging. |
| **Installation** | Secure configuration, firewall setup, enforce permissions. |
| **Maintenance**  | Apply patches, monitor system logs, update security policies. |

---

## 3. How End-User Capabilities Influence Secure Design
The **experience and knowledge of users** affect how security is implemented in software. Developers must balance usability and security to prevent mistakes while keeping the software user-friendly.

### User Awareness and Security Practices
- Users with **low technical knowledge**:
  - May need **automatic security features** (e.g., auto-updates, enforced strong passwords).
  - Require **simple and clear security messages**.
- Advanced users:
  - Prefer **customizable security settings**.
  - May need **role-based access control (RBAC)** to configure permissions.

### Usability vs Security Balance
- **Too much security can make software frustrating to use.**
- **Too little security increases risk.**
- Example:  
  - A banking app should use **multi-factor authentication (MFA)** for extra security but also provide **biometric authentication** (fingerprint, face recognition) for ease of use.

### Common User Mistakes and Risk Factors
- **Weak passwords** → Implement password managers and enforce complexity rules.
- **Phishing attacks** → Use email verification and anti-phishing filters. Run phishing campaigns to raise awareness within the organisation. 
- **Sharing credentials** → Implement **single sign-on (SSO)** and **role-based access control**.