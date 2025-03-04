# Programming and Building Practice Idea 2 - HSC Software Engineering Revision Notes

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

## **Suggested Project: Smart Automated Pet Feeder**

### **Overview**
A **Smart Automated Pet Feeder** is a **real-world mechatronic system** that dispenses food at scheduled times or based on a pet’s activity. This project integrates **software control, electronics, and mechanical engineering**, making it an excellent choice for high school students learning about mechatronic systems.

### **How It Satisfies the Content Points:**
✅ **Software Control** → Uses a microcontroller (e.g., Raspberry Pi or Arduino) to control the feeder.  
✅ **Mechanical Engineering** → A servo motor controls the food dispenser.  
✅ **Electronics & Mathematics** → Uses sensors to track feeding times and portion sizes.  
✅ **Closed-Loop Control System** → A weight sensor ensures the correct amount of food is dispensed.  
✅ **User Interface (UI)** → A simple web or mobile app allows users to schedule feedings.  
✅ **Testing & Unit Tests** → Ensures the feeder dispenses the correct food portions consistently.  

---

## **Components Needed (Available at Jaycar or Online)**
| **Component** | **Purpose** | **Estimated Cost** |
|--------------|------------|-----------------|
| **Arduino Uno / Raspberry Pi** | Main controller | $30 - $80 |
| **Servo Motor (MG995 or similar)** | Controls food dispenser | $15 - $25 |
| **Ultrasonic Sensor (HC-SR04)** | Detects pet presence | $10 - $15 |
| **Load Cell + HX711 Module** | Measures food weight for portion control | $20 - $30 |
| **Wi-Fi Module (ESP8266 for Arduino / Built-in for Raspberry Pi)** | Enables mobile app control | $10 - $20 |
| **LED Display / OLED Screen** | Displays status updates | $15 - $25 |
| **Push Buttons** | Manual override for food dispensing | $5 - $10 |
| **3D Printed or Acrylic Food Container** | Holds pet food | Variable (DIY or $20+) |
| **Power Supply (Battery Pack / Adapter)** | Powers the system | $15 - $25 |

Estimated total: **$120 - $200** (Can be reduced by using available components)

---

## **System Design & Implementation**

### **1. System Workflow**
```
User Input (App/Button) → Microcontroller → Servo Motor Dispenses Food → Load Cell Verifies Portion → Confirmation Sent to UI
```

### **2. Software & Algorithm Development**
#### **Pseudocode: Closed-Loop Food Dispensing Algorithm**
```
BEGIN
    SET scheduled_feeding_times
    WHILE system is ON
        IF current_time matches feeding_time OR manual button pressed THEN
            DISPENSE food (rotate servo motor)
            MEASURE weight (load cell sensor)
            IF weight < target THEN
                DISPENSE more food
            ELSE
                STOP dispensing
            SEND notification to UI
    WAIT for next feeding cycle
END
```

#### **Python Code: Servo Motor Control for Food Dispensing**
```python
import RPi.GPIO as GPIO
import time

SERVO_PIN = 18
GPIO.setmode(GPIO.BCM)
GPIO.setup(SERVO_PIN, GPIO.OUT)
servo = GPIO.PWM(SERVO_PIN, 50)
servo.start(0)

def dispense_food():
    print("Dispensing food...")
    servo.ChangeDutyCycle(7)  # Rotate servo to open container
    time.sleep(1)
    servo.ChangeDutyCycle(0)  # Stop rotation
    print("Food dispensed.")

try:
    dispense_food()
finally:
    servo.stop()
    GPIO.cleanup()
```

---

### **3. Prototyping & Simulation**
- **Software Simulation:** Use Tinkercad or Proteus to simulate Arduino-based circuits before physical testing.
- **3D Modeling:** Design food container parts using **Fusion 360** or **TinkerCAD**.
- **Testing Environment:** Use small food samples to test different dispensing amounts.

---

### **4. UI Development for Remote Control**
A simple **web-based or mobile UI** allows users to:
- **Schedule feeding times**.
- **Manually dispense food**.
- **View feeding logs and portion data**.

#### **Example: Flask API for UI Control**
```python
from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/dispense', methods=['POST'])
def dispense():
    # Trigger servo motor (integrate with hardware)
    return jsonify({"status": "Food dispensed"})

if __name__ == '__main__':
    app.run(debug=True)
```
- The UI **sends a request to `/dispense`**, triggering the food dispensing algorithm.

---

### **5. Unit Testing & Validation**
To ensure **accuracy and repeatability**, write unit tests for:
✅ **Sensor Readings** – Test if the ultrasonic sensor detects a pet accurately.  
✅ **Motor Functionality** – Verify that the servo motor dispenses food correctly.  
✅ **Weight Accuracy** – Check if the load cell correctly measures portion size.  

#### **Example: Unit Test for Weight Sensor (Python)**
```python
import unittest

def measure_weight():
    return 50  # Simulated weight reading (grams)

class TestWeightSensor(unittest.TestCase):
    def test_weight_measurement(self):
        self.assertEqual(measure_weight(), 50)  # Expected portion size

if __name__ == '__main__':
    unittest.main()
```