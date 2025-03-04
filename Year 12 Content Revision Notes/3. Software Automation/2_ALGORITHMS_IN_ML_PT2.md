# Algorithms in Machine Learning Part 2 - HSC Software Engineering Revision Notes

## 1. Models Used by Software Engineers to Design and Analyse ML
Software engineers use different ML models to **analyze data, recognize patterns, and make predictions**. Two commonly used models are **decision trees and neural networks**.

### Decision Trees
- A **tree-like structure** that breaks down a decision into smaller, simpler parts.
- Nodes represent **decisions or splits** based on input data.
- Used in **classification and regression tasks**.
- *Example:* Predicting whether a customer will buy a product based on age and income.

#### Example of a Simple Decision Tree:
```
        Is Age > 30?
       /         \
     Yes          No
    /              \
   High Income?    Buys
  /        \
 Yes       No
Buys       Doesn't Buy
```
- *Code Example:* Creating a decision tree using Python’s `sklearn`:
  ```python
  from sklearn.tree import DecisionTreeClassifier
  X = [[25, 30000], [35, 60000], [45, 80000]]  # Age, Income
  y = [0, 1, 1]  # 0 = No, 1 = Yes
  model = DecisionTreeClassifier().fit(X, y)
  print(model.predict([[30, 50000]]))
  ```

### Neural Networks
- A network of **artificial neurons** that simulates how the human brain processes information.
- Consists of **input layers, hidden layers, and output layers**.
- Used in **image recognition, natural language processing, and self-driving cars**.

#### Simple Neural Network Structure:
```
Input Layer → Hidden Layer(s) → Output Layer
```
- Each neuron processes input, applies a function, and passes the result forward.
- *Example:* Neural networks power **facial recognition in security systems**.

---

## 2. Types of Algorithms Associated with ML
ML algorithms help in **data prediction, classification, and pattern recognition**. Three commonly used algorithms are **linear regression, logistic regression, and K-nearest neighbour (KNN)**.

### 1. Linear Regression
- A **supervised learning algorithm** used for **predicting continuous values**.
- Fits a **straight line** to the data points.
- *Example:* Predicting **house prices based on square footage**.

- *Equation:*  
  \[ y = mx + b \]
  - `y` = predicted value
  - `m` = slope of the line
  - `x` = input feature
  - `b` = intercept

- *Code Example:* Implementing linear regression in Python:
  ```python
  from sklearn.linear_model import LinearRegression
  X = [[1000], [1500], [2000]]  # Square footage
  y = [200000, 250000, 300000]  # House prices
  model = LinearRegression().fit(X, y)
  print(model.predict([[1800]]))  # Predict price for 1800 sq ft
  ```

### 2. Logistic Regression
- Used for **binary classification problems** (e.g., yes/no, spam/not spam).
- Instead of a straight line, it produces an **S-shaped curve** (sigmoid function) that maps input values between 0 and 1.
- *Example:* Predicting whether an email is **spam or not spam**.

- *Code Example:* Predicting spam emails with logistic regression:
  ```python
  from sklearn.linear_model import LogisticRegression
  X = [[0.1], [0.5], [0.9]]  # Email spam probability factors
  y = [0, 0, 1]  # 0 = Not Spam, 1 = Spam
  model = LogisticRegression().fit(X, y)
  print(model.predict([[0.7]]))
  ```

### 3. K-Nearest Neighbour (KNN)
- A classification algorithm that assigns a label based on the **majority class of its nearest neighbors**.
- Uses **Euclidean distance** to find the closest points.
- Works well for **pattern recognition and recommendation systems**.
- *Example:* Recommending movies based on a user’s past preferences.

- *Code Example:* Implementing KNN in Python:
  ```python
  from sklearn.neighbors import KNeighborsClassifier
  X = [[1, 2], [2, 3], [3, 4], [6, 7]]  # Data points
  y = [0, 0, 1, 1]  # Labels
  model = KNeighborsClassifier(n_neighbors=2).fit(X, y)
  print(model.predict([[4, 5]]))  # Predict class for a new data point
  ```
