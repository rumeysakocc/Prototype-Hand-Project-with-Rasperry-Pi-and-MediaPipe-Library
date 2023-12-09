## Mediapipe library

<img src="https://github.com/rumeysakocc/Prototype-Hand-Project-with-Rasperry-Pi-and-MediaPipe-Library/assets/115664157/db130cba-26e3-4be9-8a77-0bdae3513a6c" alt="images" align="right" width="500" height="300">
The Mediapipe library is an open source framework created by Google, used to create machine learning solutions.
One of the most common applications using Mediapipe is Multiple Hand Movement Detection:
Mediapipe can detect the movements of multiple hands at the same time.
It can also identify 21 landmarks on the hands. In this way, information such as hand shape, direction, angle, posture can be accessed. 
As can be seen below, the landmarks of each finger joint and hand regions are defined. 
With the x,y angle values of these points, we can bring the position of the hand into a state that our computer can understand.[1] 
In this project, the y values of the end points (TIP points) and the bottom points (MCP points) of the fingers are compared with the loops to determine whether the finger is closed or open. 

## !The reason for this is that the coordinate system in the Mediapipe Library is the opposite of the coordinate system in mathematics:
Mediapipe is related to image processing and images are stored and processed in a different way. In the mathematical coordinate system, the origin is usually located in the lower left corner or centre, and the direction of the y-axis is upwards. In images, however, the origin is usually in the upper left corner and the direction of the y-axis is downwards. This is a consequence of representing images as a matrix. In matrices, the index of the first row is zero, and the indices of subsequent rows increase. Therefore, the top row of the image is the zeroth row and the bottom row is the last row. This means that the y-axis is in the opposite direction. Since the Mediapipe library processes images in this way, the coordinate system is set accordingly.[2]

<img src="https://github.com/rumeysakocc/Prototype-Hand-Project-with-Rasperry-Pi-and-MediaPipe-Library/assets/115664157/420a6af5-36b5-40df-b30a-879be7d9e2cb" alt="images" width="1100" height="300">

# RUN
Always install the cooling fan before image processing on the Raspberry Pi. Make sure it has a good supply. If you get a "Low voltage warning Please check your power supply" warning, something is wrong with the supply. If a regulator is to be used, it must be connected to both the servos and the raspberry Pi from the ground and 5V pins to complete the circuit.


*Since there are 4 PWM ports on the Raspberry Pi, only 4 finger movements are provided. The thumb is not connected to the servos.*


https://github.com/rumeysakocc/Prototype-Hand-Project-with-Rasperry-Pi-and-MediaPipe-Library/assets/115664157/9f1d7567-8cbd-4ae0-b350-b0054281c4b0

# Requirements:

Raspberry Pi 4 

9V and 2 1.5V batteries (total 12V, for battery supply)

Regulator

USB camera

model hand

breadboard

4 servo motors

female to male cable 

female to female cable

# Author:
Rumeysa KOÇ

# References:
[1] https://developers.google.com/mediapipe/solutions/vision/hand_landmarker

[2] https://github.com/google/mediapipe/issues/3370

