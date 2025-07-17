### Question 1 (1 mark)  
**Correct answer:** Restricting direct access to an object’s data and only allowing changes through methods  
**Justification:**  
Encapsulation is a key idea in object-oriented programming. It means keeping an object's internal data private and only allowing access through specific methods. This helps prevent accidental changes and makes code easier to maintain.

---

### Question 2 (1 mark)  
**Correct answer:** To transfer files over a network using port 21
**Justification:**  
FTP stands for File Transfer Protocol and is used to transfer files between a client and a server over a network. It typically uses port 21 for command and control communication. This protocol is not encrypted by default, but it’s been widely used for moving files like website updates or large data sets.

---

### Question 3 (1 mark)  

| Example Value | Data Type |
|---------------|-----------|
| `true`        | Boolean   |
| `"Australia"` | String    |
| `47.8`        | Float     |
| `2001`        | Integer   |

**Justification:**  
- `true` is a Boolean because it's a true/false value  
- `"Australia"` is a String because it's a group of characters in quotes  
- `47.8` is a Float since it's a decimal number  
- `2001` is an Integer because it's a whole number without a decimal

---

### Question 4 (1 mark)  
**Correct answer:** Using prepared statements with parameterised queries  
**Justification:**  
Prepared statements help protect against SQL injection by separating the user input from the SQL code. This makes it much harder for attackers to inject harmful commands into the database.

---

### Question 5 (1 mark)  
**Correct answers:**  
- To check the program runs without errors  
- To verify the program meets user requirements  
- To identify logic and runtime errors  

**Justification:**  
Software testing is done to make sure the program works as expected. It checks for bugs or mistakes in the logic, and confirms that the software does what the user actually needs.

---

### Question 6 (1 mark)  
**Correct answer:** FOR i = 1 TO 5  
**Justification:**  
In Python, `range(1, 6)` gives the numbers 1 to 5, stopping before 6. The equivalent in pseudocode is `FOR i = 1 TO 5`, which includes both 1 and 5.

---

### Question 7 (2 marks)  
**Correct order:**
1. Planning  
2. Requirements definition  
3. Design  
4. Development  
5. Integration  
6. Testing  
7. Deployment  
8. Maintenance  

**Justification:**  
This is the standard order for the Software Development Life Cycle (SDLC). It starts with understanding the problem and ends with keeping the system running over time.

---

### Question 8 (2 marks)  
**Correct order:**
1. READ username  
2. READ password  
3. IF username AND password are correct THEN  
4. DISPLAY "Login successful"  
5. ELSE DISPLAY "Access denied"  
6. ENDIF  

**Justification:**  
This order reflects a basic login system. You collect both inputs, check them, then show a message based on the result.

---

### Question 9 (1 mark)  
**Correct answer:** Ensuring data is accurate and has not been tampered with  
**Justification:**  
Integrity means making sure data stays correct and unchanged unless it's meant to be updated. This prevents things like corrupted files or unauthorised changes.

---

### Question 10 (3 marks)

| Input (mark) | Expected output (grade)  |
|--------------|--------------------------|
| 90           | A                        |
| 70           | B                        |
| 50           | C                        |
| 49           | D                        |

**Justification:**  
These test values cover all possible paths through the algorithm: A, B, C, and D. Each input checks whether the logic handles that boundary correctly.

---

### Question 11 (2 marks)  
**Correct answers:**  
- A user inputs `<script>` code into a form and it executes in another user’s browser  
- A user clicks a link in a comment and it runs JavaScript that steals cookies  
- A website allows users to upload profile bios without sanitising HTML input  

**Justification:**  
These are all examples of XSS, where attackers inject scripts into websites that get executed in someone else’s browser. The other two options are security issues but unrelated to XSS.

---

### Question 12 (6 marks)

**(a) Compare the agile and waterfall approaches to software development.**  
Agile is flexible, involving frequent updates and user feedback. Waterfall is a fixed, step-by-step process. Agile suits projects needing change; Waterfall suits projects with clear, fixed requirements.

**(b) Explain what a WAgile approach is and when it might be useful.**  
WAgile combines parts of Waterfall and Agile. It uses a clear plan at the start (like Waterfall) but allows feedback and iteration in later stages (like Agile). Useful for teams needing structure and flexibility.

**(c) Why is it important for teams to choose the right development approach?**  
The right approach affects time, cost, and quality. A mismatched method can lead to delays, confusion, or poor results. Each project’s needs and team experience should guide the decision.

