# **Practice Questions: Data Transmission Using the Web (Part 1)**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the primary function of the **Domain Name System (DNS)**?  
   - A) Encrypting web traffic between clients and servers  
   - B) ➡️ Converting domain names into IP addresses  
   - C) Controlling data transmission speeds  
   - D) Managing firewall security rules  

**2.** *(1 mark)* Which of the following correctly describes **Progressive Web Apps (PWAs)**?  
   - A) They require installation from an app store  
   - B) ➡️ They function like native apps but run in a browser  
   - C) They do not work offline  
   - D) They do not support push notifications  

**3.** *(1 mark)* What is the purpose of **HTTPS** compared to HTTP?  
   - A) It reduces website loading time  
   - B) It compresses website data  
   - C) ➡️ It secures data transmission using encryption  
   - D) It prevents all cyber threats  

---

## **Short Answer Questions**

**4.** *(3 marks)* Describe the three main components of a **data packet** and their functions in internet communication.  
> Header (sender IP address and destination IP address), payload (actual data itself), footer (end of packet, ensures error correction i.e. signature)


**5.** *(3 marks)* Explain the difference between **IPv4 and IPv6**, and why IPv6 is needed.  
- Because IPv4 is limited in range (only a 32 bit addressing system), and IPv6 (128 bit addressing system), IPv6 can cater for the significantly larger amount of devices globally. 


**6.** *(3 marks)* Compare **FTP and SFTP** in terms of security and functionality.  
> FTP (file transfer protocol) is less secure than SFTP (Secure file transfer protocol) as SFTP encrypts data using TLS (transport layer security). Functionally, this means that others do not have access to that data.



---

## **Extended Response Questions**

**7.** *(4 marks)* Discuss the importance of **secure email transmission** and how protocols such as **SMTP, POP3, and IMAP** function to manage email communication.  
- SMTP             is for RECIEVING
- POP3 and IMAP    is for SENDING (imap treats the server as a source of truth, but on pop3 mails only exist on the client)

**8.** *(4 marks)* Explain how **SSL/TLS encryption** protects sensitive data during online transactions and give a real-world example of its use.  
- A man-in-the-middle attack can be prevented as packets are encrypted so a man in the middle 


**9.** *(4 marks)* How do **data transmission protocols (such as TCP/IP, FTP, and DNS)** work together to enable the functioning of the internet? Provide examples.  
- Start with IP and DNS 

