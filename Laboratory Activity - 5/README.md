### Laboratory Activity No. 5  
*Title:* Receiving Serial Connection Using Arduino from Python  

***

#### I. Description  
This laboratory activity explores *serial communication* between a *Python application* and an *Arduino microcontroller*, highlighting real-time interaction between software and hardware. In this setup, Python transmits user commands through a serial port to control the Arduino’s connected LEDs. The system enables the user to toggle individual LEDs, activate all LEDs simultaneously, or turn them all off. Additionally, the Arduino provides *textual feedback* confirming each command. This experiment demonstrates the fundamental principles of *Python–hardware integration*, *real-time control*, and **bidirectional serial data exchange**—core concepts in IoT communication systems.  

***

#### II. Objectives  
1. To understand and implement bidirectional Arduino Serial communication.  
2. To use *Python* for sending commands and managing hardware interaction.  
3. To develop an *interactive LED control system* through serial command exchange.  

***

#### III. Concepts Applied  
- *Serial Communication (Arduino Side):* Implementation using Serial.begin(), Serial.available(), and Serial.read() for data handling.  
- *Command Parsing:* Employing case-insensitive input for easier execution of user commands.  
- *LED Control Logic:* Managing multiple LED states through digital output pins.  
- *Python Serial Interface:* Utilizing the *PySerial library* to transmit commands and read feedback.  
- *Menu-Driven Interaction:* Python script continuously accepts user input and updates LED behavior dynamically.  
- *Error Handling:* Detecting and responding to invalid or undefined user commands.  
- *Modular Programming:* Use of header file functions on the Arduino for clean and reusable LED control functions.  

***

#### IV. System Behavior  
- *Hardware Setup:*  
  - Arduino Uno connected to *three LEDs* (Red, Green, and Blue).  
  - USB serial communication established with a *Python program* operating through a COM port interface.  

- *System Operation:*  
  1. The Python application sends single-character commands to the Arduino over the serial connection.  
  2. The Arduino reads and interprets each command, performing corresponding LED actions.  
  3. The Arduino responds with text-based confirmation (e.g., “RED ON”, “ALL OFF”, or “ERR: UNKNOWN COMMAND”) displayed in both the Arduino Serial Monitor and Python terminal.  

- *Command Mapping (Python → Arduino):*  

  | Command | Function | Description |
  |:--------:|:----------|:-------------|
  | R / r | Toggle Red LED | Switches the red LED ON/OFF |
  | G / g | Toggle Green LED | Switches the green LED ON/OFF |
  | B / b | Toggle Blue LED | Switches the blue LED ON/OFF |
  | A / a | All LEDs ON | Turns all LEDs ON simultaneously |
  | O / o | All LEDs OFF | Turns all LEDs OFF simultaneously |
  | X / x | Exit | Terminates the Python control program |
  | Other | Error | Displays “ERR: UNKNOWN COMMAND” |

- *Interactive Feedback:*  
  Commands sent from Python trigger immediate visual feedback on the Arduino. The current LED states and corresponding confirmation messages are displayed in real time on both interfaces, emphasizing robust two-way communication between software and hardware.  

***

#### V. Circuit Diagram and Wiring  
*Components:*  
- Arduino Uno (USB connected for power and serial link)  
- 3 LEDs (Red, Green, Blue)  
- 3 × 220Ω resistors  
- Breadboard and jumper wires  

*Connection Setup:*  
| LED Color | Arduino Pin | Description |
|------------|--------------|-------------|
| Red | D8 | Connected to GND through 220Ω resistor |
| Green | D9 | Connected to GND through 220Ω resistor |
| Blue | D10 | Connected to GND through 220Ω resistor |
| USB Port | — | Provides both power supply and serial communication with Python |

*Control Interface:*  
The *Python script*, executed on a computer, communicates with the Arduino via the selected *COM port* using *PySerial* for real-time, bidirectional data exchange.  

***
