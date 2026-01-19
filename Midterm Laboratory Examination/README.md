💡 COSC 111B – MIDTERM EXAMINATION

🧠 Overview

This project implements a Smart Lighting System using an Arduino Uno, designed to automatically and manually adjust lighting indicators based on ambient light intensity measured through a photoresistor (LDR).

The system operates in two modes:

🤖 Automatic Mode

- Simulates real-world environmental lighting conditions—Cloudy, Normal, and Bright Sunlight—and activates the appropriate LED automatically based on predefined thresholds.

🧑‍💻 Manual Mode
- Allows the user to interactively configure light thresholds and control system behavior using Serial Monitor commands.

Three LEDs serve as visual indicators of light intensity:
🟢 Green → Low light
🟡 Yellow → Medium light
🔴 Red → High light

📌 At any given time, only one LED is active, ensuring clear and unambiguous system feedback.

🎯 Objectives
- Understand Arduino analog input and digital output.
- Implement sensor-based decision logic using thresholds.
- Learn Serial communication for interactive control.
- Simulate environmental conditions and automatic response.

🧰 Hardware Used
- Arduino Uno
- 1 × Photoresistor (LDR)
- 3 × LEDs (Green, Yellow, Red)
- Resistors
- Breadboard
- Jumper wires

🔌 Pin Configuration

Component	and Arduino Pin
🌞 Photoresistor	A0
🟢 Green LED	11
🟡 Yellow LED	12
🔴 Red LED	13

⚙️ Implementation Details

The system continuously reads ambient light values, processes them through threshold logic, and updates the LED output accordingly.

📟 Serial Monitor Output
- Every 1 second, the system displays real-time data:
- Light Intensity: xx%
- Active LED: Green / Yellow / Red
- Current Mode: Manual / Automatic
- Environment: Cloudy / Normal / Bright Sunlight (Automatic Mode only)

This continuous feedback ensures transparency and ease of monitoring.

🧩 Key Concepts Demonstrated
- Analog input reading using analogRead()
- LED control using digitalWrite()
- Threshold-based conditional logic
- Mode switching via Serial commands
- Dynamic environmental simulation
- Real-time system monitoring and data display
