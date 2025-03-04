# Designing Algorithms Part 1 - HSC Software Engineering Revision Notes

## 1. Applying Computational Thinking and Algorithmic Design
Computational thinking is the **process of solving problems using logical and structured approaches**. Algorithmic design involves defining **clear steps** to achieve a solution.

### **Key Features of Standard Algorithms**

| **Feature**  | **Description** | **Example** |
|-------------|----------------|-------------|
| **Sequence** | Instructions are executed **in order**, one after another. | Following a recipe step-by-step. |
| **Selection** | A decision-making step that **executes different code based on conditions**. | "If it’s raining, take an umbrella; otherwise, wear sunglasses." |
| **Iteration** | A loop that **repeats a set of instructions** until a condition is met. | Counting from 1 to 10 using a loop. |
| **Identifying Data to Store** | Choosing what information needs to be **saved and processed** in an algorithm. | Storing a user's name, age, and email in a database. |

### **Example: Applying Sequence, Selection, and Iteration**
#### **Pseudocode: A simple login system**
```
BEGIN
    INPUT username, password
    IF username == "admin" AND password == "password123" THEN
        PRINT "Access granted"
    ELSE
        PRINT "Access denied"
    ENDIF
END
```

#### **Python Code Example**
```python
username = input("Enter username: ")
password = input("Enter password: ")

if username == "admin" and password == "password123":
    print("Access granted")
else:
    print("Access denied")
```

---

## 2. Applying Divide and Conquer & Backtracking
### **Divide and Conquer Strategy**
- **Breaks a problem into smaller subproblems**, solves each one, and combines them.
- Commonly used in **sorting algorithms (Merge Sort, Quick Sort)**.

#### **Example: Divide and Conquer (Merge Sort)**
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    while left and right:
        if left[0] < right[0]:
            result.append(left.pop(0))
        else:
            result.append(right.pop(0))
    return result + left + right

numbers = [6, 3, 8, 5, 2, 7, 4, 1]
print(merge_sort(numbers))
```

### **Backtracking Strategy**
- **Explores all possibilities** by trying different solutions and backtracking when a wrong path is taken.
- Used in **maze-solving algorithms, Sudoku solvers, and pathfinding**.

#### **Example: Backtracking (Solving a Maze)**
```python
def solve_maze(maze, x, y):
    if x == len(maze)-1 and y == len(maze[0])-1:
        return True  # Reached goal
    if maze[x][y] == 1:  # If path is open
        maze[x][y] = 2  # Mark as visited
        if solve_maze(maze, x+1, y) or solve_maze(maze, x, y+1):
            return True
        maze[x][y] = 1  # Backtrack
    return False
```

---

## 3. Developing Structured Algorithms Using Pseudocode and Flowcharts

### **Example: Calculating Factorial Using a Subprogram (Function)**
#### **Pseudocode**
```
BEGIN
    FUNCTION Factorial(n)
        IF n == 0 THEN
            RETURN 1
        ELSE
            RETURN n * Factorial(n-1)
        ENDIF
    END FUNCTION

    INPUT number
    PRINT Factorial(number)
END
```

#### **Flowchart Representation**
```
  +----------------+
  | Input number   |
  +----------------+
          |
          v
  +----------------+
  | Check if n == 0|
  +----------------+
      /      \
     Yes      No
    /          \
+---------+  +----------------+
| Return 1|  | Call Factorial(n-1) |
+---------+  +----------------+
```

#### **Python Implementation**
```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

number = int(input("Enter a number: "))
print("Factorial:", factorial(number))
```

---

## 4. Using Modelling Tools in Algorithm Design
Modeling tools help visualize and **structure complex algorithms** before implementation.

### **Common Modelling Tools**
| **Tool** | **Purpose** |
|---------|------------|
| **Structure Charts** | Break down functions and procedures into a **hierarchical** format. |
| **Abstraction Diagrams** | Represent essential parts of a problem, **ignoring unnecessary details**. |
| **Refinement Diagrams** | Show **step-by-step breakdowns** of a process from a high-level overview to detailed steps. |

Check out NESA's "Terms and Examples" document (see the NESA Resources folder) for examples of diagrams and notations.