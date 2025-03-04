# Developing Secure Code Part 1 - HSC Software Engineering Revision Notes

## 1. Fundamental Software Design Security Concepts
Developing secure software requires an understanding of key security principles to protect data, systems, and users from threats. The core principles include:

### Confidentiality
- Ensures that sensitive data is **only accessible to authorised users**.
- Protects personal information, financial records, and business secrets.
- Implemented through **encryption, access controls, and secure authentication**.
- *Example:* A banking app encrypts customer transactions so that only the intended recipient can decrypt and view the details.

### Integrity
- Guarantees that **data remains accurate and unaltered** unless modified by an authorised user.
- Prevents unauthorised tampering, modification, or corruption of data.
- Common techniques include **checksums, hashing, and digital signatures**.
- *Example:* A hash (e.g. SHA-256) is a one-way operation (used to encrypt, can't be decrypted) unlike a cipher (e.g. Caesar Cipher) which is a two-way operation (can be encrypted and decrypted). A password stored using hashing looks like `5e88489...` instead of plain text, ensuring it cannot be easily reversed.

### Availability
- Ensures that software and data are **accessible when needed**.
- Protects against **denial-of-service (DoS) attacks, system failures, and data loss**.
- Implemented through **redundancy, backups, and load balancing**.
- *Example:* A cloud service provider uses multiple data centres to keep services running even if one fails.

### Authentication
- Confirms the **identity of users and systems**.
- Includes **passwords, multi-factor authentication (MFA), and biometric authentication**.
- Ensures that only legitimate users can access sensitive data.
- *Example:* A mobile app requiring fingerprint authentication before accessing user data.

### Authorisation
- Controls what actions users are allowed to perform based on their roles.
- Uses **role-based access control (RBAC) and least privilege principles**.
- Prevents users from accessing data and functions they do not need.
- *Example:* A student at a school is able to login to a web platform to access their assignments, homework, and post questions. However, they are not able to see the solutions to the homework or take administrative actions like enrolling/unenrolling other students because they do not have the teacher role assigned to them.

### Accountability
- Ensures that **actions within a system can be traced back to a responsible party**.
- Implemented through **audit logs, tracking changes, and forensic analysis**.
- Helps with **investigating security incidents and enforcing policies**.
- *Example:* A security log records login attempts, showing timestamps and user IDs.

---

## 2. Applying Security Features in Software
Secure software incorporates built-in security features to protect data, users, and systems.

### Data Protection
- **Encryption** ensures data is unreadable without the correct decryption key.
- **Hashing** secures stored passwords and sensitive data.
- *Example:* User passwords stored as hashed values instead of plaintext prevent attackers from reading them even if the database is compromised.
- **Data masking and tokenisation** protect confidential information in databases.

### Security Measures
- Implement **firewalls, intrusion detection systems (IDS), and secure APIs**.
- Enforce **secure coding practices** (e.g., input validation, secure error handling).
- Regularly update and patch software to remove vulnerabilities.
- *Example:* A web application filtering out special characters to prevent SQL injection attacks.

### Privacy
- Use **anonymisation and pseudonymisation** to protect personal information.
- Ensure **data minimisation**, only collecting and storing necessary user data.
- *Example:* A healthcare system replacing patient names with unique IDs when storing research data.

### Regulatory Compliance
- Adhere to laws and standards such as:
  - **Australian Privacy Act**
  - **General Data Protection Regulation (GDPR)**
  - **ISO/IEC 27001** security standards
- Implement **data breach response plans** and user consent management.
- *Example:* A company must notify users within 72 hours of a data breach under GDPR.

---

## 3. Cryptography and Sandboxing in Security by Design
A **Security by Design** approach integrates security features from the beginning of software development.

### Cryptography
- Protects sensitive data using **encryption algorithms** (e.g., AES, RSA).
- Ensures **data integrity and authenticity** with **digital signatures and certificates**.
- Securely **transmits data over networks** using **TLS and SSL protocols**.
- *Example:* HTTPS encrypts web traffic between a browser and a server to prevent interception.

### Sandboxing
- **Restricts applications from accessing system resources** beyond their scope.
- Prevents **malware from affecting the rest of the system**.
- Used in **web browsers, mobile apps, and virtual environments**.
- *Example:* A PDF reader opening untrusted files in a sandboxed environment to prevent malware execution.

---

## 4. Privacy by Design
Privacy by Design ensures that privacy measures are **proactively built into software**.

### Proactive, Not Reactive
- **Prevents privacy risks from the start** rather than fixing issues later.
- *Example:* Secure authentication is implemented before software deployment.

### Embed Privacy into Design
- **Privacy should be a default setting** (e.g., opt-in data sharing, secure defaults).
- Ensure **data encryption, anonymisation, and strong access controls** are standard.
- *Example:* A social media platform masking personal data from public view by default.

### Respect for User Privacy
- Allow **users control over their data** (e.g., account deletion, data access requests).
- Ensure **clear, transparent policies** on data collection and usage.
- *Example:* A website allowing users to download and delete their data easily.

---

## 5. Testing and Evaluating Software Security
Security testing is essential to ensure software is resilient against cyber threats.

### Determining Vulnerabilities
- Use **automated vulnerability scanning tools**.
- Perform **manual code reviews** to detect weak points.
- *Example:* A penetration tester exploiting a misconfigured API to gain unauthorised access.

### Hardening Systems
- Configure **secure system settings** (e.g., disable unused features, enforce strong passwords).
- Apply **patches and updates** to address security flaws.
- *Example:* A server administrator disabling unused ports to reduce attack surface.

### Handling Security Breaches
- Implement **incident response plans**.
- Conduct **forensic analysis** to determine the source of attacks.
- Notify affected users and authorities where required by law.
- *Example:* A company issuing a security patch after a ransomware attack encrypts user files.

### Business Continuity and Disaster Recovery
- Maintain **regular backups** to restore lost data.
- Implement **failover mechanisms** to ensure system availability.
- Test **disaster recovery plans** to minimise downtime during incidents.
- *Example:* An e-commerce platform switching to a backup server when the primary one fails.