---

### Question 13 (3 marks)  
**Answer:**  
WCAG has helped web designers make websites more accessible. For example, using `<alt>` text on images allows screen readers to describe visuals. Also, clear contrast in CSS improves readability for users with vision issues. These changes help more people access online content.

---

### Question 14 (6 marks)

**(a) Explain how control structures such as loops and decisions are represented in the chart. Refer to specific examples from the diagram.**  
**(3 marks)**

Loops are shown using curved arrows that loop back to an earlier module. For example, the "Until library closes" loop at the top indicates the system continues to run both borrowing and returning processes until the library closes. Another loop, “Until no more books,” is used inside the "Process books" module to repeatedly process books for a student until they have no more to borrow.

Decisions are shown using diamond-shaped symbols. For instance, after "Book information" is retrieved, there is a decision point for "Book available." This decides whether to continue and update records or not. Similarly, when a book is returned, the system checks for an "Overdue flag" before deciding whether to perform additional steps.

---

**(b) Describe what happens when an overdue book is returned.**  
**(3 marks)**

When a book is returned, the system follows the "Returning" path. It first checks the book using the "Check book" module, which gathers the book's details and due date. It then uses the "Check if overdue" module to compare the due date to the current date from "Locate book record". If the book is overdue, an "Overdue flag" is set.

Once flagged, the system proceeds to "Update files," where both the book and student records are updated. The overdue flag and student details are used to record the late return. The system may also generate a report using the "Reports" module, which receives both book and student details for tracking or notification purposes.

---

### Question 15 (3 marks)

**SQL Answer:**
```sql
SELECT * FROM Customers
WHERE SignupYear < 2022 AND ActiveSubscription = TRUE;
```

---

### Question 16 (3 marks)

- **Logistic Regression** is used for yes/no outcomes. Example: predicting if a student will pass or fail based on their study time.
- **Linear Regression** predicts continuous values. Example: estimating someone’s exam score based on how many hours they studied.
- **K-Nearest Neighbour** classifies data based on similarity to others. Example: grouping users into recommendation categories based on past purchases.

---

### Question 17 (3 marks)

**SQL query:**

```sql
SELECT Players.Name
FROM Players
JOIN Scores ON Players.PlayerID = Scores.PlayerID
WHERE Players.Country = 'AU' AND Scores.Points > 1000;
```

This joins the Players and Scores tables using `PlayerID`, filters for Australian players, and selects only those with more than 1000 points.

---

### Question 18 (6 marks)

**(a) Explain how form validation can help prevent invalid usernames being saved.**  
Form validation checks the input before it reaches the server. This helps stop incorrect or dangerous values from being stored in the system. It makes sure the data follows the expected rules and improves security.

**(b) Python function:**

```python
def is_valid_username(username):
    if len(username) < 6:
        return False
    if not username[0].isalpha():
        return False
    if not username.isalnum():
        return False
    return True
```

This function checks the username length, that it starts with a letter, and only uses letters and numbers.

---

### Question 19 (4 marks)

**Correct order of steps:**

1. Client requests a secure connection to the server  
2. Server sends its digital certificate to the client  
3. Client verifies the certificate and creates a session key  
4. Server and client begin encrypted communication  

This is the basic process for setting up a secure SSL/TLS connection.

---

### Question 20 (4 marks)

**(a)** Bias in AI means the system makes unfair decisions because of patterns in the training data.

**(b)** An example is a job application system that prefers certain names or genders because the training data was biased.

**(c)** Two ways to reduce bias:
- Use diverse and balanced training datasets  
- Test regularly to detect and fix biased outcomes

---

### Question 21 (6 marks)  
**UML Class Diagram**

```plaintext
+---------------------------+
|         Student           |
+---------------------------+
| - name: String            |
| - studentID: String       |
+---------------------------+
           | 1
           | 
           | *
+---------------------------+
|           Loan            |
+---------------------------+
| - loanID: String          |
| - dueDate: Date           |
| - returned: Boolean       |
+---------------------------+
           | 1
           | 
           | *
+---------------------------+
|           Book            |
+---------------------------+
| - title: String           |
| - isbn: String            |
| - category: String        |
+---------------------------+
```

**Relationships:**
- A **Student** can have **many Loans** → `Student 1 → * Loan`
- Each **Loan** is linked to **one Student**
- A **Loan** can include **many Books** → `Loan 1 → * Book`
- Each **Book** belongs to **one Loan**

