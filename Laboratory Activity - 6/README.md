### Laboratory Activity No. 6  
*Title:* Bidirectional Control Using Arduino and Python  

***

#### I. Description  
This laboratory activity demonstrates *bidirectional serial communication* between an *Arduino microcontroller* and a *Python application*. It establishes a two-way data exchange system where input signals from Arduino (via push buttons) are transmitted to Python, and Python, in turn, responds with control commands that influence Arduino outputs. The system functions as a complete *feedback loop*, simulating an interactive *IoT communication model* with near real-time data flow. This setup showcases the core principles of *computer–hardware integration*, *synchronous control*, and *low-latency data exchange* in modern IoT systems.  

***

#### II. Objectives  
1. To understand and implement Arduino Serial communication protocols.  
2. To utilize *Python* for serial data reception and command transmission.  
3. To design and implement *real-time bidirectional communication* between Arduino and Python.  

***

#### III. Concepts Applied  
- *Serial Communication:* Implemented using Serial.begin(), Serial.println(), and Serial.readStringUntil() for data transmission and reception.  
- *Digital Input Handling:* Capturing input signals from push buttons to trigger specific actions or data output.  
- *Edge Detection:* Identifying discrete button press events to ensure accurate signal interpretation.  
- *State-Based LED Control Logic:* Updating LED states based on received data from Python.  
- *Bidirectional Data Exchange:* Continuous feedback between Arduino and Python to maintain system synchronization.  
- *Python Serial Interface:* Using the *PySerial* library for communication, monitoring, and control operations.  
- *Low-Latency Feedback:* Ensures responsive interaction, enabling sub-second roundtrip communication between hardware and software.  

***

#### IV. System Behavior  

*Hardware Components:*  
- *Inputs:* Three push buttons.  
- *Outputs:* Three LEDs – Red, Green, and Blue.  

*Outbound Communication (Arduino → Python):*  
1. Each button press triggers Arduino to send a unique character via Serial:  
   - Button 1 → R  
   - Button 2 → G  
   - Button 3 → B  
2. At this stage, Arduino acts as the *data transmitter* and does not directly alter LED states.  

*Inbound Communication (Python → Arduino):*  
1. The Python script continuously listens for incoming serial characters.  
2. Upon detecting a specific character, Python sends back a corresponding signal:  
   - R received → Python sends 1  
   - G received → Python sends 2  
   - B received → Python sends 3  
3. Arduino interprets the returned value and toggles the corresponding LED:  
   - 1 → Toggle *Red LED*  
   - 2 → Toggle *Green LED*  
   - 3 → Toggle *Blue LED*

*System Outcome:*  
- The setup achieves real-time, *bidirectional communication* between Python and Arduino.  
- Each button press on the Arduino triggers reactive behavior on both ends, forming a *closed-loop system*.  
- The system operates with an average response latency of *less than one second*, ensuring smooth and synchronized interaction.  

***

#### V. Circuit Diagram and Wiring  

*Components:*  
- Arduino Uno  
- 3 Push buttons (inputs)  
- 3 LEDs (Red, Green, Blue outputs)  
- 3 × 220Ω resistors  
- Breadboard and jumper wires  

*Wiring Connections:*  
| Component | Arduino Pin | Type | Description |
|------------|--------------|------|-------------|
| Button 1 | D2 | Input | Sends signal “R” when pressed |
| Button 2 | D3 | Input | Sends signal “G” when pressed |
| Button 3 | D4 | Input | Sends signal “B” when pressed |
| Red LED | D8 | Output | Controlled by command 1 |
| Green LED | D9 | Output | Controlled by command 2 |
| Blue LED | D10 | Output | Controlled by command 3 |
| GND | — | — | Common ground for buttons and LEDs |

*Power and Communication:*  
- The *Arduino Uno* is powered via USB, which simultaneously provides the *Serial communication interface* for the Python program.  

***
