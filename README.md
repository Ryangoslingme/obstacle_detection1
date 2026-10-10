# Obstacle Detection Using Python

## Project Overview
This project explores basic robotics obstacle-detection logic using Python and simulated sensor distance readings. It combines obstacle classification with consecutive-reading analysis to identify distance trends.

## Objectives
- Understand obstacle detection using conditional statements.
- Compare previous and current sensor readings.
- Detect whether an obstacle is getting closer, farther away, or remaining at the same distance.
- Determine an appropriate response based on the measured distance.

## Technologies Used
- Python
- Conditional statements (`if`, `elif`, `else`)
- Functions
- Lists and loops

## Obstacle Decision Logic

| Distance | Action |
|---|---|
| Below 15 cm | STOP |
| 15 cm to below 30 cm | SLOW |
| 30 cm to 50 cm | CAUTION |
| Above 50 cm | MOVE FORWARD |

## Sensor Trend Detection
The program compares consecutive distance readings:
- **Getting closer:** Current distance is lower than the previous distance.
- **Getting farther:** Current distance is higher than the previous distance.
- **Unchanged:** Both readings are equal.

## Example Sensor Readings
`[80, 65, 48, 52, 25, 25, 18, 10]`

The program analyzes the trend and selects an action for each current reading.

## Current Status
- Day 1: Basic obstacle-distance classification completed.
- Day 2: Sensor trend detection combined with obstacle-action decisions.

**Note:** The sensor readings are simulated. The program has not yet been connected to physical sensors or motors.

## Future Improvements
- Test the program with noisy sensor readings.
- Improve reliability of distance-based decisions.
- Explore integration with real sensors and motor-control hardware.
