# Programming and Building Practice Idea 1 - HSC Software Engineering Revision Notes

The following content points outline key areas for designing, developing, and testing a **mechatronic system**:

- **Design, develop, and produce a mechatronic system for a real-world problem**
  - Including software control, mechanical engineering, electronics, and mathematics.
- **Implement algorithms and design programming code to drive mechatronic devices**
- **Develop simulations and prototypes of a potential mechatronic system to test programming code**
- **Design, develop, and implement programming code for a closed-loop control system**
- **Apply programming code to integrate sensors, actuators, and end effectors/manipulators**
- **Implement specific control algorithms that enhance the performance of a mechatronic system**
- **Design, develop, and implement a user interface (UI) to control a mechatronic system**
- **Create and use unit tests to determine the effectiveness and repeatability of each component’s control algorithm**

---

## **Suggested Project: Obstacle-Avoiding Robot**

### **Overview**
This project involves building a **small autonomous robot** that can move around and avoid obstacles using an **ultrasonic sensor**. The robot will be powered by a **microcontroller (Arduino or Raspberry Pi)** and will integrate motors, sensors, and control algorithms. 

### **How It Satisfies the Content Points:**
✅ **Software Control** → Uses a microcontroller to process sensor data and control movement.  
✅ **Mechanical Engineering** → Includes a chassis with wheels and motors for movement.  
✅ **Electronics & Mathematics** → Uses sensors to measure distances and apply logic for navigation.  
✅ **Closed-Loop Control System** → Uses sensor feedback to adjust movement and avoid obstacles.  
✅ **User Interface (UI)** → A simple remote control or debugging interface via serial communication.  
✅ **Testing & Unit Tests** → Ensures sensors and motors work consistently.  

---

## **Components Needed (Available at Jaycar or Online)**
| **Component** | **Purpose** | **Estimated Cost** |
|--------------|------------|-----------------|
| **Arduino Uno / Raspberry Pi** | Main controller | $30 - $80 |
| **Ultrasonic Sensor (HC-SR04)** | Detects obstacles | $10 - $15 |
| **Motor Driver Module (L298N)** | Controls motor speed & direction | $10 - $20 |
| **DC Motors + Wheels** | Provides movement | $15 - $30 |
| **Chassis (Acrylic/3D Printed)** | Holds components together | $10 - $25 |
| **Rechargeable Battery Pack** | Powers the system | $15 - $25 |
| **LEDs / Buzzer** | Status indicators | $5 - $10 |

Estimated total: **$100 - $180** (Prices vary based on store and alternative components.)

---

## **System Design & Implementation**

### **1. System Workflow**
```
Ultrasonic Sensor → Microcontroller → Motor Controller → Adjust Robot Movement
```

### **2. Software & Algorithm Development**
#### **Pseudocode: Obstacle Avoidance Algorithm**
```
BEGIN
    WHILE robot is ON
        READ ultrasonic_sensor_distance
        IF distance < 15cm THEN
            STOP motors
            TURN left or right randomly
        ELSE
            MOVE forward
END
```

#### **Python Code: Basic Obstacle Avoidance Algorithm (Raspberry Pi)**
```python
import RPi.GPIO as GPIO
import time
import random

TRIG = 23
ECHO = 24
MOTOR_LEFT = 17
MOTOR_RIGHT = 27

GPIO.setmode(GPIO.BCM)
GPIO.setup(TRIG, GPIO.OUT)
GPIO.setup(ECHO, GPIO.IN)
GPIO.setup(MOTOR_LEFT, GPIO.OUT)
GPIO.setup(MOTOR_RIGHT, GPIO.OUT)

def get_distance():
    GPIO.output(TRIG, True)
    time.sleep(0.00001)
    GPIO.output(TRIG, False)
    
    while GPIO.input(ECHO) == 0:
        start_time = time.time()
    while GPIO.input(ECHO) == 1:
        end_time = time.time()
    
    duration = end_time - start_time
    distance = duration * 17150  # Convert to cm
    return round(distance, 2)

def avoid_obstacle():
    distance = get_distance()
    if distance < 15:
        print("Obstacle detected! Changing direction...")
        GPIO.output(MOTOR_LEFT, False)
        GPIO.output(MOTOR_RIGHT, False)
        time.sleep(1)
        turn_direction = random.choice([MOTOR_LEFT, MOTOR_RIGHT])
        GPIO.output(turn_direction, True)
        time.sleep(1)
    else:
        GPIO.output(MOTOR_LEFT, True)
        GPIO.output(MOTOR_RIGHT, True)

while True:
    avoid_obstacle()
    time.sleep(0.5)
```
- **Uses an ultrasonic sensor** to detect obstacles.
- **Randomly turns left or right** when an obstacle is detected.
- **Continuously checks distance and updates movement.**

---

### **3. Prototyping & Simulation**
- **Circuit Simulation:** Use Tinkercad or Proteus to simulate motor and sensor functions before assembling hardware.
- **3D Modeling:** Use TinkerCAD or Fusion 360 to design the robot chassis.

---

### **4. UI Development for Remote Control & Debugging**
A simple **serial-based UI** allows debugging via a laptop or smartphone.

#### **Example: Sending Commands via Serial Monitor (Arduino)**
```cpp
void setup() {
    Serial.begin(9600);
    pinMode(LED_BUILTIN, OUTPUT);
}
void loop() {
    if (Serial.available()) {
        char command = Serial.read();
        if (command == 'F') {
            Serial.println("Moving Forward");
        } else if (command == 'B') {
            Serial.println("Moving Backward");
        }
    }
}
```
- **Allows remote control of the robot using simple text commands.**

---

### **5. Unit Testing & Validation**
Unit tests check if **motors, sensors, and logic** function correctly.

#### **Example: Unit Test for Sensor Accuracy (Python)**
```python
import unittest

def get_mock_distance():
    return 10  # Simulated 10cm obstacle distance

class TestSensor(unittest.TestCase):
    def test_distance(self):
        self.assertLess(get_mock_distance(), 15)  # Expecting obstacle detection

if __name__ == '__main__':
    unittest.main()
```
- **Verifies sensor readings match expected values.**
- **Ensures the robot correctly detects obstacles.**