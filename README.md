# Pioneering Secure Radar Data Systems for Advanced Automotive Safety

A radar-based object distance measurement and secure wireless communication system using ESP32 microcontrollers, AES-128 encryption, and Wi-Fi UDP transmission.

## Overview

This project demonstrates a secure radar data communication system designed for automotive safety, Advanced Driver Assistance Systems (ADAS), and IoT-based applications.

The system captures positional data from a Texas Instruments AWR1243 radar sensor, processes object distance information, encrypts the data using AES-128, and transmits it wirelessly between two ESP32 microcontrollers using Wi-Fi and UDP.

The receiving ESP32 decrypts the transmitted information and displays the recovered distance on an I2C LCD.

## Key Features

- Radar-based object distance measurement
- Real-time radar data processing
- AES-128 data encryption and decryption
- Wireless communication using ESP32 Wi-Fi
- UDP-based data transmission
- Dual ESP32 sender and receiver architecture
- I2C LCD-based output visualization
- Communication status feedback

## System Architecture

The system consists of two ESP32 microcontrollers:

**Sender Unit**
1. Acquires radar sensor measurements.
2. Processes positional data and calculates object distance.
3. Encrypts the processed data using AES-128.
4. Transmits the encrypted data through Wi-Fi using UDP.

**Receiver Unit**
1. Receives encrypted UDP packets.
2. Decrypts the received information using the corresponding AES configuration.
3. Processes the recovered distance information.
4. Displays the decrypted output on the LCD.

## Technologies Used

| Category | Technology |
|---|---|
| Programming | C/C++ embedded firmware |
| Microcontroller | ESP32 |
| Radar sensor | Texas Instruments AWR1243 |
| Encryption | AES-128 |
| Communication | Wi-Fi |
| Network protocol | UDP |
| Radar interface | SPI |
| Display interface | I2C |
| Display | 16×2 LCD |
| Development environments | Arduino IDE, ESP-IDF |

## Hardware Requirements

- Texas Instruments AWR1243 radar sensor
- 2 × ESP32 development boards
- 2 × 16×2 LCD modules
- USB cables and power supply
- Jumper wires and prototype boards
- Wi-Fi network
- Laptop or computer for development and debugging

## Software Requirements

- Arduino IDE
- ESP-IDF development framework
- ESP32 board support and required libraries
- AES encryption implementation
- UDP networking support

The exact dependency versions and library requirements will be documented after verification against the source code.

## Project Workflow

Radar Data Acquisition  
↓  
Object Distance Calculation  
↓  
AES-128 Encryption  
↓  
Wi-Fi / UDP Transmission  
↓  
ESP32 Receiver  
↓  
AES Decryption  
↓  
LCD Output Display

## Results

The project report demonstrates successful encrypted data transmission and decryption between two ESP32 devices.

The sender LCD displays encrypted transmission status, while the receiver LCD displays the decrypted distance information.

One example displayed in the report is:

`Decrypted Dist: 5.708`

The report does not provide independently measured latency, throughput, packet-loss percentage, or a numerical accuracy benchmark.

## Applications

- Advanced Driver Assistance Systems (ADAS)
- Automotive safety communication
- Secure radar data transmission
- Internet of Things (IoT)
- Smart transportation systems
- Industrial monitoring and automation

## Limitations

- The project is an academic prototype.
- Quantitative communication and latency benchmarks are not documented in the report.
- The AES mode and key-management implementation require further documentation.
- Further testing and optimization are necessary for deployment in safety-critical environments.

## Future Enhancements

- Advanced radar signal processing
- Multi-radar data fusion
- Improved encryption and key management
- Cloud-based monitoring and analytics
- Enhanced HMI visualization
- Performance optimization for embedded platforms

## Project Information

**Project Type:** Senior Design Project  
**Institution:** KLE Technological University  
**Department:** School of Electronics and Communication Engineering  
**Academic Year:** 2024–2025

**Project Team**
- Vivekanand Naik
- Sunil Dyamakkanavar
- Chetan Havanagi
- Samarth G

**Project Guides**
- Prof. Shraddha Hiremath
- Prof. Preeti Pillay

## Safety Disclaimer

This project is an academic prototype intended for educational and demonstration purposes. It is not a certified automotive safety system and must not be used as the sole basis for vehicle control, collision avoidance, or other safety-critical decisions.

## License

License to be determined after reviewing the source code and third-party dependencies.
