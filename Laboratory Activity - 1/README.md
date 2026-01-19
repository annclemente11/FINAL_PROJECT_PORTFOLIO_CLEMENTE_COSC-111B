### Laboratory Activity No. 1  
*Title:* Working with Digital Signals  

***

#### I. Description  
This laboratory exercise focuses on controlling digital outputs using an *Arduino Uno*. The activity demonstrates the manipulation of digital signals through a sequence of five LEDs, which create a “running light” effect by illuminating in a forward and reverse order. The program illustrates transitions between digital *HIGH (5V)* and *LOW (0V)* states with one-second intervals, providing foundational insights into digital signal timing, sequencing, and control in IoT-based systems.

***

#### II. Objectives  
1. To review the use of Arduino as a platform for implementing Internet of Things (IoT) systems.  
2. To discuss the concept and application of digital signals in Arduino circuits.  

***

#### III. Concepts Applied  
- *Digital Signal States:*  
  - HIGH = 5V  
  - LOW = 0V  
- *pinMode(pin, OUTPUT):* Configures a specified pin as an output.  
- *digitalWrite(pin, HIGH/LOW):* Sets the digital output state of a pin.  
- *delay(ms):* Introduces a time delay, used here for signal synchronization.  
- *Sequential Programming:* Employed to achieve the LED chase (running light) effect.  
- *Breadboard Prototyping:* Utilizes 220Ω current-limiting resistors to protect LEDs.  

***

#### IV. System Behavior  
- *Pins Used:* 8, 9, 10, 11, and 12  
- *Forward Sequence:*  
  LEDs turn ON sequentially → Pin 8 → 9 → 10 → 11 → 12 (1-second interval per transition)  
- *Reverse Sequence:*  
  LEDs turn OFF sequentially → Pin 12 → 11 → 10 → 9 → 8 (1-second interval per transition)  
- *Cycle Duration:* Approximately 10 seconds (continuous loop)  
- *Visual Effect:* A left-to-right running light followed by a right-to-left dimming pattern.  

***

#### V. Circuit Diagram and Wiring  
*Components:*  
- Arduino Uno  
- 5 LEDs (Orange, Yellow, Green, Blue, Red)  
- 5 × 220Ω resistors  
- Breadboard and connecting wires  

*Wiring Connections:*  
| Pin | Wire Color | LED Color | Connection |
|-----|-------------|------------|-------------|
| 8 | Orange | — | Through 220Ω resistor to GND |
| 9 | Yellow | — | Through 220Ω resistor to GND |
| 10 | Green | — | Through 220Ω resistor to GND |
| 11 | Blue | — | Through 220Ω resistor to GND |
| 12 | Red | — | Through 220Ω resistor to GND |

***