---

### Question 22 (5 marks)

**(a)**  
- Hashing is one-way and can't be reversed, while encryption is two-way and can be decrypted.  
- Hashing always gives the same result for the same input, but encryption uses a key and produces different outputs depending on the method.

**(b)**  
- Hashing: Used to store passwords securely because they don’t need to be reversed.  
- Encryption: Used to send private messages because the data must be recovered and read again.

**(c)**  
- Symmetric encryption uses the same key to encrypt and decrypt. Asymmetric uses a public key to encrypt and a private key to decrypt.

---

### Question 23 (4 marks)

**(a)**  
- Advantage 1: Easier to update content without coding, often instead using a click-and-drag system to build your web pages.
- Advantage 2: Many themes and plugins are available for free, so you can have professional looking web pages without much design knowledge. 
- Disadvantage: Less flexible in design. If it can't be done with the design tools provided or added with a plugin/widget, you're out of luck.

**(b)**  
- A small business wanting to launch a blog or online store quickly should use a CMS. It saves time and doesn’t require a developer to change the content.

---

### Question 24 (4 marks)

**(a)**  
- It’s free to use, which saves money.  
- The source code is available, so developers can modify it to suit their needs.

**(b)**  
- Risk: Open-source software might have unpatched security issues.  
- To reduce the risk, always use well-maintained projects and keep them updated.

---

### Question 25 (8 marks)

Streaming platforms like Netflix and Spotify use metadata and big data to give users a smoother and more personalised experience.

Metadata is information that describes content, such as the title, genre, artist, or language. Big data refers to the large amount of information collected from users, like what shows or songs they play, pause, skip, or search for. This data is collected every time someone uses the app, and it helps the platform learn about user preferences.

Real-time data ingestion means that this information is collected and processed as it happens. For example, when you watch a show, the system records that activity immediately. This allows the platform to quickly update what it recommends to you and what shows or songs appear on your home screen.

Personalisation is a key feature of these platforms. By combining metadata with your viewing or listening habits, the system can suggest content that matches your interests. If you often listen to pop music or watch documentaries, the platform will recommend similar content. This helps keep users interested and saves time searching for something to watch or listen to.

Behind the scenes, the platform needs to support millions of users at once. To do this, they use load balancing. Load balancing spreads user requests across different servers so that no single server becomes overloaded. This keeps the app running smoothly, even when many people are using it at the same time.

These systems often use a microservices architecture. Instead of one big program doing everything, the system is made of smaller services that each do one job, like handling user accounts, streaming content, or giving recommendations. This makes the system easier to update and scale, since each part can work independently and be improved without affecting the others.

The overall system architecture is designed to be fast, reliable, and able to handle large amounts of data. It allows content to be delivered quickly and personalisation to happen in real time.

In summary, streaming platforms use metadata and big data to understand users and deliver a personalised experience. Real-time data ingestion, smart recommendations, load balancing, and microservices all work together to make the platform fast, helpful, and enjoyable to use.

---

### Question 26 (8 marks)

Data privacy is an essential part of software engineering, especially as modern systems collect personal data from users. Developers must follow legal and ethical guidelines to ensure this data is handled safely and respectfully.

In Australia, the Privacy Act 1988 includes the Australian Privacy Principles (APPs), which set out rules for how organisations can collect, store, and use personal information. For example, APP 6 requires data to only be used for the purpose it was collected, and APP 11 requires reasonable steps to protect it from misuse, interference, or loss. Software engineers must design systems that meet these requirements to avoid breaking the law.

There are several ways developers can protect user data. These include encrypting data during storage and transmission, using secure authentication methods like multi-factor login, and limiting access to data only to people who need it. It’s also important to clearly explain to users what data is collected and why, usually through a privacy policy.

Ethically, software engineers have a duty to respect the privacy of users. Misusing or carelessly handling data can lead to serious harm, like identity theft or loss of trust. Even if the law doesn’t cover every situation, doing the right thing means treating data responsibly and putting user safety first.

A well-known example of a privacy breach is the 2018 Facebook–Cambridge Analytica scandal. Millions of users’ data was accessed without proper consent and used to influence political campaigns. This led to public backlash, legal investigations, and loss of trust in the platform.

In summary, data privacy is not just a legal requirement but an ethical responsibility. By following laws like the APPs and using secure development practices, software engineers can protect users and build systems that are safe, trustworthy, and compliant.