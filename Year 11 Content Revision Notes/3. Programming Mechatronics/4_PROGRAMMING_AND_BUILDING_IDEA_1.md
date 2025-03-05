# Programming and Building Practice Idea 1 (Easier) - HSC Software Engineering Revision Notes

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

## **Suggested Project: MicroBit & Maqueen Obstacle Avoiding Robot**

### **Introduction**
This project will involve building an **obstacle-avoiding robot** using a **MicroBit microcontroller** and a **Maqueen vehicle base**. This is a great introduction to robotics, coding, and engineering for high school students with no prior experience.

By the end of this project, you will:
- ✅ Learn how to program the **MicroBit** to control a robot.  
- ✅ Understand how sensors help robots interact with their environment.  
- ✅ Use simple **block-based programming** (MakeCode) to write your first robot program.  
- ✅ Keep a **logbook** to track your progress, errors, and improvements.  

---

## **What You Need**
| **Component** | **Purpose** |
|--------------|------------|
| **BBC MicroBit** | The brain of the robot |
| **Maqueen Robot Base** | Provides motors, wheels, and chassis |
| **Ultrasonic Sensor** | Detects obstacles ahead |
| **Battery Pack** | Powers the MicroBit and Maqueen |

---

## **How the Robot Works**
1. The **ultrasonic sensor** measures the distance to objects in front of the robot.
2. The **MicroBit** reads this distance and decides whether the robot should move forward or turn.
3. The robot will **move forward** until it detects an obstacle **closer than 15cm**.
4. If an obstacle is detected, it **stops and turns** to find a clear path.

---

## **Step 1: Setting Up the Hardware**
1. Attach the **MicroBit** to the Maqueen robot base.
2. Connect the **ultrasonic sensor** to the Maqueen.
3. Insert the **battery pack** and turn on the power.

---

## **Step 2: Writing the Code (MakeCode)**
Use **MakeCode**, a block-based coding platform, to program the robot.

### **Basic Obstacle Avoidance Algorithm (MakeCode Blocks)**
1. Go to [MakeCode MicroBit](https://makecode.microbit.org/).
2. Create a new project.
3. Drag and drop the following blocks:
   - Start by continuously checking the **ultrasonic sensor**.
   - If the sensor detects an obstacle **closer than 15cm**, stop and turn.
   - If no obstacle is detected, move forward.

---

## **Step 3: Keeping a Logbook**
Keeping track of your progress is important! Here’s what to include:
- ✅ **Daily Entries** – What did you work on today? What worked well? What didn’t?  
- ✅ **Error Tracking** – Write down any issues and how you fixed them.  
- ✅ **Ideas & Improvements** – What changes would you make next time?  

Example Log Entry:
```
Date: March 6, 2025
What I did: Wrote code to make the robot move forward.
Problem: The robot wasn’t moving at all.
Solution: I forgot to upload the code! Once I uploaded it, it worked.
Next Steps: Add turning when an obstacle is detected.
```

---

## **Step 4: Testing & Improving Your Robot**
- 🔍 **Test your robot** – Does it avoid obstacles? Does it turn correctly?
- 🔧 **Debug your code** – If something doesn’t work, check your logbook and experiment with different solutions.
- 🎯 **Enhance your robot** – Can you add sound or lights when it detects an obstacle? Perhaps you could also make the robot follow a **line or track**?