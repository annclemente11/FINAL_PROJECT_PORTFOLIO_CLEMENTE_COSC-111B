🌐🔗 COSC 111B – FINAL EXAMINATION

🧠 Overview

This project demonstrates a hardware-to-cloud communication bridge using Arduino, Python, and a remote HTTP API. A push button connected to the Arduino acts as the physical trigger, while Python serves as an intermediate client that translates hardware signals into web-based actions.

The Arduino itself does not interact with the API. Instead, it sends a clean, debounced signal via Serial communication to a Python program. The Python client then processes the input and sends an HTTP request to a predefined endpoint, which controls LEDs on another Arduino or IoT-enabled device.

This architecture reflects real-world IoT systems where microcontrollers delegate networking tasks to more capable software clients.

🎯 Objectives
- Understand Arduino Serial communication and push button handling.
- Implement software debouncing to avoid repeated signals.
- Use Python to interface with Arduino and send HTTP requests.
- Normalize serial input to ensure case-insensitive handling.
- Build a reliable, non-terminating system for IoT control.

🧰 Hardware Used
- Arduino MCU
- 1 × Push Button
- Breadboard, Jumper wires, Resistor
- Laptop with Python and pyserial installed

🔌 Pin Configuration

Component	and Arduino Pin
🔘 Push Button	e.g., 12
⏚ GND	GND
⚡ VCC	5V (through resistor if needed)

⚙️ Implementation Details
The system is divided into two clearly defined roles: Arduino (signal generation) and Python (signal processing & API interaction).

🔘 Arduino Requirements
- The Arduino is responsible solely for detecting button presses and sending a clean signal to Python.
- Detect valid push button presses
- Send one Serial signal per press
- Implement software debouncing to prevent repeated signals during long presses

🖥️ Terminal Feedback
For every valid interaction, the Python client displays:
- ✅ Group number received
- 🌐 Endpoint called
- 📡 API response (success or error)

📏 Behavior Rules
✔️ One button press = one API request
⛔ Long button presses must not generate repeated API calls
🧪 Serial input must be validated
- Invalid input produces an error message
- Valid input proceeds to API interaction
🔁 The system runs continuously without termination

🧩 Key Concepts Demonstrated
- 🔘 Push button input handling on Arduino
- 🧼 Software debouncing for clean, reliable signals
- 🔌 Arduino-to-Python communication via Serial
- 🌐 HTTP request automation using Python
- 🧠 Input validation and normalization
- IoT system design using an intermediate client architecture
