# Autonomous Obstacle-Avoiding Robot 

## Project Overview
This project implements an autonomous obstacle-avoidance robot using the e-puck robot in Webots. The robot uses proximity sensors to detect nearby obstacles and adjusts its wheel speeds to avoid collisions.

## Objectives
- Understand proximity sensors and obstacle detection.
- Implement decision-making using Python.
- Control robot movement through wheel-speed adjustments.
- Simulate autonomous navigation in Webots.

## Technologies Used
- **Simulator:** Webots
- **Programming Language:** Python
- **Robot:** e-puck
- **Concepts:** Proximity sensing, conditional logic, motor control, autonomous navigation

## How It Works
1. The robot reads values from its proximity sensors.
2. It compares the readings with a predefined threshold.
3. If an obstacle is detected, it changes its wheel speeds to turn away.
4. If no obstacle is detected, it continues moving forward.

## Algorithm
- Read proximity sensor values.
- Check whether the values exceed the obstacle-detection threshold.
- Determine the appropriate movement based on the sensor readings.
- Apply the calculated speeds to the left and right motors.

## How to Run
1. Install Webots.
2. Open a world containing the e-puck robot.
3. Assign the Python controller to the robot.
4. Place the controller code in the robot's controller folder.
5. Run the simulation and observe the robot's behavior.

## Current Status
**Working simulation prototype.**

The robot detects obstacles using proximity sensors and changes its movement in response. Further testing and improvements can help make navigation more reliable.

## Future Improvements
- Tune the sensor threshold using measured readings.
- Improve turning behavior and collision prevention.
- Test different obstacle positions and layouts.
- Record performance results and simulation demonstrations.

## Author
Robotics and Artificial Intelligence Engineering Student
