# Bloombot Project - Current Test Results  

## Test Results Summary  
The following table outlines the results of the latest tests conducted on the Bloombot project:  

| **Test Name**                | **Description**                          | **Expected Result**                     | **Actual Result**              | **Status**  |
|------------------------------|------------------------------------------|-----------------------------------------|--------------------------------|-------------|
| **UART Communication Test**  | Verify data transmission between boards. | Reliable data exchange without errors.  | Successful with zero errors.   | ✅ Pass     |
| **Moisture Sensor Test**      | Check soil moisture readings.            | Consistent analog-to-digital readings.  | Values within expected range.  | ✅ Pass     |
| **LDR Sensor Test**           | Test ambient light measurements.         | Accurate light intensity detection.     | Working as expected.           | ✅ Pass     |
| **LCD Display Test**          | Verify data display on LCD.              | Correct and readable output on LCD.     | Display showing sensor data.   | ✅ Pass     |
| **Power Consumption Test**    | Measure system's power requirements.     | Current draw within safe limits.        | Measured at 200mA max.         | ✅ Pass     |
| **Error Handling Test**       | Test system response to invalid inputs.  | System maintains stability.             | Recovered from UART errors.    | ✅ Pass     |

---

## Detailed Test Results  

### 1. **UART Communication Test**  
- **Setup:** Connected TX/RX pins between STM32 boards.  
- **Procedure:** Sent test packets of sensor data from Board 1 to Board 2.  
- **Results:**  
  - Data transmission successful.  
  - No packet loss observed at a baud rate of 9600.  
- **Status:** ✅ Pass  

### 2. **Moisture Sensor Test**  
- **Setup:** Moisture sensor connected to Board 1 analog input pin.  
- **Procedure:** Placed sensor in dry soil, damp soil, and water.  
- **Results:**  
  - Dry soil: 200 ADC value.  
  - Damp soil: 600 ADC value.  
  - Water: 800 ADC value.  
- **Status:** ✅ Pass  

### 3. **LDR Sensor Test**  
- **Setup:** LDR connected to Board 1 analog input pin.  
- **Procedure:** Measured light levels under different conditions (dark, room light, sunlight).  
- **Results:**  
  - Dark: 50 ADC value.  
  - Room light: 400 ADC value.  
  - Sunlight: 800 ADC value.  
- **Status:** ✅ Pass  

### 4. **LCD Display Test**  
- **Setup:** LCD connected to Board 2 GPIO pins.  
- **Procedure:** Sent data from Board 1 to Board 2 and displayed it on the LCD.  
- **Results:**  
  - Displayed: "Moisture: 600, Light: 400".  
- **Status:** ✅ Pass  

### 5. **Power Consumption Test**  
- **Setup:** Powered system with 5V and measured current draw.  
- **Procedure:** Monitored power usage during data acquisition and transmission.  
- **Results:**  
  - Maximum current draw: 200mA.  
  - Well within the capacity of the power supply.  
- **Status:** ✅ Pass  

### 6. **Error Handling Test**  
- **Setup:** Induced UART errors by sending invalid data packets.  
- **Procedure:** Observed system behavior and recovery mechanism.  
- **Results:**  
  - Detected errors and retransmitted packets successfully.  
  - No system crash or data loss.  
- **Status:** ✅ Pass  

---

## Observations  
- The system performed well across all tests.  
- No major issues encountered during the testing phase.  
- Future tests may focus on long-term durability and wireless integration.  

---

## Next Steps  
1. Conduct prolonged testing to evaluate system stability over time.  
2. Implement additional sensors to expand system capabilities.  
3. Explore integration with a cloud-based monitoring platform.  

