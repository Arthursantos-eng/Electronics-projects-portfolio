# WiFi-Controlled Smart RGB Lamp

## Overview
A cloud-controlled RGB lighting system using Arduino Uno and Particle Argon. Color values are transmitted over WiFi and displayed locally through PWM-based LED mixing.

## Hardware
- Arduino Uno
- Particle Argon
- 3x individual LEDs (R,G,B)
- 4-pin RGB LED
- Breadboard & resistors

## Architecture
Smartphone → Particle Cloud → Argon → UART (SoftwareSerial) → Arduino → LEDs

## Features
- Real-time RGB color control
- UART communication between microcontrollers
- SoftwareSerial implementation
- Parallel output mirroring to blended RGB LED

## Skills Demonstrated
- Multi-microcontroller communication  
- PWM color mixing  
- Serial protocol debugging  
- Hardware-software co-design

## Media
<img width="305" height="422" alt="image" src="https://github.com/user-attachments/assets/d39014a1-ae74-417c-a1ff-d29dfc0308bc" /> <img width="378" height="406" alt="image" src="https://github.com/user-attachments/assets/1b6020dc-ef22-4e28-81a6-124329f7cc79" /> 

## Code 
-Arduino UNO Code

  <img width="410" height="395" alt="image" src="https://github.com/user-attachments/assets/a8624f4b-81e4-4684-8338-6c1075ffb128" />

-Photon 1 Code

<img width="300" height="125" alt="image" src="https://github.com/user-attachments/assets/a9397537-8d5b-41be-b45a-c398618e3975" /> 







