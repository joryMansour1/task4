
# ROS2 Turtlesim Project 🐢

## Overview
This project demonstrates how to use **ROS2** with the **Turtlesim** package to manually draw a shape (square) using keyboard controls.  
The process started by installing **Ubuntu 22.04 LTS** and **ROS2 Humble** on a virtual machine, then launching the turtle node and controlling it through the appropriate topic.

---

## Requirements
- **Ubuntu 22.04 LTS**
- **ROS2 Humble**
- `turtlesim` package installed

---

## Installation
After installing Ubuntu 22.04, ROS2 Humble was installed using the official ROS2 installation guide.  
The Turtlesim package was installed via:

```bash
sudo apt install ros-humble-turtlesim

—-

Running the Project

1. Launch the Turtle Node
source /opt/ros/humble/setup.bash
ros2 run turtlesim turtlesim_node

This node is responsible for launching the simulation window and displaying the turtle.

2. Control the Turtle
Open a new terminal and run:
source /opt/ros/humble/setup.bash
ros2 run turtlesim turtle_teleop_key

This node listens to keyboard inputs and sends movement commands to the topic /turtle1/cmd_vel.


Understanding Nodes and Topics
	•	Node: A process that performs a specific task in ROS2.
In this project:
	•	turtlesim_node → Displays the simulation and updates the turtle’s position.
	•	turtle_teleop_key → Reads keyboard input and sends movement commands.
	•	Topic: A communication channel between nodes.
In this project:
	•	/turtle1/cmd_vel → Receives velocity commands from turtle_teleop_key and applies them in turtlesim_node.

⸻

Drawing the Shape
	1.	Used the ↑ arrow key to move forward.
	2.	Used the ← arrow key to rotate 90 degrees.
	3.	Repeated the process 4 times to draw a square.
	4.	The final drawing appeared in the turtlesim_node simulation window.


Result

A perfect square was drawn manually using ROS2 and the Turtlesim package.
🔴Example result🔴:
[(img1.jpg)](https://github.com/joryMansour1/task4/blob/15a816a623fec229346466bf2b1785801bcdc311/img1.jpg)

Conclusion

This project showcases the basics of working with ROS2 using nodes and topics, and demonstrates how to interact with a graphical simulation through keyboard teleoperation.
