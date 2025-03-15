# **Practice Questions: Developing Secure Code**

## **Multiple Choice Questions**

**1.** *(1 mark)* Which of the following is a fundamental principle of confidentiality in secure software design?  
   - A) Ensuring that data is available at all times  
   - B) ➡️ Protecting sensitive information from unauthorized access  
   - C) Preventing modification of data by unauthorized users  
   - D) Tracing user activities in a system  

**2.** *(1 mark)* What is the primary role of authentication in secure software?  
   - A) Controlling what actions users can perform  
   - B) ➡️ Confirming the identity of users and systems  
   - C) Encrypting data before storage  
   - D) Preventing system failures  

**3.** *(1 mark)* Which of the following best describes sandboxing?  
   - A) Encrypting user data before transmission  
   - B) ➡️ Restricting applications from accessing system resources beyond their scope  
   - C) Detecting unauthorized access to the network  
   - D) Storing hashed passwords for authentication  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the differences between confidentiality, integrity, and availability in software security.  


**5.** *(3 marks)* Describe how encryption and hashing differ in securing data.  
> Encryption refers to making data unreadable unless a key is provided. Only allowing authorised people with the key ensures that the data is only readable to authorised people. Hashing refers to the process of creating an irreversable, fixed length digest of given data. Encyption is a two way process, meaning it is reversible, ensuring it's confidentiality, whereas hashing is a one way process, making it irreversible, and ensuring it's integrity.



**6.** *(2 marks)* Give two examples of how role-based access control (RBAC) is used in secure systems.  
> In some organisations, users are not able to change their account passwords without elevated access that can only be granted by an IT administrator. In file sharing platforms, like Google Drive (when set up), contributors could add files, but only managers are able to write or delete files.

---

## **Extended Response Questions**

**7.** *(4 marks)* Discuss how cryptography is used in software security. Provide real-world examples.  
- Encyption, used to encypt data at transit (i.e. TLS certificates), ensuring it's confidentiality 
- Hashing, used in ways such as stamping data to check for changes (digital signature) or being able to check data without knowing the original value (i.e. password hashing), ensuring it's integrity.


**8.** *(4 marks)* Explain the concept of privacy by design and how it improves user data protection.  
- Principle of least privilage (dont collect data that you dont need)











