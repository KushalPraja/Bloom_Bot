# Bloombot Project Using Two STM32 Boards and UART Communication

## Overview  
Bloombot is a project designed to demonstrate efficient communication and sensor-based control using two STM32 Nucleo boards. The project utilizes UART (Universal Asynchronous Receiver/Transmitter) for communication between the boards. It incorporates a moisture sensor, an LDR (Light Dependent Resistor), and an LCD to monitor and display environmental parameters, simulating smart agriculture or similar IoT-based systems.

---

## Features  
- **UART Communication:** Reliable transmission of data between two STM32 boards.  
- **Moisture Sensor Integration:** Monitors soil moisture levels.  
- **Light Sensing with LDR:** Measures ambient light intensity.  
- **LCD Display:** Outputs real-time data for easy monitoring.  
- **Expandable Design:** Modular setup for additional sensors or functionalities.  

---

## Components  
### Hardware  
1. **STM32 Nucleo Boards (x2):** Primary microcontrollers.  
2. **Moisture Sensor:** Measures soil moisture level.  
3. **LDR (Light Dependent Resistor):** Measures light intensity.  
4. **LCD Display (16x2 or similar):** Displays sensor data and system status.  
5. **Resistors and Capacitors:** For circuit stability and sensor connections.  
6. **Breadboard and Wires:** For prototyping connections.  
7. **Power Supply:** 5V/3.3V for the STM32 and sensors.  

---

### Software  
- **STM32CubeIDE:** For writing and debugging firmware.  
- **HAL Library:** For peripheral initialization and control.  
- **UART Driver:** For serial communication.  
- **Embedded C/C++ Codebase:** Handles data acquisition, processing, and display.  

---

## Circuit Diagram  
Design the following connections:  
1. **Moisture Sensor:** Connect to analog input pins on STM32 Board 1.  
2. **LDR:** Connect to another analog input pin on STM32 Board 1.  
3. **LCD Display:** Attach to GPIO pins of STM32 Board 2 for output.  
4. **UART TX (Board 1) to UART RX (Board 2):** For transmitting data between the boards.  
5. **Common Ground:** Ensure all components share a common ground.

---

## Setup Instructions  
1. **Hardware Setup:**  
   - Assemble components as per the circuit diagram.  
   - Connect UART pins (TX/RX) between the two STM32 boards.  
   - Power the components and STM32 boards.  

2. **Software Setup:**  
   - Open STM32CubeIDE and create two separate projects: one for each STM32 board.  
   - Configure UART communication in asynchronous mode using HAL libraries.  
   - Implement analog-to-digital conversion for the moisture sensor and LDR on STM32 Board 1.  
   - Transmit sensor data via UART from Board 1 to Board 2.  
   - Decode received data on STM32 Board 2 and display it on the LCD
