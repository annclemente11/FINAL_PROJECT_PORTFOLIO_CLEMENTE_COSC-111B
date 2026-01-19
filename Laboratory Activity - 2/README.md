🌈 Laboratory Activity 2: Working with Analog Signals

🧠 Overview
Laboratory Activity 2 builds upon the digital running light experiment by introducing analog signal control. Rather than limiting LEDs to simple ON and OFF states, this activity leverages Pulse Width Modulation (PWM) to smoothly control LED brightness.

By gradually fading LEDs in and out, the Arduino simulates analog behavior using digital signals—demonstrating how microcontrollers handle real-world variations such as light intensity, speed, and voltage levels. The result is a visually fluid running light effect that highlights the power and flexibility of PWM-based control.

🎯 Objectives
- Understand the concept of analog signals and how they are represented in Arduino
- Learn how to adjust LED brightness using PWM and the analogWrite() function

🧰 Hardware Used
- Arduino Uno
- 5 LEDs
- Resistors
- Breadboard
- Jumper wires

⚙️ Implementation Details
This experiment enhances efficiency and readability by organizing LED control through arrays and loop-based logic.

🔌 Circuit Configuration
Five LEDs are connected to Arduino digital pins 8 to 12
Each LED is paired with a resistor to limit current
All components are assembled on a breadboard for clean wiring

🧠 Program Logic
LED pin numbers are stored in an array for simplified control
A loop is used to configure pin modes and manage LED sequencing

Each LED:
- Gradually increases brightness from 0 to 255 using analogWrite()
- Reaches maximum brightness
- Slowly dims back down to 0

A brief delay is applied between LED transitions to ensure smooth and observable fading
