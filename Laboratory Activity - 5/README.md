🐍🔌 Laboratory Activity 5: Arduino Serial Communication with Python

🧠 Overview

This activity bridges the gap between embedded hardware and software control by integrating Arduino Serial communication with a Python application. In this activity, students develop an Arduino sketch capable of interpreting serial commands and a Python script that sends those commands in real time.

Through this interaction, LEDs connected to the Arduino are controlled directly from a computer—demonstrating how higher-level programming languages can interface with microcontrollers to create responsive and interactive systems.

🎯 Objectives
- Understand and implement Arduino Serial communication
- Utilize Python as a tool to send and receive serial commands
- Create a circuit where LEDs can be controlled via Arduino and Python

🛠️ Instructions

Using the laboratory guide, implement the following requirements:
🧰 Components Required
- Arduino MCU
- 3 LEDs (Red, Green, Blue recommended)
- Standard components: wires, breadboard, resistors
- Laptop with Python and pyserial installed

🔌 Pin Assignments

LED Color	and Arduino Pin

🔴 Red	Pin 8
🟢 Green	Pin 9
🔵 Blue	Pin 10

⚙️ Arduino Sketch Requirements

The Arduino program must listen for Serial input and respond as follows:

Serial Command Mapping

- R / r → Toggle Red LED ON/OFF
- G / g → Toggle Green LED ON/OFF
- B / b → Toggle Blue LED ON/OFF
- A / a → Turn all LEDs ON
- O / o → Turn all LEDs OFF

Any other input → Return an error message

📌 All inputs must be case-insensitive

🐍 Python Script Requirements
The Python program serves as a continuous user interface for controlling the Arduino.

🖥️ Program Behavior

The script must be non-terminating and continuously display the following options:

[R] Red ON/OFF
[G] Green ON/OFF
[B] Blue ON/OFF
[A] All ON
[O] All OFF
(X) Exit

⌨️ Input Handling

Commands must follow the same logic as the Arduino sketch
- Input must be case-insensitive
- Entering X / x:
- Terminates the Python program cleanly

🧩 Key Concepts Demonstrated
- Arduino Serial communication and input handling
- Python interaction with Arduino via pyserial
- Controlling multiple outputs through serial commands
- Conditional logic and case-insensitive input processing
- Real-time integration of hardware and software
