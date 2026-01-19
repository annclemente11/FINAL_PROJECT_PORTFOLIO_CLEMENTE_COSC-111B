🔥 Laboratory Activity 3: Fire Sensor Simulation Using Arduino

🧠 Overview
Laboratory Activity 3 presents a simulated fire detection system using the Arduino Uno and basic environmental sensors. By combining a thermistor for temperature monitoring and a photoresistor for light detection, the system evaluates surrounding conditions in real time.

When sensor readings exceed predefined safety thresholds, the Arduino triggers a visual alert, demonstrating how embedded systems can make decisions based on multiple inputs—a core concept in IoT-based safety and monitoring applications.

🎯 Objectives
- Gain familiarity with basic sensor components used in IoT systems
- Integrate multiple sensors in an Arduino circuit
- Implement threshold-based decision logic for fire detection

🧰 Hardware Used
- Arduino Uno
- Thermistor
- Photoresistor
- Red LED
- Resistors
- Breadboard and jumper wires

🔌 Pin Configuration

 Component and Arduino Pin
🌡️ Thermistor	Analog Pin A0
💡 Photoresistor	Analog Pin A2
🚨 Alert LED	Digital Pin 12

⚙️ Implementation Details
The system operates by continuously sampling environmental data and responding when conditions indicate a potential fire.

🔄 Sensor Monitoring
- Temperature data is read from the thermistor
- Light intensity is measured using the photoresistor
- Sensor values are continuously evaluated during program execution

📐 Data Processing
Temperature is calculated in degrees Celsius based on the thermistor’s resistance

Light intensity readings are compared against a predefined threshold to detect abnormal brightness

🚨 Alert Logic
- If temperature ≥ 50 °C and light intensity ≥ 220:
- A red LED blinks rapidly to signal a potential fire condition
- A buzzer is connected in parallel with the alert LED
- It activates simultaneously without requiring additional control logic

🧩 Code Structure
- Temperature calculations are encapsulated in a separate function
- Improves readability
- Enhances modularity and code organization
