# Programming for Automation - HSC Software Engineering Revision Notes

## 1. Designing, Developing, and Applying ML Regression Models Using OOP
Object-Oriented Programming (OOP) can be used to structure **Machine Learning (ML) models** in a way that enhances **code reusability, modularity, and maintainability**. Regression models predict **numeric values** based on input data.

### **1.1 Linear Regression**
Linear Regression models the relationship between **a dependent variable (y)** and **one or more independent variables (x)** using a straight-line equation:

\[ y = mx + b \]

- `y`: The value we are trying to predict (e.g., house price, sales figures).
- `m`: The slope of the line, representing how much `y` changes when `x` increases.
- `x`: The input value (e.g., number of hours studied).
- `b`: The intercept, or where the line crosses the y-axis.

This means that for a given input `x`, the model **multiplies it by a weight (`m`) and adds a bias (`b`)** to make a prediction.

#### **Implementation in OOP (Python using scikit-learn)**
```python
import numpy as np
from sklearn.linear_model import LinearRegression

class LinearRegressor:
    def __init__(self):
        self.model = LinearRegression()
    
    def train(self, X, y):
        self.model.fit(X, y)
    
    def predict(self, X):
        return self.model.predict(X)

# Example Usage
X = np.array([[1], [2], [3], [4], [5]])  # Input Features
y = np.array([10, 20, 30, 40, 50])  # Target Values

regressor = LinearRegressor()
regressor.train(X, y)
print(regressor.predict([[6]]))  # Predict for x = 6
```

### **1.2 Polynomial Regression**
Polynomial regression is an extension of linear regression that can **fit curved relationships** by adding higher-degree polynomial terms. The equation looks like this:

\[ y = a + bx + cx^2 + dx^3 + ... \]

- `a`, `b`, `c`, `d`: Coefficients learned from the data.
- `x^2`, `x^3`: Higher-order terms allow the model to **capture more complex patterns**.

This is useful when a simple straight line **doesn’t fit the data well**.

#### **Implementation in OOP (Python using scikit-learn)**
```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import make_pipeline

class PolynomialRegressor:
    def __init__(self, degree=2):
        self.model = make_pipeline(PolynomialFeatures(degree), LinearRegression())
    
    def train(self, X, y):
        self.model.fit(X, y)
    
    def predict(self, X):
        return self.model.predict(X)

# Example Usage
X = np.array([[1], [2], [3], [4], [5]])
y = np.array([2, 6, 12, 20, 30])

poly_regressor = PolynomialRegressor(degree=3)
poly_regressor.train(X, y)
print(poly_regressor.predict([[6]]))  # Predict for x = 6
```

### **1.3 Logistic Regression**
Logistic Regression is used for **classification problems**, meaning it predicts **categories** instead of numbers (e.g., "spam" or "not spam"). Instead of a straight line, it uses an **S-shaped curve** (sigmoid function) to map values between **0 and 1**:

\[ P(y=1) = \frac{1}{1 + e^{-(b_0 + b_1X_1 + ... + b_nX_n)}} \]

- The **denominator** ensures that the output is always **between 0 and 1**.
- Values closer to 1 indicate higher confidence in **belonging to the positive class**.

#### **Implementation in OOP (Python using scikit-learn)**
```python
from sklearn.linear_model import LogisticRegression

class LogisticRegressor:
    def __init__(self):
        self.model = LogisticRegression()
    
    def train(self, X, y):
        self.model.fit(X, y)
    
    def predict(self, X):
        return self.model.predict(X)

# Example Usage
X = np.array([[0.1], [0.5], [0.9], [1.5]])  # Features
y = np.array([0, 0, 1, 1])  # Labels (Binary classification)

logistic_regressor = LogisticRegressor()
logistic_regressor.train(X, y)
print(logistic_regressor.predict([[1.0]]))  # Predict for x = 1.0
```

---

## 2. Applying Neural Network Models Using OOP to Make Predictions
Neural Networks (NN) **simulate how the human brain processes information**. Instead of a single equation, they use **multiple layers of neurons** to extract patterns from data.

### **2.1 Structure of a Simple Neural Network**
```
Input Layer → Hidden Layer(s) → Output Layer
```
Each neuron applies a **mathematical function** to its input and passes the result forward to the next layer.

- **Input Layer:** Accepts raw data.
- **Hidden Layers:** Process and refine the data.
- **Output Layer:** Generates a final prediction (e.g., "dog" vs "cat").

