# Data Transmission Using the Web Part 2 - HSC Software Engineering Revision Notes

## 1. Processes for Securing the Web
Securing web communications ensures data remains **confidential, authentic, and protected** from interception or tampering. Various cryptographic methods and security mechanisms are used to achieve this.

### Secure Sockets Layer (SSL) Certificates
- **SSL/TLS certificates** encrypt data transmitted between a client (browser) and a server, preventing eavesdropping.
- Websites with **HTTPS** use SSL/TLS to ensure **secure transactions**.
- *Example:* A user logging into an online banking website with an HTTPS connection ensures their credentials are protected from attackers.

### Encryption Algorithms
- Convert **plain text (readable data)** into **cipher text (unreadable scrambled data)** to protect it from unauthorised access.
- Common encryption algorithms:
  - **AES (Advanced Encryption Standard)** – Used for securing sensitive information.
  - **RSA (Rivest-Shamir-Adleman)** – Commonly used for encrypting communication over the web.
  - **ECC (Elliptic Curve Cryptography)** – Provides high security with smaller key sizes.
- *Example:* A messaging app encrypts text messages using **AES-256**, ensuring only the intended recipient can decrypt and read them.

### Encryption Keys
- Encryption relies on **keys** that determine how data is scrambled and unscrambled.
- Types of encryption:
  - **Symmetric encryption:** Uses the **same key** for encryption and decryption (e.g., AES).
  - **Asymmetric encryption:** Uses a **public key** for encryption and a **private key** for decryption (e.g., RSA).
- *Example:* An e-commerce site encrypts customer credit card details using an RSA public key; only the business's private key can decrypt it.

### Plain Text and Cipher Text
- **Plain text:** Unencrypted data that anyone can read.
- **Cipher text:** Encrypted data that appears scrambled.
- **Simple Example – Caesar Cipher:**
  - A **Caesar cipher** is a basic encryption method where each letter is shifted by a fixed number of places in the alphabet.
  - Example: With a shift of **3**, `HELLO` becomes `KHOOR`.
  - While simple, this method is **easily breakable**.
- **Real-World Example – AES Encryption:**
  - Before encryption: `password123`
  - After encryption with AES-256: `F5A1B6C9D8E2…`
  - Unlike the Caesar cipher, AES is **highly secure** and widely used.

### Authentication and Authorisation
- **Authentication** verifies a user's identity (e.g., entering a username and password).
- **Authorisation** determines what a user is allowed to do (e.g., an admin can access all settings, but a regular user cannot).
- *Example:* A user logs into their email (authentication), but only an admin can reset passwords for all users (authorisation).

### Hash Values
- A **hash function** converts data into a fixed-length string that represents the original data.
- Hashes are **irreversible** and used to securely store passwords.
- Common hash functions:
  - **SHA-256** – Used for password hashing.
  - **MD5** (obsolete) – Previously used for file verification but now insecure.
- *Example:* A password `mypassword` hashed with SHA-256 becomes `5e88489f...`, preventing attackers from recovering the original password.

### Digital Signatures
- Ensure **data integrity and authenticity** by verifying that a message or document has not been altered.
- Generated using **asymmetric encryption**.
- *Example:* When downloading software, a digital signature ensures it was not tampered with before installation.

### How an Encryption Handshake Works
An encryption handshake is a **process used to establish a secure connection** between a client and a server. This is crucial for HTTPS websites and other secure online communications.

1. **Client Hello:**
   - The client (e.g., a web browser) sends a request to the server, listing supported encryption algorithms (cipher suites).

2. **Server Hello:**
   - The server selects the strongest available encryption method and sends back its **SSL/TLS certificate**, which contains its **public key**.

3. **Key Exchange:**
   - The client verifies the server's certificate using a trusted certificate authority (CA).
   - The client and server generate a **shared secret key** using asymmetric encryption (e.g., RSA or Diffie-Hellman key exchange).

4. **Session Key Established:**
   - From this point onward, all communication is **encrypted using symmetric encryption** (e.g., AES), which is faster and more efficient.

5. **Secure Communication Begins:**
   - The encrypted session allows safe transmission of sensitive data, such as passwords or credit card details.
   
*Example:* When you log into your online banking account, an encryption handshake ensures that your login details are securely transmitted over HTTPS.

---

## 2. The Effect of Big Data on Web Architecture
Big data has transformed web architecture by introducing **massive datasets, real-time processing, and advanced analytics**. Businesses and technology providers must adapt their infrastructure to handle large-scale data efficiently.

### Data Mining
- The process of **analyzing large datasets** to find patterns, trends, and relationships.
- Used in **advertising, fraud detection, and recommendation systems**.
- *Example:* E-commerce sites like Amazon analyze purchase history to recommend products.
- *Security Implications:* Hackers can use data mining to identify security vulnerabilities or predict user behavior for phishing attacks.

### Metadata
- **Data about data**, describing its content, origin, and structure.
- Includes information like **timestamps, geolocation, and file properties**.
- *Example:* A photo taken on a smartphone has metadata storing the date, time, and location.
- *Privacy Concern:* Websites and companies collect metadata to track users, often without their explicit consent.

### Streaming Service Management
- Platforms like **Netflix, YouTube, and Spotify** handle enormous amounts of **real-time data** to deliver seamless experiences.
- Uses **CDNs (Content Delivery Networks)** to distribute content efficiently.
- Requires **load balancing** to handle millions of concurrent users.
- *Example:* Netflix optimises video quality based on a user's internet speed using adaptive streaming.
- *Security Concerns:* Cyberattacks like **DDoS (Distributed Denial of Service)** can target streaming services, overwhelming servers with traffic and causing service outages.