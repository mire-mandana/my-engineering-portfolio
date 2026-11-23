# PROJECT 01: AUTOMATIC STREET LIGHTING SYSTEM

## 1. Project Overview

The Automatic Street Lighting System is an embedded electronics project designed to control street lighting based on the intensity of surrounding light.

The system uses a Light Dependent Resistor (LDR) to detect changes in light intensity. An Arduino Uno processes the sensor readings and controls an LED to represent the streetlight.

## 2. Problem Statement

Traditional streetlights may remain ON during daylight hours, resulting in unnecessary energy consumption.

This project explores an automated solution that switches lighting according to environmental conditions.

## 3. Project Objectives

- Understand how an LDR works.
- Measure light intensity using an analogue input.
- Interface an electronic sensor with Arduino.
- Program automatic switching logic.
- Understand the relationship between hardware and software.
- Explore energy-saving lighting automation.

## 4. Components and Equipment

| Component | Function |
|---|---|
| Arduino Uno | Main controller |
| LDR | Detects light intensity |
| 10kΩ resistor | Forms voltage divider |
| LED | Represents the streetlight |
| 220Ω resistor | Limits LED current |
| Breadboard | Circuit assembly |
| Jumper wires | Electrical connections |

## 5. Engineering Principles

### Light Dependent Resistor (LDR)

An LDR is a light-sensitive resistor.

Its resistance changes according to the amount of light falling on its surface.

- Bright environment: Lower resistance.
- Dark environment: Higher resistance.

### Voltage Divider

The LDR and 10kΩ resistor form a voltage divider.

This produces a changing voltage that Arduino can measure through analogue pin A0.

### Analogue-to-Digital Conversion

Arduino reads the analogue voltage using analogRead(A0).

The reading ranges from 0 to 1023.

## 6. Circuit Connections

### LDR Voltage Divider

- One LDR terminal → 5V.
- Other LDR terminal → Arduino A0.
- 10kΩ resistor between A0 and GND.

### LED Connections

- Arduino digital pin D8 → 220Ω resistor.
- 220Ω resistor → LED anode (+).
- LED cathode (-) → GND.

## 7. System Operation

1. The LDR detects the surrounding light.
2. Arduino reads the sensor voltage through A0.
3. The program compares the reading with a predefined threshold.
4. When the environment becomes dark, the LED switches ON.
5. When sufficient light is detected, the LED switches OFF.

## 8. Programming

The project uses Arduino IDE and C++.

Main programming concepts:

- analogRead()
- digitalWrite()
- pinMode()
- if/else conditions
- Serial.begin()
- Serial.println()

## 9. Simulation and Testing

The system was tested by observing sensor readings through the Serial Monitor.

A reading of 728 was observed during one test using a threshold of 800, triggering the programmed dark-condition message.

Further LED output testing was necessary because the LED did not initially illuminate as expected.

## 10. Challenges Encountered

- Understanding the relationship between LDR resistance and voltage.
- Selecting an appropriate light threshold.
- Troubleshooting LED polarity and breadboard connections.
- Understanding the relationship between sensor readings and output control.

## 11. Future Improvements

- Replace the demonstration LED with a suitable lighting driver.
- Add hysteresis to prevent rapid switching.
- Measure actual light intensity using a calibrated sensor.
- Introduce energy monitoring.
- Explore solar-powered street lighting.

## 12. Skills and Knowledge Gained

- Basic embedded systems design.
- Sensor interfacing.
- Analogue signal measurement.
- Arduino programming.
- Electronic circuit assembly.
- Hardware troubleshooting.
- Automatic control logic.

## 13. Project Status

Prototype development and testing.

Further validation of the physical LED output is required.

## 14. Conclusion

This project demonstrates how embedded electronics can be used to automate lighting systems.

It introduces the practical integration of sensors, microcontrollers, electronic components and programming to address an everyday engineering problem.
## Project Images

### Tinkercad Circuit Design
![LDR Circuit - Image 1](LDR%20image1.jpeg)

### Tinkercad Simulation
![LDR Circuit - Image 2](LDR%20image2.jpeg)
