# ADAPTIVE VEHICLE DASHBOARD SIMULATOR

## Project Overview

The Adaptive Vehicle Dashboard Simulator is an embedded systems-based project developed using two LPC2129 ARM7 microcontroller nodes. It monitors important vehicle parameters such as speed, fuel level, engine temperature, and indicator status.

The system uses Node A as the transmitter and Node B as the receiver. Node A collects sensor readings and indicator information and transmits the data to Node B using interrupt-based CAN communication. Node B processes the received data and displays the vehicle information on the serial monitor through UART communication.

## Key Features

- Vehicle speed monitoring using a potentiometer.
- Fuel level monitoring using an ultrasonic sensor.
- Engine temperature monitoring using an LM35 sensor.
- Left indicator status detection.
- Right indicator status detection.
- Headlight status detection.
- ADC-based sensor data acquisition.
- External interrupt handling for input detection.
- Interrupt-based CAN communication.
- UART-based real-time dashboard monitoring.
- Data packing and unpacking using bitwise operations.

## Hardware Components

- LPC2129 ARM7 Microcontrollers (2)
- Potentiometer
- Ultrasonic Sensor
- LM35 Temperature Sensor
- Left Indicator Switch
- Right Indicator Switch
- Headlight Switch
- CAN Communication Interface
- UART Serial Communication Interface

## Software and Tools

- Embedded C
- Keil µVision IDE
- ADC
- GPIO
- External Interrupts (EINT)
- CAN Protocol
- CAN Interrupts
- UART Protocol
- Serial Monitor

## System Architecture

### Node A – Transmitter

- Reads vehicle speed using a potentiometer through ADC.
- Measures fuel level using an ultrasonic sensor.
- Reads engine temperature using an LM35 sensor through ADC.
- Detects left indicator, right indicator, and headlight status.
- Packs sensor readings and indicator information into a CAN data frame.
- Transmits the collected information to Node B using CAN communication.

### Node B – Receiver

- Receives vehicle information from Node A through CAN communication.
- Handles CAN data reception using interrupts.
- Extracts individual sensor values and indicator status using bitwise operations.
- Processes the received data.
- Displays vehicle speed, fuel level, temperature, and indicator status on the serial monitor using UART communication.

## Communication Protocols

| Protocol | Purpose |
|---|---|
| ADC | Potentiometer and LM35 sensor data acquisition |
| GPIO | Digital input and output control |
| EINT | External interrupt handling |
| CAN | Communication between Node A and Node B |
| CAN Interrupts | Interrupt-based data transmission and reception |
| UART | Displaying dashboard information on the serial monitor |

## Working Principle

1. Node A collects vehicle speed, fuel level, and temperature readings from the respective sensors.
2. Indicator and headlight information is detected through digital inputs and external interrupt handling.
3. All collected information is packed into a CAN data frame.
4. Node A transmits the CAN frame to Node B.
5. Node B receives the CAN frame through interrupt-based communication.
6. The received data is unpacked and processed using bitwise operations.
7. The final vehicle parameters and indicator statuses are displayed on the serial monitor using UART.

## Project Structure


Adaptive-Vehicle-Dashboard-Simulator/
│
├── ADC_DRIVER.c
├── CAN_DRIVER.c
├── EXTINT_DRIVER.c
├── NODE-A.c
├── NODE-B.c
├── UART0_DRIVER.c
├── ULTRASONIC.c
├── header.h
└── README.md


## Learning Outcomes

- LPC2129 ARM7 microcontroller programming.
- ADC and GPIO peripheral interfacing.
- Sensor interfacing and data acquisition.
- External interrupt configuration and handling.
- CAN protocol configuration and communication.
- Interrupt-based CAN transmission and reception.
- CAN data frame packing and unpacking.
- UART serial communication.
- Multi-node embedded system development.
- Real-time vehicle parameter monitoring.

## Applications

- Automotive dashboard simulation.
- Vehicle parameter monitoring systems.
- Embedded automotive communication systems.
- CAN-based distributed control systems.
- Automotive electronics prototyping.

## Future Enhancements

- Integrating an OLED or LCD dashboard display.
- Adding warning alerts for low fuel and high temperature.
- Implementing automatic indicator switching.
- Adding vehicle speed-based adaptive alerts.
- Integrating wireless monitoring through Bluetooth or Wi-Fi.
- Extending the system to support additional vehicle parameters.

## Disclaimer

This project is developed for educational and simulation purposes. It demonstrates vehicle parameter monitoring and CAN-based communication between microcontroller nodes. It is not intended for direct use in real vehicle control or safety-critical automotive applications.


## Author

**Ishwari Sampatakumar Bilagi**

- GitHub: [ishwaribilagi-gif](https://github.com/ishwaribilagi-gif)
- LinkedIn: [Ishwari Bilagi](https://www.linkedin.com/in/ishwari-bilagi-61b762277/)
- Email: ishwaribilagi@gmail.com

**Project:** Adaptive Vehicle Dashboard Simulator

**Domain:** Embedded Systems | ARM7 LPC2129 | Embedded C
