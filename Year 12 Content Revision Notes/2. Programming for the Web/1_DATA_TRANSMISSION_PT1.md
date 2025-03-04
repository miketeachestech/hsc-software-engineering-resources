# Data Transmission Using the Web Part 1 - HSC Software Engineering Revision Notes

## 1. Applications of Web Programming
Web programming allows developers to create a wide range of online applications that facilitate user interaction, transactions, and accessibility.

### Interactive Websites and Webpages
- Websites that **dynamically update content** and respond to user actions.
- Commonly built with **HTML, CSS, JavaScript, and front-end frameworks** like React or Vue.js.
- *Example:* A social media platform updates posts in real-time without needing to refresh the page.

### E-commerce
- Online platforms that enable **buying and selling of goods/services**.
- Require **secure payment processing, shopping carts, and user authentication**.
- *Example:* Amazon and eBay allow customers to purchase items using encrypted transactions.

### Progressive Web Apps (PWAs)
- Web applications that **function like native mobile/desktop apps**.
- Offer **offline access, push notifications, and responsive design**.
- *Example:* Twitter Lite is a PWA that runs efficiently on mobile browsers with app-like functionality.

---

## 2. How Data is Transferred on the Internet
The internet operates by **transmitting data in packets** using **specific addressing and routing mechanisms**.

### Data Packets
- Information sent across the internet is broken into **small units (packets)** for transmission.
- Each packet contains:
  - **Header:** Includes source/destination IP addresses and other control information.
  - **Payload:** The actual data being transmitted.
  - **Footer:** Signals the end of the packet.
- *Example:* When loading a webpage, packets containing HTML, CSS, and JavaScript files are sent from the server to the client.

### Internet Protocol (IP) Addresses
- **Unique numerical identifiers** assigned to devices for network communication.
- Two main versions:
  - **IPv4:** 32-bit addresses (e.g., `192.168.1.1`).
  - **IPv6:** 128-bit addresses (e.g., `2001:db8::ff00:42:8329`) for expanded internet capacity.
- *Example:* A laptop connecting to a website uses its IP address to request data from the server’s IP.

### Domain Name System (DNS)
- **Translates human-readable domain names** (e.g., `google.com`) into **IP addresses**.
- Acts as an **address book of the internet**, mapping domain names to their respective servers.
- *Example:* When a user types `facebook.com`, the DNS finds the corresponding IP and directs the browser to Facebook’s servers.

---

## 3. Web Protocols and Their Functions
Various protocols facilitate communication between devices and servers over the internet.

### What Are Ports and Why Are They Needed?
- **Ports** are numerical identifiers used by protocols to determine where network traffic should be directed within a system.
- Each service on a device (e.g., a web browser, email client, or FTP program) communicates through a specific port.
- Ports ensure that multiple network applications can function simultaneously without interfering with one another.
- *Example:* A device can browse the web while receiving emails because web traffic uses port **443 (HTTPS)**, while email uses port **993 (IMAP)**.

### HTTP & HTTPS (Hypertext Transfer Protocol / Secure)
- **HTTP (port 80):** Transfers web data in plaintext.
- **HTTPS (port 443):** Uses SSL/TLS encryption for secure communication.
- *Example:* A bank website uses HTTPS to protect login credentials from hackers.

### TCP/IP (Transmission Control Protocol / Internet Protocol)
- **TCP:** Ensures **reliable, ordered data transmission** by breaking data into packets and reassembling them.
- **IP:** Handles **addressing and routing** of packets between devices.
- *Example:* TCP ensures an email arrives intact, even if some packets take different routes.

### DNS (Domain Name System)
- Resolves **domain names into IP addresses**.
- Uses port **53** to query name servers.
- *Example:* When visiting `netflix.com`, DNS servers find the corresponding IP address and return it to the browser.

### FTP & SFTP (File Transfer Protocol / Secure File Transfer Protocol)
- **FTP (port 21):** Transfers files between clients and servers but lacks security.
- **SFTP (port 22):** Uses SSH encryption for secure file transfers.
- *Example:* A web developer uploads a website’s files using SFTP to ensure secure transmission.

### SSL & TLS (Secure Sockets Layer / Transport Layer Security)
- **SSL (deprecated) & TLS:** Encrypts data to secure communications between clients and servers.
- Commonly used for **secure login forms, payment gateways, and email encryption**.
- *Example:* Online banking websites use TLS encryption to protect financial transactions.

### SMTP, POP3, & IMAP (Email Protocols)
- **SMTP (port 25, or 587 for encryption):** Sends outgoing emails.
- **POP3 (port 110):** Downloads emails from a server to a local device and then removes the emails from the server. This is an older way of doing things; it made more sense when server space was more expensive and households usually only had one computer.
- **IMAP (port 143, or 993 for encryption):** Keeps emails stored on the server while syncing multiple devices.
- *Example:* Gmail uses IMAP to allow users to access their email from multiple devices while keeping messages on the server.