# ROS2 Mobile Robot & 2-DoF Manipulator Simulation

##  Overview

This repository demonstrates the implementation of a complete robotic simulation pipeline using ROS2, including mobile robot modeling, manipulator integration, TF tree construction, and real-time control in simulation.

The system consists of:

* A differential-drive mobile robot (2 wheels + caster)
* A 2-DoF manipulator mounted on the mobile base
* Full simulation in Gazebo with visualization in RViz
* Real-time control via ROS2 topics

---

##  System Architecture

The project covers the full ROS2 workflow:

* URDF/Xacro-based robot modeling
* TF tree creation and broadcasting
* Robot State Publisher integration
* Gazebo simulation with physics (inertia, collision)
* ROS2 ↔ Gazebo bridge configuration
* Launch-based system orchestration

---

##  Technologies Used

* ROS2 (Humble)
* Gazebo (Fortress/Harmonic)
* RViz2
* URDF / Xacro
* TF2
* ros_gz_bridge
* YAML configuration
* Python-based ROS2 launch system

---

##  Features

* Modular robot modeling using Xacro (macros & properties)
* Complete TF tree for mobile base + manipulator
* Differential drive simulation
* 2-DoF manipulator modeling and integration
* Real-time control via:

  * `/cmd_vel` (mobile robot)
  * `/joint_states` (manipulator joints)
* Custom Gazebo world and object integration
* Camera sensor plugin integration
* Unified launch file for full system startup

---

##  Control

The robot can be controlled using ROS2 topics:

* Mobile base:

```bash
ros2 topic pub /cmd_vel geometry_msgs/msg/Twist ...
```

* Manipulator joints:

```bash
ros2 topic pub /joint_states sensor_msgs/msg/JointState ...
```

---

##  Simulation

The system is fully simulated in Gazebo and visualized in RViz:

* TF tree visualization
* Robot kinematic structure
* Real-time movement and interaction

---

##  What I Learned

* ROS2 node, topic, service architecture
* TF tree design and debugging
* URDF/Xacro modular robot modeling
* Launch system configuration
* Gazebo simulation pipeline
* Robot control using ROS2 topics
* Debugging ROS2–Gazebo integration issues

---

##  Disclaimer

This project is based on ROS2 courses from Udemy.

The implementation follows the course structure and guidance provided by the instructor.
The purpose of this repository is to demonstrate my understanding and hands-on implementation of ROS2 concepts, simulation workflows, and robotic system integration.

All credits for the original course structure belong to the instructor.

---

##  How to Run (Basic)

```bash
# Build workspace
colcon build

# Source
source install/setup.bash

# Launch simulation
ros2 launch <your_package> <your_launch_file>.launch.py
```

---

##  Media

(Add here)

* Gazebo simulation screenshots
* RViz TF tree
* Robot movement GIF/video

---
