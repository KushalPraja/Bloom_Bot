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



### Software  
- **STM32CubeIDE:** For writing and debugging firmware.  
- **HAL Library:** For peripheral initialization and control.  
- **UART Driver:** For serial communication.  
- **Embedded C/C++ Codebase:** Handles data acquisition, processing, and display.  



## Circuit Diagram  
Design the following connections:  
1. **Moisture Sensor:** Connect to analog input pins on STM32 Board 1.  
2. **LDR:** Connect to another analog input pin on STM32 Board 1.  
3. **LCD Display:** Attach to GPIO pins of STM32 Board 2 for output.  
4. **UART TX (Board 1) to UART RX (Board 2):** For transmitting data between the boards.  
5. **Common Ground:** Ensure all components share a common ground.

---

## Setup Instructions  

# Bloombot Project Using Two STM32 Boards and UART Communication

## Overview  
Bloombot is a project designed to demonstrate efficient communication and sensor-based control using two STM32 Nucleo boards. The project utilizes UART (Universal Asynchronous Receiver/Transmitter) for communication between the boards. It incorporates a moisture sensor, an LDR (Light Dependent Resistor), and an LCD to monitor and display environmental parameters, simulating smart agriculture or similar IoT-based systems.


## Features  
- **UART Communication:** Reliable transmission of data between two STM32 boards.  
- **Moisture Sensor Integration:** Monitors soil moisture levels.  
- **Light Sensing with LDR:** Measures ambient light intensity.  
- **LCD Display:** Outputs real-time data for easy monitoring.  
- **Expandable Design:** Modular setup for additional sensors or functionalities.  


## Components  
### Hardware  
1. **STM32 Nucleo Boards (x2):** Primary microcontrollers.  
2. **Moisture Sensor:** Measures soil moisture level.  
3. **LDR (Light Dependent Resistor):** Measures light intensity.  
4. **LCD Display (16x2 or similar):** Displays sensor data and system status.  
5. **Resistors and Capacitors:** For circuit stability and sensor connections.  
6. **Breadboard and Wires:** For prototyping connections.  
7. **Power Supply:** 5V/3.3V for the STM32 and sensors.  


### Software  
- **STM32CubeIDE:** For writing and debugging firmware.  
- **HAL Library:** For peripheral initialization and control.  
- **UART Driver:** For serial communication.  
- **Embedded C/C++ Codebase:** Handles data acquisition, processing, and display.  

---

## Setup Instructions  


### 1. Repository Clone:
   - Start by cloning this repository to access the project files:
```bash git clone https://github.com/KushalPraja/Bloom_Bot```

```cd Bloom_Bot```

###  2. Hardware Setup:
   - Assemble components as per the circuit diagram.  
   - Connect UART pins (TX/RX) between the two STM32 boards.  
   - Power the components and STM32 boards.  

### 3. Software Setup  

#### Import Source Files  
- Open **STM32CubeIDE** and create **two separate projects**, one for each STM32 board:  
  - **Input Board (STM32 Board 1):**  
    - Copy the `src` files from the **Input_Board** folder in the repository into the project for this board.  
    - This board handles **analog-to-digital conversion** for the moisture sensor and LDR and transmits sensor data using **UART1**.  
  - **Output Board (STM32 Board 2):**  
    - Copy the `src` files from the **Output_Board** folder in the repository into the project for this board.  
    - This board receives the UART data, decodes it, and displays it on the LCD.  

#### Configuration and Libraries  
- Ensure UART communication is configured in **asynchronous mode** using HAL libraries.  

---

### 4. Compilation and Upload  
- Compile each project individually in **STM32CubeIDE**.  
- Flash the binaries to the respective STM32 boards using a **ST-Link programmer**.  

---

### 5. Testing and Debugging  
- Verify the system by checking that:  
  - Sensor data is accurately transmitted from Board 1 to Board 2 via UART.  
  - The LCD connected to Board 2 displays the data correctly.  
- Use the UART debug tools in **STM32CubeIDE** for troubleshooting if needed.  

---

### 6. Explore the Repository  
- For detailed explanations and additional resources, refer to the **README** and **project folders** on GitHub: [GitHub Repository](https://github.com/KushalPraja/Bloom_Bot).  


