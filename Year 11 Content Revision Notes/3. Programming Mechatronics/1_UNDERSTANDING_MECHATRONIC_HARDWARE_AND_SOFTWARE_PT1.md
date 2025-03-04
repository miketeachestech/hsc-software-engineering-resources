# Understanding Mechatronic Hardware and Software Part 1 - HSC Software Engineering Revision Notes

## 1. Applications of Mechatronic Systems in Specialised Fields
Mechatronic systems combine **mechanical, electronic, and software components** to automate and improve efficiency in various industries.

### **Examples of Mechatronic Applications**
| **Field** | **Application** |
|-----------|----------------|
| **Medical** | Robotic-assisted surgery (e.g., Da Vinci Surgical System) |
| **Automotive** | Autonomous vehicles (self-driving cars) |
| **Manufacturing** | Industrial robots in assembly lines (e.g., robotic arms) |
| **Agriculture** | Automated harvesting machines, drone-based crop monitoring |
| **Aerospace** | Fly-by-wire aircraft systems, autopilot technologies |
| **Defense** | Military drones, robotic bomb disposal units |
| **Consumer Electronics** | Smart home devices (e.g., automated vacuum cleaners, AI assistants) |

---

## 2. Hardware Requirements to Run a Program and Its Effect on Code Development
Understanding hardware constraints is essential for **optimizing software and ensuring compatibility** with mechatronic systems.

### **2.1 Relationship Between Microcontrollers and the CPU**
- **Microcontrollers**: Small, embedded processors designed for **specific tasks** (e.g., controlling sensors and actuators in robots).
- **CPU (Central Processing Unit)**: More powerful processors that handle **complex calculations and multitasking** in computers and advanced mechatronic systems.
- **Comparison:**
  - **Microcontrollers** (e.g., Arduino, ESP32) have **low power usage** and handle **real-time control tasks**.
  - **CPUs** (e.g., Intel, AMD) execute **multiple instructions per second** and are optimized for **high-speed processing**.

### **2.2 Influence of Instruction Set and Opcodes**
- **Instruction Set**: Defines what operations a processor can execute.
- **Opcodes**: Machine code instructions that tell the processor what to do.
- **Example:** Different processors have different **instruction sets** (e.g., ARM vs. x86), which affects how software is written and compiled.
- **Effect on Code Development:**
  - Low-level programming (e.g., Assembly) must be optimized for a processor’s instruction set.
  - Higher-level languages (e.g., Python, C++) abstract these details for easier coding.

### **2.3 Use of Address and Data Registers**
- **Registers**: Small memory locations inside a CPU/microcontroller that store temporary data.
- **Address Registers**: Store memory addresses for **fetching instructions and data**.
- **Data Registers**: Hold values currently being processed.
- **Example:**
  - A robotic arm microcontroller fetches sensor data using address registers and stores calculations in data registers for fast execution.

---

## 3. Sensors, Actuators, and End Effectors in Mechatronic Systems
Mechatronic systems rely on **sensors** (to detect changes), **actuators** (to produce movement), and **end effectors** (to interact with objects).

### **3.1 Sensors**
| **Sensor Type** | **Function** | **Example Application** |
|---------------|------------|-------------------|
| **Motion Sensors** | Detect movement | Automatic doors, security systems |
| **Light Level Sensors** | Measure brightness | Street lighting automation, solar panels |
| **Temperature Sensors** | Monitor heat changes | Air conditioning systems, industrial monitoring |
| **Proximity Sensors** | Detect nearby objects | Parking sensors, collision avoidance in robots |

#### **Example: Motion Sensor in a Security System (Python Code)**
```python
import time
import RPi.GPIO as GPIO

PIR_SENSOR = 4  # GPIO pin
GPIO.setmode(GPIO.BCM)
GPIO.setup(PIR_SENSOR, GPIO.IN)

print("Monitoring motion...")
while True:
    if GPIO.input(PIR_SENSOR):
        print("Motion detected!")
    time.sleep(1)
```

---

### **3.2 Actuators**
| **Actuator Type** | **Function** | **Example Application** |
|---------------|------------|-------------------|
| **Hydraulic Actuators** | Use fluid pressure to generate force | Construction machinery, robotic arms |
| **Pneumatic Actuators** | Use compressed air for movement | Industrial automation, vehicle brakes |
| **Electric Motors** | Convert electrical energy into motion | Conveyor belts, robotic joints |
| **Solenoids** | Convert electrical energy into linear motion | Door locks, fuel injectors |

#### **Example: Controlling a Motor with Python (Raspberry Pi)**
```python
import RPi.GPIO as GPIO
import time

MOTOR_PIN = 17  # GPIO pin
GPIO.setmode(GPIO.BCM)
GPIO.setup(MOTOR_PIN, GPIO.OUT)

print("Starting motor...")
GPIO.output(MOTOR_PIN, GPIO.HIGH)
time.sleep(3)
GPIO.output(MOTOR_PIN, GPIO.LOW)
print("Motor stopped.")
GPIO.cleanup()
```

---

### **3.3 End Effectors and Manipulators**
End effectors are **tools attached to robotic arms** that allow interaction with the environment.

| **End Effector Type** | **Function** | **Example Application** |
|----------------|------------|-------------------|
| **Robotic Grippers** | Grip and move objects | Warehouse automation, robotic surgery |
| **Suction Cups** | Pick up objects using vacuum force | Assembly lines, logistics sorting |
| **Welding Torch** | Automated welding | Car manufacturing, construction |
| **Paint Sprayers** | Apply coatings evenly | Automotive painting, industrial finishing |

#### **Example: Controlling a Robotic Gripper (Pseudocode)**
```
BEGIN
    SET gripper_position TO open
    WAIT FOR object detection
    CLOSE gripper TO pick object
    MOVE to destination
    OPEN gripper TO release object
END
```