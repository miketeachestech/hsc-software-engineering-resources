# **Answers: Developing Secure Code Part 2**

## **Multiple Choice Questions**

**1.** *(1 mark)*
- Correct Answer: **B) To detect security flaws and inefficiencies before deployment**
- **1 mark** awarded for correctly selecting the answer.

**2.** *(1 mark)*
- Correct Answer: **A) By analyzing source code for vulnerabilities without executing it**
- **1 mark** awarded for correctly selecting the answer.

**3.** *(1 mark)*
- Correct Answer: **B) Performing penetration testing on a live web application**
- **1 mark** awarded for correctly selecting the answer.

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the difference between **vulnerability assessment** and **penetration testing** in software security.
- **1 mark** for defining **vulnerability assessment** as a systematic review to identify software weaknesses.
- **1 mark** for defining **penetration testing** as an ethical hacking approach to exploit vulnerabilities.
- **1 mark** for explaining that penetration testing actively attempts to breach security, whereas vulnerability assessment only identifies weaknesses.

**5.** *(3 marks)* Describe how **input validation, sanitization, and error handling** work together to prevent security threats.
- **1 mark** for defining **input validation** as checking if input data matches expected formats.
- **1 mark** for defining **sanitization** as cleaning or filtering input to remove harmful content.
- **1 mark** for explaining that **error handling** ensures sensitive system details are not exposed in error messages.

**6.** *(3 marks)* What are the key principles of **secure API development**, and how do they protect software systems?
- **1 mark** for requiring **authentication and authorization** (e.g., OAuth, JWT) to control API access.
- **1 mark** for implementing **input validation** to prevent injection attacks.
- **1 mark** for enforcing **rate limiting** to protect against denial-of-service (DoS) attacks.

---

## **Extended Response Questions**

**7.** *(4 marks)* Discuss how **memory management, session management, and exception management** contribute to software security. Provide examples.
- **1 mark** for explaining **memory management** (prevents memory leaks and buffer overflows, e.g., garbage collection in Java).
- **1 mark** for explaining **session management** (ensures secure session expiration, e.g., auto-logout after inactivity).
- **1 mark** for explaining **exception management** (prevents system crashes and error-based attacks, e.g., structured exception handling in Python).
- **1 mark** for providing a relevant example linking all three concepts.

**8.** *(4 marks)* Explain how **broken authentication, cross-site scripting (XSS), and cross-site request forgery (CSRF)** affect web application security. How can these vulnerabilities be mitigated?
- **1 mark** for defining **broken authentication** (e.g., weak password storage, lack of MFA).
- **1 mark** for explaining **XSS** (injecting malicious scripts into web pages).
- **1 mark** for explaining **CSRF** (tricking a user into performing unintended actions).
- **1 mark** for mitigation strategies (e.g., secure password hashing, content security policy for XSS, CSRF tokens for request validation).

**9.** *(4 marks)* What are **file attacks and side channel attacks**, and how can they be prevented in secure software development?
- **1 mark** for defining **file attacks** (e.g., path traversal, improper file permissions).
- **1 mark** for defining **side channel attacks** (e.g., timing attacks, power analysis in cryptographic systems).
- **1 mark** for explaining how **file attacks** can be mitigated (e.g., restricting file permissions, validating file paths).
- **1 mark** for explaining how **side channel attacks** can be mitigated (e.g., using constant-time cryptographic operations, hardware-level protections).

