### Midterm Laboratory Exam  
*Title:* Smart Lighting System Using Arduino  

***

#### I. Description  
This laboratory examination involves the development of a *smart lighting system* using an *Arduino Uno* that adapts to changing ambient light conditions. The system employs a *photoresistor (LDR)* to detect light intensity and utilizes *three LEDs* (green, yellow, and red) to represent *low*, *medium*, and *high* brightness levels. It operates in two modes — *manual* and *automatic* — enabling flexible control for simulated environmental conditions such as cloudy, normal daylight, or bright sunlight.  

Through this experiment, students gain practical experience in *sensor data processing*, *threshold-based control*, and *serial communication*, emphasizing the importance of responsive and context-aware system design in IoT applications.  

***

#### II. Objectives  
1. To read analog sensor data using a photoresistor (LDR).  
2. To implement LED indicators representing varying levels of light intensity.  
3. To switch between *manual* and *automatic* operation modes.  
4. To adjust light thresholds dynamically or manually via user commands.  
5. To display system readings and status updates using the Serial Monitor.  

***

#### III. Concepts Applied  
- *Analog Input Processing:* Reading sensor data through analogRead().  
- *Signal Mapping:* Scaling analog values to percentage representation using the map() function.  
- *Threshold-Based Control:* Activating LEDs based on defined or computed light level boundaries.  
- *Serial Communication:* Exchanging user commands and system feedback via Serial.print() and Serial Monitor.  
- *Command Parsing:* Using string functions such as startsWith() and substring() for structured command interpretation.  
- *Automatic Mode Logic:* Dynamically setting environmental thresholds based on pre-defined lighting profiles.  
- *Modular Programming Design:* Organizing functions for readability, maintainability, and logical flow.  

***

#### IV. System Behavior  

##### A. System Overview  
*Primary Components:*  
| Component | Arduino Pin | Function |
|------------|--------------|----------|
| Photoresistor (LDR) | A0 | Measures ambient light intensity |
| Green LED | D8 | Indicates low light level |
| Yellow LED | D9 | Indicates medium light level |
| Red LED | D10 | Indicates high light intensity |

The system continuously *reads light intensity values* in real time, processes the data, and activates the corresponding LED to provide intuitive *visual feedback* of environmental illumination.  

***

##### B. Modes of Operation  

*Manual Mode:*  
- The user defines custom *low* and *high* light thresholds via Serial Monitor commands.  
- LED activation is determined according to these manually set parameters.  

*Automatic Mode:*  
- The system automatically adjusts brightness thresholds according to preset environmental profiles.  

| Environment | Low Threshold (%) | High Threshold (%) |
|--------------|------------------|-------------------|
| Cloudy | 0–40 | — |
| Normal | 41–70 | — |
| Bright Sunlight | 71–100 | — |

This flexibility demonstrates context-driven behavior replicating real-world adaptive lighting systems.  

***

##### C. Serial Monitor Commands  

| Command | Description |
|----------|-------------|
| MODE AUTO | Switches the system to automatic mode. |
| MODE MANUAL | Switches the system to manual mode. |
| SET LOW xx | Sets the lower threshold (in %) for manual mode. |
| SET HIGH xx | Sets the upper threshold (in %) for manual mode. |
| Invalid Commands | System responds with Error: Wrong command. |

These commands are processed through the Serial Monitor, allowing dynamic system tuning during runtime.  

***

##### D. Runtime Behavior  
- The system outputs updates *every one second* to the Serial Monitor, including:  
  - *Current light intensity (%)*  
  - *Operating mode:* Manual or Automatic  
  - *Active LED indicator (Green, Yellow, or Red)*  
  - In *Automatic Mode*, the detected environment (*Cloudy*, *Normal*, or *Bright*)  

This feedback mechanism provides transparent system monitoring and reinforces the concept of *data-driven decision-making* in embedded systems.  

***

#### V. Circuit Diagram and Wiring  

*Components:*  
- Arduino Uno  
- Photoresistor (LDR) in voltage divider configuration  
- 3 LEDs (Green, Yellow, Red)  
- 3 × 220Ω resistors  
- Breadboard and jumper wires  

*Wiring Configuration:*  
| Component | Arduino Pin | Connection Details |
|------------|--------------|--------------------|
| LDR | A0 | Analog input (voltage divider) |
| Green LED | D8 | Through 220Ω resistor to GND |
| Yellow LED | D9 | Through 220Ω resistor to GND |
| Red LED | D10 | Through 220Ω resistor to GND |
| Power Supply | 5V USB | Provides power and Serial link to PC |

The entire system is powered through the USB connection, which also enables *Serial communication* with the Arduino IDE for command-based interaction and monitoring.  

***
