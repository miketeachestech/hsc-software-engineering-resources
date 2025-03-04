# Designing Control Algorithms - HSC Software Engineering Revision Notes

## 1. Developing, Modifying, and Applying Algorithms to Control a Mechatronic System
Control algorithms are essential for **automating mechatronic systems**, allowing them to function without direct human input. These algorithms use **sensors, actuators, and control logic** to manage system behavior.

### **1.1 Example: Basic Motor Control Algorithm**
This algorithm **activates a motor** based on sensor input.

#### **Pseudocode**
```
BEGIN
    READ sensor_value
    IF sensor_value > threshold THEN
        ACTIVATE motor
    ELSE
        STOP motor
END
```

#### **Python Implementation**
```python
import RPi.GPIO as GPIO
import time

SENSOR_PIN = 4
MOTOR_PIN = 17

GPIO.setmode(GPIO.BCM)
GPIO.setup(SENSOR_PIN, GPIO.IN)
GPIO.setup(MOTOR_PIN, GPIO.OUT)

while True:
    if GPIO.input(SENSOR_PIN):  # Sensor detects movement
        GPIO.output(MOTOR_PIN, GPIO.HIGH)  # Turn on motor
    else:
        GPIO.output(MOTOR_PIN, GPIO.LOW)  # Turn off motor
    time.sleep(0.5)
```
- **Uses a sensor to activate a motor.**
- **Loop continuously checks input values.**

---

## 2. Algorithmic Patterns, Code, and Applications for Open and Closed Control Systems
Control systems are classified into **open-loop** and **closed-loop** systems.

### **2.1 Open-Loop Control Systems**
- **Does not use feedback.**
- The system follows **predefined instructions** without checking if the task is performed correctly.
- **Example:** A washing machine runs a cycle without checking if clothes are clean.

#### **Example: Open-Loop Algorithm (Simple Timer-Controlled Motor)**
```python
import time

def run_motor():
    print("Motor ON")
    time.sleep(5)  # Runs for 5 seconds
    print("Motor OFF")

run_motor()
```
- **Limitation:** No feedback to adjust based on real-world conditions.

---

### **2.2 Closed-Loop Control Systems**
- **Uses sensor feedback** to adjust behavior.
- The system continuously monitors performance and makes corrections.
- **Example:** A thermostat maintains a room’s temperature by turning heating on/off based on temperature readings.

#### **Example: Closed-Loop Algorithm (Temperature-Controlled Fan)**
```python
import random

def get_temperature():
    return random.uniform(15.0, 35.0)  # Simulated sensor reading

def control_fan():
    temperature = get_temperature()
    if temperature > 30:
        print("Fan ON - Cooling down")
    else:
        print("Fan OFF - Temperature is stable")

while True:
    control_fan()
    time.sleep(2)
```
- **Continuously adjusts the fan** based on temperature feedback.

---

## 3. Features of an Algorithm and Program Code Used for Autonomous Control
Autonomous control algorithms enable mechatronic systems to **operate independently** by making real-time decisions based on sensor data.

### **3.1 Features of Autonomous Control Algorithms**
| **Feature** | **Description** |
|------------|----------------|
| **Real-Time Decision Making** | Uses sensor input to adjust system behavior instantly. |
| **Error Handling** | Detects failures and applies corrective actions. |
| **Adaptive Behavior** | Adjusts based on environmental changes. |
| **Self-Learning (AI-Based)** | Uses machine learning to improve performance over time. |

### **3.2 Example: Obstacle Avoidance Robot Algorithm**
This algorithm enables a robot to **move forward** and avoid obstacles using an **ultrasonic sensor**.

#### **Pseudocode**
```
BEGIN
    WHILE robot is ON
        READ distance_sensor
        IF distance < 10cm THEN
            STOP movement
            TURN in random direction
        ELSE
            MOVE forward
END
```

#### **Python Implementation**
```python
import random

def get_distance():
    return random.randint(5, 30)  # Simulated distance sensor reading

def obstacle_avoidance():
    while True:
        distance = get_distance()
        if distance < 10:
            print("Obstacle detected! Turning...")
        else:
            print("Moving forward")
        time.sleep(1)

obstacle_avoidance()
```
- **Uses a distance sensor** to detect objects.
- **Automatically changes direction** when an obstacle is too close.