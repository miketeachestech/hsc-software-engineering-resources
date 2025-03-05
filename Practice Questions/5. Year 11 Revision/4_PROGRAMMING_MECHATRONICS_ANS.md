# **Answers: Mechatronic Systems and Control Algorithms**

## **Multiple Choice Questions**

**1.** *(1 mark)*  
- Correct Answer: **B) To control sensors and actuators based on programmed instructions.**  
- **1 mark** awarded for correctly selecting the answer.  

**2.** *(1 mark)*  
- Correct Answer: **B) Adjusts system behavior using sensor feedback.**  
- **1 mark** awarded for correctly selecting the answer.  

**3.** *(1 mark)*  
- Correct Answer: **B) Ultrasonic sensor**  
- **1 mark** awarded for correctly selecting the answer.  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the difference between **open-loop and closed-loop control systems**. Provide a real-world example for each.
- **1 mark** for stating that an **open-loop system operates without feedback**, only following predefined instructions.
- **1 mark** for explaining that a **closed-loop system uses sensor feedback to adjust its actions**.
- **1 mark** for providing examples:
  - **Open-loop**: A **microwave oven** that runs for a fixed time without sensing food temperature.
  - **Closed-loop**: A **thermostat-controlled air conditioner** that turns off when the desired temperature is reached.

**5.** *(3 marks)* Identify the **error(s) in the following motor control algorithm** and suggest a fix:
```python
class Motor:
    def __init__(self):
        self.speed = 0

    def increase_speed(self, increment):
        self.speed += increment

motor = Motor()
motor.increase_speed()
print(motor.speed)
```
- **1 mark** for identifying the error: `increase_speed()` is missing a required argument.
- **1 mark** for explaining that `increment` must be specified when calling the function.
- **1 mark** for providing the correct fix:
```python
motor.increase_speed(10)  # Specify increment value
```

**6.** *(3 marks)* How do **sensors, actuators, and controllers** work together in a mechatronic system? Provide an example.
- **1 mark** for stating that **sensors collect data**, **controllers process it**, and **actuators perform actions**.
- **1 mark** for explaining the feedback loop in an automated system.
- **1 mark** for providing an example (e.g., **self-driving cars** use sensors to detect objects, controllers process data, and actuators steer or brake).

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a **Python class** `TemperatureControlSystem` that:
```python
import random

class TemperatureControlSystem:
    def __init__(self):
        self.temperature = 0
        self.fan_status = "OFF"

    def read_sensor(self):
        self.temperature = random.uniform(20, 40)  # Simulated sensor reading

    def control_fan(self):
        if self.temperature > 30:
            self.fan_status = "ON"
        else:
            self.fan_status = "OFF"
        print(f"Temperature: {self.temperature:.1f}°C, Fan: {self.fan_status}")

system = TemperatureControlSystem()
system.read_sensor()
system.control_fan()
```
- **1 mark** for correctly defining the `TemperatureControlSystem` class.
- **1 mark** for simulating sensor readings using `random`.
- **1 mark** for implementing logic to **turn the fan on or off**.
- **1 mark** for printing the output correctly.

**8.** *(4 marks)* The following Python code **aims to implement an ultrasonic sensor for obstacle detection** but contains a bug. Identify and fix the issue.
```python
import random

def get_distance():
    return random.randint(5, 50)  # Simulated distance sensor

def obstacle_detection():
    distance = get_distance()
    if distance < 10:
        print("No obstacle detected, continue moving")
    else:
        print("Obstacle detected! Stopping.")

obstacle_detection()
```
**Bug:** The logic is incorrect—the messages are reversed.

**Fixed Version:**
```python
def obstacle_detection():
    distance = get_distance()
    if distance < 10:
        print("Obstacle detected! Stopping.")
    else:
        print("No obstacle detected, continue moving")
```
- **1 mark** for identifying the incorrect message logic.
- **1 mark** for explaining the correct behavior.
- **1 mark** for swapping the messages.
- **1 mark** for maintaining proper formatting.

**9.** *(4 marks)* Convert the following **pseudocode into Python code**:
```
BEGIN
    WHILE robot is ON
        READ sensor_value
        IF sensor_value < threshold THEN
            STOP robot
        ELSE
            MOVE forward
END
```
**Python Implementation:**
```python
class Robot:
    def __init__(self):
        self.is_on = True

    def read_sensor(self):
        return random.randint(5, 50)  # Simulated sensor reading

    def move(self):
        while self.is_on:
            sensor_value = self.read_sensor()
            if sensor_value < 10:
                print("Obstacle detected! Stopping robot.")
                break
            else:
                print("Moving forward...")
```
- **1 mark** for correctly defining the **Robot class**.
- **1 mark** for simulating a **sensor reading**.
- **1 mark** for implementing the **loop** correctly.
- **1 mark** for ensuring the robot **stops when an obstacle is detected**.

