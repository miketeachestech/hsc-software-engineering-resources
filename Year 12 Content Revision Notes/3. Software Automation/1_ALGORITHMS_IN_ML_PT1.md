# Algorithms in Machine Learning Part 1 - HSC Software Engineering Revision Notes

## 1. How Machine Learning Supports Automation
Machine Learning (ML) enables computers to **learn from data** and improve their performance on tasks **without explicit programming**. It is widely used in automation to improve **efficiency, accuracy, and decision-making**.

### ML in DevOps
- **Predictive Analytics:** ML helps predict **system failures** and optimize **server performance**.
- **Automated Code Review:** Identifies **bugs, security vulnerabilities, and inefficiencies**.
- **CI/CD Optimization:** Automates **testing and deployment processes**.

### ML in Robotic Process Automation (RPA)
- Enhances **rule-based automation** by allowing bots to learn from data.
- Used in **document processing, chatbots, and customer service**.
- *Example:* An RPA bot automatically extracts and processes invoices.

### ML in Business Process Automation (BPA)
- Improves **workflow efficiency** by automating **decision-making**.
- **Fraud detection, sentiment analysis, and customer recommendations**.
- *Example:* A finance system uses ML to approve **loan applications based on risk scores**.

---

## 2. Difference Between Artificial Intelligence (AI) and Machine Learning (ML)
| **Aspect** | **Artificial Intelligence (AI)** | **Machine Learning (ML)** |
|------------|----------------------------------|---------------------------|
| Definition | The broader concept of **machines simulating human intelligence**. | A subset of AI that **learns from data** without explicit programming. |
| Scope | Encompasses **ML, expert systems, robotics, NLP**. | Focuses on **pattern recognition and prediction**. |
| Example | AI-powered **chess bots, self-driving cars**. | ML-powered **recommendation systems, fraud detection**. |

*Example:* AI includes a **self-driving car’s decision-making system**, while ML is used in the car’s **object recognition and lane detection**.

---

## 3. Models of Training ML
Machine learning models are **trained using different approaches** based on the availability of labeled data and learning objectives.

### 1. Supervised Learning
- The model learns from **labeled data**.
- Input-output pairs are provided during training.
- *Example:* Spam email classification (Emails labeled as **spam or not spam**).
- *Code Example:* Simple **Supervised Learning** model using Python’s `sklearn`:
  ```python
  from sklearn.linear_model import LogisticRegression
  X = [[0], [1], [2], [3]]  # Features
  y = [0, 0, 1, 1]  # Labels
  model = LogisticRegression().fit(X, y)
  print(model.predict([[1.5]]))  # Predicts class
  ```

### 2. Unsupervised Learning
- The model learns **patterns and relationships** from **unlabeled data**.
- Used for **clustering and anomaly detection**.
- *Example:* Customer segmentation in marketing.
- *Code Example:* Using `sklearn` for clustering:
  ```python
  from sklearn.cluster import KMeans
  X = [[1,2], [1,4], [3,2], [5,6]]
  model = KMeans(n_clusters=2).fit(X)
  print(model.labels_)  # Outputs cluster labels
  ```

### 3. Semi-Supervised Learning
- Combines **a small amount of labeled data** with **a large amount of unlabeled data**.
- Useful when labeling data is expensive or time-consuming.
- *Example:* Medical diagnosis where few cases are labeled but vast patient data is available.

### 4. Reinforcement Learning
- The model learns by **trial and error** and receives **rewards or penalties**.
- Used in **robotics, gaming, and self-driving cars**.
- *Example:* A robot learning to navigate an environment by receiving **positive reinforcement for correct moves**.

---

## 4. Common Applications of Key ML Algorithms
Machine learning is applied in various industries to **analyze data, improve decision-making, and enhance user experiences**.

### 1. Data Analysis and Forecasting
- ML models predict **future trends** based on historical data.
- Used in **stock market predictions, weather forecasting, and sales forecasting**.
- *Example:* A retail company uses ML to **forecast demand for seasonal products**.

### 2. Virtual Personal Assistants
- AI-powered assistants like **Siri, Alexa, Google Assistant** use ML for **natural language processing (NLP)**.
- They learn **user preferences and improve interactions over time**.
- *Example:* Google Assistant suggests **reminders based on a user’s daily routine**.

### 3. Image Recognition
- ML algorithms can **detect and classify objects in images**.
- Used in **facial recognition, medical imaging, and security systems**.
- *Example:* Facebook’s ML model automatically tags people in photos.
- *Code Example:* Basic image classification using `tensorflow`:
  ```python
  import tensorflow as tf
  model = tf.keras.applications.MobileNetV2(weights='imagenet')
  ```