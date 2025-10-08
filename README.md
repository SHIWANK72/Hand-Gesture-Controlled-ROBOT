# Hand-Gesture-Controlled-ROBOT
An Arduino-based robotic car controlled wirelessly by hand gestures, utilizing an MPU6050 accelerometer and gyroscope.
# Hand Gesture Controlled Robot with Arduino

This repository contains the code and documentation for a wireless gesture-controlled car. The project is a practical application of embedded systems, demonstrating real-time data processing from an IMU (Inertial Measurement Unit) to control a robotic vehicle.

## System Architecture
The system consists of two main parts: the transmitter (glove with sensor) and the receiver (the car). For this prototype, the system is integrated.

- **Sensing Unit**: An MPU6050 accelerometer and gyroscope reads the tilt and orientation of the hand.
- **Control Unit**: An Arduino UNO processes the raw sensor data to interpret it as a command (e.g., forward, left).
- **Actuation Unit**: An L298N motor driver receives signals from the Arduino to drive the DC motors of the car chassis.

## How It Works
1.  The MPU6050 continuously provides acceleration data for the X and Y axes.
2.  The Arduino reads this data via the I2C communication protocol. 
3.  A simple algorithm within the Arduino code translates the tilt direction into one of five commands: Forward, Backward, Left, Right, or Stop.
4.  The corresponding command is sent to the motor driver, which powers the motors accordingly.

## Key Learnings
This project provided hands-on experience with I2C communication, sensor data filtering and interpretation, and motor control logic. It was a valuable exercise in integrating hardware and software to create an intuitive human-machine interface.
