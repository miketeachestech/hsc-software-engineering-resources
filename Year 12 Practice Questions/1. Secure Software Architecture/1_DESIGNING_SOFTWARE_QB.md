# **Practice Questions: Designing Software**

## **Multiple Choice Questions**

**1.** *(1 mark)* Which of the following is *not* a key benefit of developing secure software?  
   - A) Ensures the confidentiality, integrity, and availability of data  
   - B) Increases the performance of the software  
   - C) Prevents unauthorized access and data breaches  
   - D) Helps maintain user trust and regulatory compliance  

<details>
  <summary>✅ **Answer (1 mark)**</summary>
  **1 mark** – Correctly selects **B) Increases the performance of the software**  
</details>

---

**2.** *(1 mark)* What is the primary purpose of the "Least Privilege Principle" in software security?  
   - A) To restrict software updates to authorized users only  
   - B) To ensure that users only have access to the data and features necessary for their role  
   - C) To improve system performance by limiting concurrent users  
   - D) To enhance encryption methods in secure databases  

<details>
  <summary>✅ **Answer (1 mark)**</summary>
  **1 mark** – Correctly selects **B) To ensure that users only have access to the data and features necessary for their role**  
</details>

---

**3.** *(1 mark)* Which of the following security threats involves injecting malicious scripts into web pages?  
   - A) SQL Injection  
   - B) Denial-of-Service (DoS) Attacks  
   - C) Cross-Site Scripting (XSS)  
   - D) Phishing  

<details>
  <summary>✅ **Answer (1 mark)**</summary>
  **1 mark** – Correctly selects **C) Cross-Site Scripting (XSS)**  
</details>

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain how secure coding practices help prevent SQL injection attacks.  

<details>
  <summary>✅ **Answer (3 marks)**</summary>
  **3 marks** – Detailed and correct explanation covering:
  - **1 mark** – Use of **prepared statements and parameterized queries** to prevent user inputs from being executed as SQL commands.
  - **1 mark** – Importance of **input validation and sanitization** to remove malicious inputs.
  - **1 mark** – Explanation of how these practices reduce the risk of unauthorized database manipulation.  
</details>

---

**5.** *(3 marks)* What is the purpose of **Static Application Security Testing (SAST)** and how does it differ from **Dynamic Application Security Testing (DAST)?**  

<details>
  <summary>✅ **Answer (3 marks)**</summary>
  **3 marks** – Comprehensive comparison covering:
  - **1 mark** – Defines **SAST** as analyzing the source code before execution.
  - **1 mark** – Defines **DAST** as testing the software while it is running.
  - **1 mark** – Correctly identifies the **key difference**: SAST works at the code level, whereas DAST evaluates security in real-time.  
</details>

---

**6.** *(2 marks)* Describe two ways **input validation** can improve software security.  

<details>
  <summary>✅ **Answer (2 marks)**</summary>
  **2 marks** – Each valid reason earns **1 mark**:
  - **1 mark** – Prevents **injection attacks** by restricting user inputs to predefined formats.
  - **1 mark** – Avoids **unexpected system behavior** by ensuring only expected input data is processed.  
</details>

---

## **Extended Response Questions**

**7.** *(4 marks)* The software development lifecycle (SDLC) includes multiple phases. Discuss how security considerations are integrated into each of the following stages:  
   - **Design**  
   - **Development**  
   - **Testing**  
   - **Maintenance**  

<details>
  <summary>✅ **Answer (4 marks)**</summary>
  **4 marks** – Breakdown of security considerations across SDLC stages:
  - **1 mark** – **Design**: Implementing **threat modeling, input validation planning, and least privilege principle**.
  - **1 mark** – **Development**: Use of **secure coding practices, version control (Git), encryption, and modularization**.
  - **1 mark** – **Testing**: Conducting **penetration testing, SAST, DAST, and unit testing**.
  - **1 mark** – **Maintenance**: Regular **security patches, system monitoring, and authentication updates**.  
</details>

---

**8.** *(4 marks)* Explain how **user awareness and security practices** influence software security. Provide examples of how software developers can improve security for users with different levels of technical knowledge.  

<details>
  <summary>✅ **Answer (4 marks)**</summary>
  **4 marks** – Explanation covering:
  - **1 mark** – How **non-technical users** may require enforced **strong password policies, MFA, and automatic updates** to ensure security.
  - **1 mark** – How **advanced users** may prefer **customizable security settings and role-based access control (RBAC)**.
  - **1 mark** – Example of a **banking app** using **biometric authentication (fingerprint, face ID) for ease of use while maintaining MFA for critical actions**.
  - **1 mark** – How software can balance usability and security by providing **clear security prompts, phishing warnings, and access control measures**.  
</details>