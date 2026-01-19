### Laboratory Activity No. 2  
*Title:* Working with Analog Signals  

***

#### I. Description  
This laboratory activity explores the concept of *analog signals* and their practical application in an *Arduino-based circuit*. It builds upon Laboratory Activity No. 1 by extending digital signal control to *analog output modulation*, specifically varying LED brightness. The experiment applies *Pulse Width Modulation (PWM)* to demonstrate how analog values can represent signal intensities. Through this, students gain a foundational understanding of *analog-to-digital interfacing* and its importance in IoT systems that require fine control of hardware components.  

***

#### II. Objectives  
1. To discuss analog signals and their implementation in Arduino circuits.  
2. To understand the principles of analog-to-digital signal conversion and scaling.  

***

#### III. Concepts Applied  
- *Analog Signal Representation:* Continuous signal levels corresponding to varying voltage.  
- *Pulse Width Modulation (PWM):* Achieved using analogWrite() to control analog output levels.  
- *Array Utilization:* Arrays (int ledPins[5] = {8, 9, 10, 11, 12}) enable structured and efficient LED pin management.  
- *Iterative Control:* Implemented through while() loops for sequential brightness control.  
- *Sequential Logic Execution:* Ensures smooth transition of brightness across LEDs.  
- *Timing Control:* Managed using delay() to regulate brightness change timing.  

***

#### IV. System Behavior  
- *Pins Used:* Digital Pins 8, 9, 10, 11, and 12  
- *Control Method:* LED pin numbers are stored in an array for streamlined looping.  
- *Sequence Operation:*  
  - The program *gradually increases* LED brightness sequentially from Pin 12 → Pin 8 until the maximum analog value is reached.  
  - Once all LEDs are fully illuminated, the brightness *gradually decreases* from Pin 12 → Pin 8 back to zero.  
- *Visual Effect:*  
  The LEDs produce a smooth, flowing light pattern with varying brightness levels, demonstrating the continuous nature of analog output control.  
- *Control Logic:*  
  Arrays and iterative loops simplify LED sequencing, ensuring uniform brightness transition and efficient signal modulation.  

***

#### V. Circuit Diagram and Wiring  
*Components:*  
- Arduino Uno  
- 5 LEDs  
- 5 × 220Ω resistors  
- Breadboard and connecting wires  

*Connection Setup:*  
| Pin | Wire Color | LED | Connection |
|-----|-------------|-----|-------------|
| 8 | Orange | LED 1 | Through 220Ω resistor to GND |
| 9 | Yellow | LED 2 | Through 220Ω resistor to GND |
| 10 | Green | LED 3 | Through 220Ω resistor to GND |
| 11 | Blue | LED 4 | Through 220Ω resistor to GND |
| 12 | Red | LED 5 | Through 220Ω resistor to GND |

*PWM Control:*  
Brightness levels are regulated through analogWrite(), allowing smooth transitions rather than simple ON/OFF toggles as in the previous digital signal experiment.  

***
