# 🦾 UR5 Pick & Place | CoppeliaSim
**Autonomous Robotic Manipulation using Lua & simIK**

This project implements a high-precision pick and place system using a **UR5 robotic arm** in the CoppeliaSim environment. It leverages **Inverse Kinematics (IK)** and scripted gripper control to perform seamless object manipulation.

---

## 🚀 Features
* **Smooth Motion:** Uses the `simIK` module for fluid trajectory planning.
* **Gripper Control:** Automated open/close cycles for the BarrettHand.
* **Intelligence:** Object parenting logic for secure "attach and detach" mechanics.
* **Collision-Safe:** Release protocols designed to avoid contact with bowl edges.

## 🛠️ Technologies Used
* **Simulator:** CoppeliaSim
* **Language:** Lua
* **Module:** simIK
* **Logic:** Linear Interpolation (Lerp) for movement smoothing.

## ⚙️ Operational Workflow
1.  **Approach:** The robot moves to a pre-calculated position above the cuboid.
2.  **Pickup:** Gripper closes and the cuboid is parented to the `attachPoint`.
3.  **Transfer:** The arm lifts and translates to the target coordinates above the bowl.
4.  **Placement:** The object is released inside the bowl, and the arm returns to **Home Position**.

## 🔧 Scene Requirements
To ensure the script runs correctly, the following objects must exist in your scene hierarchy:
* `/UR5` (Robot Base)
* `/Cuboid` (Target)
* `/Bowl` (Destination)
* `/UR5/BarrettHand` (End-Effector)
* `/UR5/attachPoint` (IK Tip)

## 📺 Simulation Demo
Watch the full operation here:  
**[YouTube Project Demo](https://youtu.be/P_COw3LUsKQ)**

---

## 🔮 Future Improvements
* Vision-based detection (OpenCV integration).
* Multi-object sorting and handling.
* Physical implementation on a real UR5 manipulator.

---

### 👨‍💻 Developed By
**Team:** Debuggers  
**Core Architect:** **Hitesh Rajpurohit**
