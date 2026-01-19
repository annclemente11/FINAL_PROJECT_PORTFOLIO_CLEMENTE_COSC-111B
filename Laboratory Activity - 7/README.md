🌐🔌 Laboratory Activity #7: Controlling Arduino Using FastAPI

🧠 Overview

This demonstrates bi-directional control of an Arduino using Python and FastAPI, extending serial communication into the world of web-based APIs. In this project, Arduino hardware is controlled not only through the Serial Monitor, but also via HTTP requests handled by a FastAPI server.

Three LEDs—Red, Green, and Blue—serve as visual outputs and can be toggled using:

📟 Arduino Serial Monitor commands
🌐 FastAPI HTTP requests
🔘 Physical push buttons on the Arduino

At the same time, button presses on the Arduino send signals back to Python, enabling real-time two-way communication between hardware and a web-enabled application.

🎯 Objectives

- Implement Arduino Serial communication.
- Use Python to interface with Arduino via Serial.
- Control Arduino LEDs through an HTTP-based API using FastAPI.
- Enable bi-directional communication between Arduino and Python.

🧰 Hardware Used

- Arduino MCU
- 3 × LEDs (Red, Green, Blue recommended)
- 3 × Push Buttons
- Breadboard, Jumper Wires, Resistors
- Laptop with Python, pyserial, and FastAPI installed

🔌 Pin Configuration

Component	Arduino Pin

🔴 Red LED	7
🟢 Green LED	6
🔵 Blue LED	5
🔘 Button 1	12
🔘 Button 2	11
🔘 Button 3	10

⚙️ Implementation Details

- This system operates through two communication layers:

- Arduino ↔ Python (Serial) and Python ↔ Client (HTTP).

⬇️ Arduino Logic — Inbound Signals

Arduino listens for Serial commands sent from Python or FastAPI:
"1" → Toggle Red LED
"2" → Toggle Green LED
"3" → Toggle Blue LED

📌 Inputs are case-insensitive

⬆️ Arduino Logic — Outbound Signals
Push button presses send corresponding characters to Python:
🔘 Button 1 → 'R'
🔘 Button 2 → 'G'
🔘 Button 3 → 'B'

These signals are immediately processed by the FastAPI-backed Python application.

🌐 FastAPI API Endpoints
The FastAPI server exposes HTTP endpoints that translate web requests into Serial commands.

🎛️ LED Control Endpoints

POST /led/
- Toggle a single LED by color:
color = "red" → Sends "1" to Arduino
color = "green" → Sends "2" to Arduino
color = "blue" → Sends "3" to Arduino

POST /led/on
- Turns all LEDs ON

POST /led/off
- Turns all LEDs OFF

📡 All HTTP requests interact with Arduino in real time via Serial.

🧩 Key Concepts Demonstrated

- Bi-directional Serial communication between Arduino and Python
- Hardware control through an HTTP-based interface
- Real-time response handling (< 1 second)
- Case-insensitive command processing
- Integration of embedded systems with modern web frameworks
