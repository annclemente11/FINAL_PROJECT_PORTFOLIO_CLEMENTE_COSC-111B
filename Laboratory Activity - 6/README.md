🔁🔌 Laboratory Activity 6: Bidirectional Control Using Arduino and Python

🧠 Overview
This showcases bidirectional serial communication between Arduino and Python, enabling real-time two-way interaction between hardware and software. In this activity, push buttons connected to the Arduino send signals to a Python program, which then responds with commands that control LEDs on the Arduino.

This experiment highlights how embedded systems and software applications can communicate continuously—listening, responding, and reacting within fractions of a second.

🎯 Objectives
- Understand and implement Arduino Serial communication
- Use Python to interact with Arduino in a bidirectional manner
- Create a circuit that allows real-time two-way control between Arduino and Python

🧰 Components Required
- Arduino MCU
- 3 LEDs (Red, Green, Blue recommended)
- 3 Push Buttons
- Standard components: wires, breadboard, resistors
- Laptop with Python and pyserial installed

🔌 Pin Assignments
💡 LEDs
LED Color	and Arduino Pin

🔴 Red	Pin 7
🟢 Green	Pin 6
🔵 Blue	Pin 5

🔘 Push Buttons
Button and Arduino Pin
Button 1	Pin 12
Button 2	Pin 11
Button 3	Pin 10

⚙️ Implementation Details

This system operates in two communication directions: Arduino → Python and Python → Arduino.

⬆️ Arduino Sketch — Outbound Signals (Button Presses)

When a push button is pressed, the Arduino sends a single character to Python via Serial:

🔘 Button 1 → sends 'R' once
🔘 Button 2 → sends 'G' once
🔘 Button 3 → sends 'B' once

📌 During button presses:
❌ No LED actions occur on the Arduino
📤 Arduino acts strictly as a signal transmitter
⬇️ Arduino Sketch — Inbound Signals (Serial Commands)

Arduino listens for Serial commands sent from Python and responds as follows:

Receiving "1" → Toggle Red LED ON/OFF
Receiving "2" → Toggle Green LED ON/OFF
Receiving "3" → Toggle Blue LED ON/OFF

📌 Inputs are case-insensitive

🐍 Python Script Behavior
- The Python program acts as the decision-making controller.
- Runs as a non-terminating script
- Continuously monitors incoming Serial data from Arduino

When button signals are received:
'R' → Python sends "1" to Arduino
'G' → Python sends "2" to Arduino
'B' → Python sends "3" to Arduino

⏱️ Response time must be less than 1 second to ensure real-time interaction

🧩 Key Concepts Demonstrated
- Bidirectional Serial communication between Arduino and Python
- Handling outbound signals (Arduino → Python)
- Handling inbound signals (Python → Arduino)
- Real-time LED control through external software
- Event-driven programming and responsiveness
- Hardware–software integration in IoT systems