### **2.2 Implementing a Neural Network Using OOP (Python using TensorFlow/Keras)**
```python
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense
import numpy as np

class NeuralNetwork:
    def __init__(self, input_dim):
        self.model = Sequential([
            Dense(16, activation='relu', input_shape=(input_dim,)),
            Dense(8, activation='relu'),
            Dense(1, activation='sigmoid')  # Sigmoid for binary classification
        ])
        self.model.compile(optimizer='adam', loss='binary_crossentropy', metrics=['accuracy'])
    
    def train(self, X, y, epochs=50):
        self.model.fit(X, y, epochs=epochs, verbose=0)
    
    def predict(self, X):
        return self.model.predict(X)

# Example Usage
X = np.array([[0], [1], [2], [3]])  # Input Data
y = np.array([0, 0, 1, 1])  # Labels

nn = NeuralNetwork(input_dim=1)
nn.train(X, y)
print(nn.predict(np.array([[1.5]])))  # Predict for x = 1.5
```
---

## **3. Key Takeaways on Neural Networks**
Neural networks are the foundation of **Machine Learning and AI**. They help models like ChatGPT **analyze patterns, learn relationships between words, and make predictions**. Here are some key concepts explained in **simple terms**.

### **1. Activation Functions (How Neurons Decide What Matters)**
- Every neuron in a neural network **processes input data** and decides whether to "activate".
- An **activation function** is like a decision-maker that tells a neuron **how much importance to give** to the input.
- Example: If you’re making a **spam filter**, an activation function decides if an email looks "spammy" enough to be classified as spam.
- **Common Activation Functions:**
  - **ReLU (Rectified Linear Unit):** If the input is positive, pass it forward; if negative, ignore it.
  - **Sigmoid:** Compresses values between 0 and 1, used in classification problems (e.g., "Is this email spam?").

### **2. Optimizers (How the Model Learns and Improves)**
- Optimizers help the neural network **adjust itself** to become more accurate.
- They work by **changing the model’s internal parameters** (called weights and biases) based on errors it makes.
- Example: If a chatbot keeps giving wrong answers, an optimizer tweaks the network so it improves over time.
- **Common Optimizers:**
  - **Gradient Descent:** Moves in the direction that reduces errors.
  - **Adam Optimizer:** A more advanced version that adapts the learning process based on past mistakes.

### **3. Loss Functions (Measuring How Wrong the Model Is)**
- The "loss" is **how far off the model’s prediction is from the correct answer**.
- A loss function helps the model figure out **how much it needs to improve**.
- Example: If a house price prediction model says a house costs **$500,000**, but the real price is **$480,000**, the loss function calculates the **$20,000 error**.
- **Common Loss Functions:**
  - **Mean Squared Error (MSE):** Used for predicting numbers, calculates the average difference between predicted and actual values.
  - **Cross-Entropy Loss:** Used for classification problems, helps predict categories like "spam" or "not spam".

### **4. How Everything Works Together**
- The **activation function** decides which neurons are important.
- The **optimizer** adjusts the model based on errors.
- The **loss function** tells the model how much it needs to improve.
- Over many cycles, the model **learns patterns and gets better at making predictions**.

---

## 4. An Example: How ChatGPT Works as a Neural Network
ChatGPT is a type of **artificial neural network** called a **Transformer model** (specifically, GPT-4). It learns to generate text by **predicting the next word in a sentence** based on **patterns it has learned from large amounts of data**.

### **1. Neural Network Structure**
- ChatGPT is built using a **Transformer-based neural network**.
- It consists of **many layers of artificial neurons** that process information.
- The network is trained on a vast collection of **text data** to learn how words and sentences fit together.

### **2. Training Process**
- ChatGPT was trained on **billions of sentences** from books, articles, and websites.
- It doesn’t **memorize** facts—it learns **patterns in language**.
- The training process involves showing the model **a sentence with a missing word** and asking it to predict the missing part.

### **3. Tokenization**
- When you type a message, ChatGPT **breaks it into smaller pieces called tokens** (e.g., "Hello world" → `["Hello", "world"]`).
- These tokens are converted into **numbers** so that the neural network can process them mathematically.

### **4. Self-Attention Mechanism (Understanding Context)**
- ChatGPT uses **self-attention**, which allows it to weigh the importance of different words in a sentence.
- Example: In **"The cat sat on the mat"**, the model recognizes that "cat" and "sat" are related, even if other words separate them.

### **5. Generating Responses**
- When you type a message, ChatGPT **analyzes context** and **predicts the most likely next words**.
- Instead of choosing the most common response, it selects words based on **probabilities**.

### **6. Reinforcement Learning and Fine-Tuning**
- After training, ChatGPT was fine-tuned using **human feedback** to make responses **more helpful and less biased**.
- This process is called **Reinforcement Learning from Human Feedback (RLHF)**.

### **Summary**
- **ChatGPT is a neural network** that processes text using **self-attention and pattern recognition**.
- It **doesn’t think** like a human—it **predicts the next most likely words**.
- Neural networks **learn from errors** using **activation functions, optimizers, and loss functions**.
- These concepts allow **AI models to improve and become more accurate over time**.