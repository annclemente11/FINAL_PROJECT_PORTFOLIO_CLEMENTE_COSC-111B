### Laboratory Activity No. 3  
*Title:* Working with Sensors  

***

#### I. Description  
This laboratory activity introduces the use of *sensor components* commonly utilized in *IoT (Internet of Things)* applications. It demonstrates how multiple sensors can be integrated into a single *Arduino-based circuit* to monitor environmental conditions. Specifically, the activity implements a simple *fire detection system* using a *thermistor* for temperature sensing and a *photoresistor (LDR)* for light intensity measurement. By combining data from these two sensors, the system illustrates how *real-world analog signals* can be processed and used by the Arduino to activate hardware-based alert mechanisms.  

***

#### II. Objectives  
1. To familiarize students with basic sensor components used in IoT systems.  
2. To integrate multiple sensor components within an Arduino circuit.  
3. To design and implement a simple fire detection system.  

***

#### III. Concepts Applied  
- *Analog Sensor Data Acquisition:* Reading real-world environmental parameters through Arduino’s analog input pins.  
- *Thermistor Temperature Measurement:* Calculated using the *Beta parameter equation* to estimate real-time temperature.  
- *Light Intensity Sensing:* Utilized through a *photoresistor (LDR)* that detects variations in light levels.  
- *Threshold-Based Logic:* Decision-making process based on predefined threshold values for temperature and light intensity.  
- *Function Modularization:* Separating sensor-reading logic into functions for organized and readable code.  
- **Use of #define and const:** For defining pin assignments and maintaining fixed threshold constants.  
- *Digital Output Control:* Activating alert mechanisms such as LEDs based on conditional evaluations.  

***

#### IV. System Behavior  
- *Sensors Used:*  
  - *Thermistor:* Connected to *Analog Pin A0* for temperature sensing (°C).  
  - *Photoresistor (LDR):* Connected to *Analog Pin A2* for measuring ambient light intensity.  

- *Program Logic:*  
  - Each sensor reading is processed using dedicated functions for modular program design.  
  - The system continuously monitors both temperature and light levels.  
  - When *both temperature and light intensity exceed their predefined thresholds*, a *fire condition* is detected.  

- *Alert Mechanism:*  
  - An *LED connected to Digital Pin 12* blinks rapidly to indicate a potential fire event.  
  - This setup demonstrates how multiple sensor inputs can work in combination to generate real-time system responses.  

***

#### V. Circuit Diagram and Wiring  
*Components:*  
- Arduino Uno  
- Thermistor (Temperature Sensor)  
- Photoresistor (LDR)  
- 1 LED Indicator  
- 220Ω resistor (for LED)  
- Breadboard and connecting wires  

*Connection Setup:*  
| Component | Arduino Pin | Description |
|------------|--------------|--------------|
| Thermistor | A0 | Measures temperature in °C |
| Photoresistor (LDR) | A2 | Measures ambient light intensity |
| LED Indicator | D12 | Alerts using rapid blinking pattern |
| GND | — | Common ground for all components |
| Power Source | USB / 5V | Powers the entire circuit |

*Design Notes:*  
- The circuit supports *modular testing*, allowing independent validation of each sensor.  
- All sensor readings can be observed via the Serial Monitor for calibration and debugging.  

***
