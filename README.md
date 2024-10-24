# Robot Arm Project

## Overview
This project involves the integration of a robotic arm with object detection capabilities, allowing the arm to interact with identified objects based on color. The system utilizes MoveIt for motion planning and control, while a custom script detects objects in the camera's view.

## Setup and Configuration

### MoveIt Setup
1. **Create Planning Groups**:
   - Configured planning groups for the robotic arm and gripper.
   
2. **Set End-Effector**:
   - Defined the gripper as the end-effector with the robotic arm as the parent group.
   
3. **Define Starting Pose**:
   - Established a basic starting pose for the arm and filled in the remaining MoveIt configurations for exporting.

### Object Detection
1. **Camera Positioning**:
   - Initially moved the robot arm out of the camera's view to avoid obstructions during detection.

2. **Color Detection**:
   - Implemented a script that uses RGB value ranges to classify objects as red or blue.

3. **Distance Calculation**:
   - Calculated the distance of objects from the camera by determining the center of bounding boxes around detected objects.
   - Used the image center to guide the arm's movements, ensuring as many objects as possible are captured in the frame.

4. **Camera Control**:
   - Utilized the calculated distances to adjust the camera's pan and tilt, maximizing object visibility.

## Getting Started
- Ensure all dependencies are installed and configured, including ROS and MoveIt.
- Connect the robot arm and camera to your system.
- Launch the MoveIt node and the object detection script to begin interacting with the environment.

## Usage
- Run the MoveIt configuration to plan and execute movements.
- Start the object detection script to identify and track objects in the camera's view.

## Future Improvements
- Enhance object detection algorithms to include more colors and shapes.
- Implement feedback mechanisms to refine object tracking and arm movement accuracy.
