# DC Motor with Quadrature Encoder

This repository contains a project demonstrating how to control a DC motor with a quadrature encoder using a microcontroller and a control algorithm.

## Project Overview

The project utilizes an Arduino Uno to read the current position of the DC motor through the quadrature encoder and adjusts the motor speed to follow a given setpoint. A PID control algorithm is employed to achieve this.

## Project Requirements

The project requires the following components:

- Arduino Uno
- 12V DC motor with quadrature encoder
- Motor driver (L298N)
- 12V power supply for the motor
- ROS Melodic installed on your computer

## Instructions for Running the Project

1. **Download and Extract:**
   - Download the repository as a `.zip` file and extract it.

2. **Set Up ROS Workspace:**
   - Open a terminal and navigate to your ROS workspace:
     ```bash
     cd ~/catkin_ws/
     cd src
     ```

3. **Create a New ROS Package:**
   - Create a new ROS package:
     ```bash
     catkin_create_pkg motor_driver rospy roscpp std_msgs
     cd motor_driver
     ```

4. **Copy Files:**
   - Copy the extracted contents of the `.zip` file into the `motor_driver` package directory.

5. **Upload Code to Arduino:**
   - Open the `inal.ino` file in the `src` folder and upload it to the Arduino Uno.

6. **Build the Workspace:**
   - In the terminal, build the workspace:
     ```bash
     cd ~/catkin_ws/
     catkin_make
     source devel/setup.bash
     ```

7. **Launch ROS Core:**
   - Start ROS core:
     ```bash
     roscore
     ```

8. **Run the Node:**
   - Open a new terminal and run:
     ```bash
     source devel/setup.bash
     roslaunch motor_driver package_fn.launch
     ```

A window displaying several graphs should appear if everything is set up correctly.
