# Smart-Lighting-System
Project Overview
This project demonstrates a simple yet effective smart lighting system that combines an LDR (Light Dependent Resistor) and a PIR (Passive Infrared) motion sensor to control a bulb. The system ensures energy efficiency by turning on the bulb only when motion is detected and the ambient light level is below a certain threshold. This smart lighting solution is ideal for use in corridors, rooms, or outdoor areas where automatic lighting control is required.

The code provided is written in Arduino IDE and uses basic electronic components like an LDR, PIR sensor, and an LED bulb (or relay-controlled bulb). It is designed to be beginner-friendly while showcasing practical applications of sensors in IoT-based systems.

Features
Motion Detection : The PIR sensor detects human movement in its range.
Ambient Light Sensing : The LDR measures the ambient light intensity.
Smart Control Logic : The bulb turns on only if:
Motion is detected AND
The ambient light level is above a defined threshold (Frequency).
Serial Monitoring : Real-time data from the sensors is displayed on the Serial Monitor for debugging and monitoring purposes.
Components Used
The following components are used in this project:

Arduino Board (e.g., Arduino Uno)
LDR (Light Dependent Resistor) : To measure ambient light levels.
PIR Sensor : To detect motion.
LED Bulb or Relay Module : Acts as the bulb controlled by the system.
Resistors :
10kΩ resistor for the LDR voltage divider circuit.
Appropriate resistors for the PIR sensor (if needed).
Breadboard and Jumper Wires : For connections.
Circuit Diagram
Below is the circuit diagram for the project. It illustrates how the components are connected to the Arduino board:



Note: Replace images/circuit_diagram.png with the actual path to your circuit diagram image.

How It Works
PIR Sensor :
Detects motion and outputs a digital signal (HIGH or LOW) to the Arduino.
When motion is detected, the output is HIGH.
LDR Sensor :
Measures the ambient light intensity using a voltage divider circuit.
Outputs an analog value between 0 and 1023, which corresponds to the light level.
Logic Implementation :
If motion is detected (motion == 1) and the light level is above the threshold (light > Frequency), the bulb is turned on.
Otherwise, the bulb remains off.
Serial Monitor :
Displays real-time data such as the LDR value and motion detection status for debugging.
Code Explanation
Key Variables:
LDR_pin: Analog pin connected to the LDR sensor.
PIR_pin: Digital pin connected to the PIR sensor.
BULB_pin: Digital pin controlling the bulb.
Frequency: Threshold value for the light level.
Setup Function:
Initializes serial communication at 9600 baud rate.
Configures pin modes for input/output.
Loop Function:
Reads the PIR sensor and LDR sensor values.
Implements the logic to control the bulb based on motion and light level.
Prints sensor readings and motion status to the Serial Monitor.
Images of the Project
Below are images of the completed project:

Prototype Setup :

Close-Up of Connections :

Final Working Model :

Note: Replace images/prototype.jpg, images/connections.jpg, and images/working_model.jpg with the actual paths to your project images.

Applications
Home Automation : Automatically turn on lights in hallways, bathrooms, or basements.
Security Systems : Illuminate areas when motion is detected at night.
Energy Saving : Prevent unnecessary power consumption by ensuring lights are only on when needed.
Future Improvements
WiFi Connectivity : Integrate an ESP8266 or ESP32 module to enable remote monitoring and control via a smartphone app.
Advanced Threshold Adjustment : Allow dynamic adjustment of the light threshold (Frequency) through a potentiometer or mobile app.
Data Logging : Log sensor data to an SD card or cloud platform for analysis.
Multi-Zone Control : Expand the system to control multiple bulbs in different zones
