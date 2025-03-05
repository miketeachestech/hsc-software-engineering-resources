# **Practice Questions: Mechatronic Systems and Control Algorithms**

## **Multiple Choice Questions**

**1.** *(1 mark)* What is the main function of a **microcontroller** in a mechatronic system?  
   - A) To provide graphical user interfaces.  
   - B) To control sensors and actuators based on programmed instructions.  
   - C) To store large amounts of external data.  
   - D) To replace mechanical components in robotic systems.  

**2.** *(1 mark)* Which of the following is a characteristic of a **closed-loop control system**?  
   - A) Operates based only on predefined instructions without feedback.  
   - B) Adjusts system behavior using sensor feedback.  
   - C) Does not require sensors to function.  
   - D) Runs continuously without making corrections.  

**3.** *(1 mark)* What type of sensor is typically used for **collision detection** in autonomous robots?  
   - A) Temperature sensor  
   - B) Ultrasonic sensor  
   - C) Light sensor  
   - D) Humidity sensor  

---

## **Short Answer Questions**

**4.** *(3 marks)* Explain the difference between **open-loop and closed-loop control systems**. Provide a real-world example for each.

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

**6.** *(3 marks)* How do **sensors, actuators, and controllers** work together in a mechatronic system? Provide an example.

---

## **Code-Based Questions**

**7.** *(4 marks)* Write a **Python class** `TemperatureControlSystem` that:
   - Reads a temperature sensor value.
   - Turns a cooling fan **ON** if the temperature is above 30°C.
   - Turns the fan **OFF** otherwise.
   - Simulate sensor readings using a `random` value.

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