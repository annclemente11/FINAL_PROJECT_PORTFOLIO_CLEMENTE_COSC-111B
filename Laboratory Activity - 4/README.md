### Laboratory Activity No. 4  
*Title:* Arduino Serial Connection  

***

#### I. Description  
This laboratory activity explores the use of *Arduino Serial Communication* to monitor sensor data and interact with hardware components through user commands. It integrates a *photoresistor (LDR)* for analog input and employs *Serial-based user interaction* to control LED behavior dynamically. Building on Laboratory Activity No. 3, this experiment demonstrates how *real-time sensor readings* can be transmitted and controlled via the Serial Monitor, allowing users to modify system states based on both *sensor-driven* and *command-driven* conditions.  

***

#### II. Objectives  
1. To understand and implement Arduino Serial communication.  
2. To use basic Serial functions for real-time data monitoring and control.  
3. To design a sensor-based circuit that can respond to Serial commands.  

***

#### III. Concepts Applied  
- *Serial Communication Functions:*  
  Utilization of Serial.begin(), Serial.print(), and Serial.readStringUntil() for data transmission and command reception.  
- *Analog Sensor Data Acquisition:*  
  Reading analog input using analogRead() to measure ambient light intensity.  
- *Signal Mapping:*  
  Using the map() function to scale analog sensor inputs into meaningful ranges for control logic.  
- *Threshold-Based Logic:*  
  Determining system responses based on previously defined sensor value limits.  
- *State Management:*  
  Implementing boolean flags to maintain LED status and memory of previous system states.  
- *String Processing:*  
  Handling Serial commands using case-insensitive string comparison for flexibility in user inputs.  
- *Digital Output Control:*  
  Implementing LED blinking sequences and state persistence via software control.  

***

#### IV. System Behavior  
- *Sensor Input:*  
  - The *photoresistor (LDR)* is connected to *Analog Pin A2* to measure ambient light intensity.  
  - The raw sensor values are processed through the map() function and displayed on the Serial Monitor in real time.  

- *LED Control:*  
  - An *LED connected to Digital Pin 8* serves as a visual alert indicator.  
  - When the mapped brightness exceeds a predefined threshold, the LED enters a *continuous blinking* state.  
  - The LED continues blinking even when brightness later drops below the threshold, maintaining its previous activation state.  

- *Serial Command Control:*  
  - The user can override the LED’s blinking behavior by entering a specific *Serial command* (e.g., “STOP”) in the Serial Monitor.  
  - This illustrates *real-time control* of hardware through Serial input, combining automated sensor logic with manual user interaction.  

***

#### V. Circuit Diagram and Wiring  
*Components:*  
- Arduino Uno (USB connected)  
- Photoresistor (LDR)  
- 1 LED with 220Ω resistor  
- Breadboard and jumper wires  

*Connection Setup:*  
| Component | Arduino Pin | Description |
|------------|--------------|-------------|
| Photoresistor (LDR) | A2 | Measures light intensity |
| LED Indicator | D8 | Blinks based on sensor reading or Serial command |
| GND | — | Common ground for sensor and LED |
| Power Supply | USB (5V) | Provides power and Serial interface |

*Interface:*  
- Data communication and hardware interaction are monitored via the *Serial Monitor* in the Arduino IDE.  

***
