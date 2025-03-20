# **Practice Questions: Data Transmission Using the Web (Part 2)**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the primary function of **SSL/TLS certificates**?  
   - A) Converting IP addresses into domain names  
   - B) ➡️ Encrypting data between a client and a server  
   - C) Speeding up web page loading times  
   - D) Storing password hashes on a server  

**2.** *(1 mark)* How does **asymmetric encryption** differ from symmetric encryption?  
   - A) It uses a single key for encryption and decryption  
   - B) ➡️ It requires both public and private keys for encryption and decryption  
   - C) It does not involve encryption keys  
   - D) It only encrypts file names, not data  

**3.** *(1 mark)* What is the purpose of a **hash function** in secure communication?  
   - A) It compresses data before transmission  
   - B) ➡️ It verifies data integrity by generating a fixed-length output  
   - C) It encrypts user passwords for transmission  
   - D) It speeds up internet browsing by caching web pages  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the difference between **plain text and cipher text**, and why encryption is necessary for secure communication.  
> Plain text is unencrypted text, whereas cipher text takes plain text and encrypts the text, requiring a key to unencryption. Encryption is necessesary to faciliate secure communication to prevent sensitive data from being leaked incase a packet is intercepted during transit.
> - Provide example 


**5.** *(3 marks)* Describe the steps involved in an **encryption handshake** when establishing a secure HTTPS connection.  
> ClientHello sends a list of possible SSL/TLS versions that the client supports. ServerHello responds with a SSL/TLS certificate using the most secure version that both client and server supports. The certificate contains the public key. Client generates a pre-master key, encrypts the pre-master key using the public key, sends it to the server which decrypts the pre-master key using it's private key, and the pre-master key is now a shared-secret to facilitate symmetric encryption. 

**6.** *(3 marks)* What is the role of **digital signatures** in verifying the authenticity of transmitted data?  
> Digital signatures provide a way to ensure that data has not been tampered with during transit. Digital signatures achieves this by creating an hash of data, which is then encrypted asymmetrically. A recipient can generate a hash of transmitted data and compare this with the decrypted hash to verify that the data has not been modified during transit; the data is authentic. An example of this is a digitally signed PDF, in which the signature provides information to a recipient of any modifications have been made to the PDF. 



---

## **Extended Response Questions**

**7.** *(4 marks)* Discuss the impact of **big data on web architecture**, including the role of **data mining, metadata, and streaming service management**.  
> Scale up computing power and storage resources to handle analysis of that data. For example, storing data in a SQL table, however due to the limitations of querying a database of that size, a more powerful alternative is required to handle that amount of data. This means people rely on more scalable and powerful database services.
> - Data mining: analysing customer habits to then recommend them products (analysing data to find patterns, trends, and relationships, to create insights)
> - Metadata: **content, origin, and structure**, in terms of big data, usually it's timestamp, filetypes, and location. For example uploading an image with a geolocation metadata, indicating the user is on a trip, allowing facebook to push more targeted advertising.
> - Steaming services: as streaming is resource intensive, which requires highly optimised content delivery networks (CDNs). CDNs geolocated at optimised locations caches popular content to improve loading times geographically. For example, Netflix caches more popular shows to Australians in their Australia CDN, reducing loads on central servers by scaling on demand and using load-balancers to steer clients to different server. 

**8.** *(4 marks)* Explain how **encryption algorithms** such as AES, RSA, and ECC enhance data security, and provide examples of their real-world applications.  


**9.** *(4 marks)* How does the **TLS encryption handshake process** work, and why is it crucial for securing online transactions?  

