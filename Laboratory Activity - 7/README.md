### Laboratory Activity No. 7  
*Title:* Controlling Arduino Using FastAPI  

***

#### I. Description  
This laboratory activity focuses on establishing *real-time, bidirectional control* between an *Arduino microcontroller* and a *FastAPI-based web server*. The setup integrates *hardware inputs* (push buttons) and *software-driven HTTP requests*, allowing LEDs to be toggled either physically or via a web interface. This experiment models a modern *IoT architecture*, demonstrating seamless synchronization between *hardware events* and *API-based commands* for interactive device management.  

***

#### II. Objectives  
1. To implement Arduino Serial communication for hardware control.  
2. To utilize *Python* and *FastAPI* for developing HTTP endpoints that interact with the Arduino.  
3. To design a *bidirectional control system* integrating physical inputs with web-based command execution.  

***

#### III. Concepts Applied  
- *Serial Communication:* Establishing a continuous data link between Arduino and Python for sending and receiving control signals.  
- *Digital Input Handling:* Using push buttons to generate input events detected through digital pins.  
- *Edge Detection Logic:* Ensuring accurate LED state toggling by capturing discrete button press transitions.  
- *Digital Output Control:* Managing LED indicators through program-controlled digital outputs.  
- *HTTP Server Implementation:* Building an asynchronous web interface with *FastAPI* for issuing control commands.  
- *Request-to-Command Mapping:* Translating API calls into serial commands understood by the Arduino.  
- *State Synchronization:* Maintaining consistent LED states across both *hardware interactions* and *software API control*.  

***

#### IV. System Behavior  

##### A. Hardware Configuration  
*Components Used:*  
- *LEDs:* Red, Green, Blue  
- *Push Buttons:* Three — one for each LED  

*Pin Assignments:*  
| Component | Arduino Pin | Type | Description |
|------------|--------------|------|-------------|
| Red LED | D5 | Output | Toggles when /led/red API or button pressed |
| Green LED | D6 | Output | Toggles when /led/green API or button pressed |
| Blue LED | D7 | Output | Toggles when /led/blue API or button pressed |
| Button 1 | D10 | Input | Controls Red LED |
| Button 2 | D11 | Input | Controls Green LED |
| Button 3 | D12 | Input | Controls Blue LED |

***

##### B. Arduino Sketch Behavior  
- Continuously *reads push button inputs* to toggle each corresponding LED when pressed.  
- Listens for *incoming serial commands* from the FastAPI application.  
- Parses received characters and executes matching LED toggle actions.  
- Maintains synchronized LED states whether the trigger originates from physical inputs or software commands.  

***

##### C. FastAPI Application Behavior  
- Runs a local *HTTP server* that defines endpoints for real-time LED control.  
- Each endpoint sends a corresponding character command to the Arduino via *PySerial*.  

*Defined API Endpoints:*  
| Endpoint | Function | Description |
|-----------|-----------|-------------|
| /led/red | Toggle Red LED | Sends command to toggle the red LED |
| /led/green | Toggle Green LED | Sends command to toggle the green LED |
| /led/blue | Toggle Blue LED | Sends command to toggle the blue LED |
| /led/on | Turn all LEDs ON | Activates all LEDs simultaneously |
| /led/off | Turn all LEDs OFF | Deactivates all LEDs simultaneously |

- The FastAPI server ensures *state consistency* so that LED states remain synchronized even when toggled manually via buttons.  
- The interaction demonstrates the combination of *web-based control* and *physical input monitoring* in a unified IoT environment.  

***

#### V. Circuit Diagram and Wiring  

*Components:*  
- Arduino Uno  
- 3 LEDs (Red, Green, Blue)  
- 3 Push Buttons  
- 3 × 220Ω resistors  
- Breadboard and jumper wires  

*Wiring Configuration:*  
| Component | Connection | Description |
|------------|-------------|-------------|
| Red LED | Pin 5 → Resistor → GND | Indicator for Red toggle control |
| Green LED | Pin 6 → Resistor → GND | Indicator for Green toggle control |
| Blue LED | Pin 7 → Resistor → GND | Indicator for Blue toggle control |
| Button 1 | Pin 10 | Controls Red LED |
| Button 2 | Pin 11 | Controls Green LED |
| Button 3 | Pin 12 | Controls Blue LED |
| Power Supply | USB | Provides both power and serial data connection |

*System Operation:*  
The Arduino board operates interactively—users can control the LEDs either by pressing the buttons on the hardware or by sending HTTP requests to the FastAPI server. The system reflects *true bidirectional synchronization*, characteristic of IoT-enabled control systems.  

***
