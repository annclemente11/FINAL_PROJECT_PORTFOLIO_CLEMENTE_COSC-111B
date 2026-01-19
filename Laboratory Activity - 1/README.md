🚦 Laboratory Activity 1: Working with Digital Signals

🧠 Overview
Laboratory Activity 1 explores the fundamentals of digital signal control using the Arduino Uno. Through a visually engaging running light circuit, this activity demonstrates how microcontrollers communicate with hardware using digital outputs, timing, and programmed logic.

By sequentially turning LEDs ON and OFF, this experiment transforms abstract digital concepts into a clear, observable process—making it an ideal starting point for students entering the world of embedded systems and IoT development.

🎯 Objectives
- Understand the use of Arduino as a basic device for IoT projects
- Learn how to control digital output pins using Arduino

🧰 Hardware Used
- Arduino Uno
- 5 LEDs
- Resistors
- Breadboard
- Jumper wires

⚙️ Implementation Details
The running light effect is achieved by assigning each LED to a specific digital pin and controlling them programmatically using loops and delays.

🔌 Circuit Configuration
LEDs are connected to digital pins 8 through 12
Each LED is paired with a current-limiting resistor
Components are mounted on a breadboard for easy modification

🔄 Program Logic
LEDs turn ON sequentially from pin 12 down to pin 8
Once all LEDs are ON, they turn OFF in the same order
A 1-second delay is applied between each step for clear visual feedback

🧩 Code Structure
setup() function
Initializes all LED pins as OUTPUT
loop() function
🔁 One loop to turn LEDs ON sequentially
🔁 One loop to turn LEDs OFF sequentially
