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
![Lamp](lamp.jpg)
![Wiring](wiring.jpg)
