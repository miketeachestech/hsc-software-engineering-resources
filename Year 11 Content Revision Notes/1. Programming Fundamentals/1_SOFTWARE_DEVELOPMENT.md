# Software Development - Year 11 Software Engineering Revision Notes

## 1. Fundamental Software Development Steps
Software development follows a structured process to ensure programs are **functional, reliable, and maintainable**. Each step plays a role in turning an idea into a working software solution.

### **1.1 Requirements Definition**
- **What it is:** Understanding the problem and defining what the software must do.
- **Key Questions:**
  - What problem is the software solving?
  - Who will use it?
  - What features are needed?
- **Example:** A school wants an app to track student attendance. Requirements might include:
  - Ability for teachers to mark students as present/absent.
  - A database to store attendance records.

### **1.2 Determining Specifications**
- **What it is:** Translating requirements into **technical details**.
- **Includes:**
  - Choosing a programming language.
  - Deciding on database storage.
  - Setting performance goals (e.g., load time under 2 seconds).
- **Example:** If creating a website, specifications might include:
  - HTML/CSS for design, JavaScript for interaction.
  - MySQL database to store user accounts.

### **1.3 Design**
- **What it is:** Planning how the software will work before coding.
- **Common Design Elements:**
  - **Flowcharts** – Visual representation of logic.
  - **Wireframes** – UI layout sketches.
  - **Pseudocode** – Written steps of how the program will work.
- **Example:** A login system design might include:
  ```
  BEGIN
      Ask user for username and password
      Check database for user details
      IF match found THEN
          Grant access
      ELSE
          Show error message
  END
  ```

### **1.4 Development (Coding Phase)**
- **What it is:** Writing the actual code based on the design.
- **Programming Languages:** Python, Java, JavaScript, C++, etc.
- **Example:** A basic Python program that asks for a name and prints a greeting:
  ```python
  name = input("Enter your name: ")
  print("Hello, " + name + "!")
  ```

### **1.5 Integration**
- **What it is:** Combining different parts of the software so they work together.
- **Example:** A school system integrates:
  - A website (front-end) with a student database (back-end).
  - A mobile app with an online payment system.

### **1.6 Testing and Debugging**
- **What it is:** Ensuring the software works correctly and fixing errors.
- **Types of Testing:**
  - **Unit Testing** – Checking individual parts of the program.
  - **Integration Testing** – Ensuring different components work together.
  - **User Testing** – Getting real users to test and provide feedback.
- **Example:** A login system test:
  - Enter **correct credentials** → Should allow access.
  - Enter **wrong password** → Should show an error.

### **1.7 Installation**
- **What it is:** Deploying the software so users can install and use it.
- **Methods:**
  - **Cloud-based apps** (e.g., Google Docs) – No installation needed.
  - **Installable software** (e.g., Microsoft Office) – Needs downloading.
- **Example:** A school installs attendance-tracking software on all teacher computers.

### **1.8 Maintenance**
- **What it is:** Updating software to fix bugs and improve features.
- **Types of Maintenance:**
  - **Corrective Maintenance** – Fixing bugs.
  - **Adaptive Maintenance** – Updating to support new devices or systems.
  - **Enhancements** – Adding new features.
- **Example:** A mobile banking app releases an update to improve security.

---

## 2. Researching and Evaluating Online Code Collaboration Tools
Modern software development relies on **collaboration tools** to help teams write and manage code together.

### **What Are Code Collaboration Tools?**
- Platforms that allow multiple programmers to work on the same codebase.
- Help with **version control, issue tracking, and communication**.
- Essential for **team projects, open-source software, and professional development**.

### **Popular Online Code Collaboration Tools**
| **Tool** | **Features** | **Used For** |
|---------|-------------|--------------|
| **GitHub** | Version control, issue tracking, pull requests | Open-source projects, team collaboration |
| **GitLab** | Integrated CI/CD, DevOps tools | Enterprise software, secure coding environments |
| **Bitbucket** | Supports Git and Mercurial, Jira integration | Private repositories, team coding |
| **Replit** | Online coding, real-time collaboration | Beginners, quick prototyping |
| **Google Colab** | Jupyter Notebooks in the cloud | Machine learning, data science collaboration |

### **How Developers Use These Tools**
- **Version Control:**
  ```bash
  git init  # Initialize a new repository
  git add .  # Add files to staging
  git commit -m "Initial commit"  # Save changes
  git push origin main  # Upload to GitHub
  ```
- **Pull Requests:** Used to suggest and review code changes.
- **Issue Tracking:** Developers report and fix bugs collaboratively.
- **Live Collaboration:** Some platforms (e.g., Replit) allow coding together in real-time.

### **Advantages of Using Code Collaboration Tools**
- ✅ **Tracks Changes:** Allows programmers to revert to previous versions.
- ✅ **Enables Teamwork:** Multiple developers can work on the same project.
- ✅ **Supports Remote Work:** Teams can collaborate from different locations.
- ✅ **Improves Code Quality:** Peer reviews help catch errors before deployment.

### **Challenges of Code Collaboration**
- ⚠ **Merge Conflicts:** When multiple people edit the same file.
- ⚠ **Learning Curve:** Some tools (like Git) can be difficult for beginners.
- ⚠ **Internet Dependency:** Requires an internet connection for cloud collaboration.