# Pioneering Secure Radar Data Systems for Advanced Automotive Safety

An academic prototype exploring radar-derived distance measurement and encrypted wireless data transfer between two ESP32 microcontrollers using AES-128 and Wi-Fi/UDP.

> **Safety notice:** This is an educational prototype, not a certified automotive safety system. Do not use it as the sole basis for vehicle control, collision avoidance, or other safety-critical decisions.

## Overview

The project report describes a system that acquires positional measurements from a Texas Instruments AWR1243 radar sensor, calculates object distance from 3D coordinates, encrypts the resulting data with AES-128, and sends it over Wi-Fi using UDP. A second ESP32 receives and decrypts the data, then displays the recovered distance on a 16×2 I2C LCD.

The report describes radar-to-controller communication over SPI and LCD communication over I2C. This repository currently documents the project; source code, wiring diagrams, dependency manifests, and reproducible setup instructions have not yet been added.

## System workflow

1. Acquire radar positional measurements (X, Y, Z).
2. Calculate object distance.
3. Encrypt the data using AES-128 on the sender ESP32.
4. Transmit the encrypted data over Wi-Fi using UDP.
5. Receive and decrypt the data on a second ESP32.
6. Display the recovered distance on the LCD.

```text
AWR1243 radar → ESP32 sender → AES-128 → Wi-Fi / UDP
                                             ↓
16×2 I2C LCD ← ESP32 receiver ← decryption ←─┘
```

## Project details

| Area | Reported details |
|---|---|
| Project type | Senior Design Project, Semester VII, academic year 2024–2025 |
| Institution | KLE Technological University, School of Electronics and Communication Engineering |
| Microcontrollers | 2 × ESP32 development boards |
| Radar | Texas Instruments AWR1243 |
| Radar interface | SPI |
| Distance input | 3D positional coordinates (X, Y, Z) |
| Wireless transport | Wi-Fi using UDP |
| Encryption | AES-128; mode and key-management details are not specified in the report |
| Display | 16×2 LCD using I2C |
| Development environments mentioned | Arduino IDE and ESP-IDF; the exact environment used for the final firmware is not confirmed here |

## Dataset

This is an embedded sensing and communications project, not a machine-learning project. It does not use a training, validation, or test dataset. The report describes live radar measurements but does not provide a recorded dataset, sample count, or downloadable data files.

## Results

The report describes a demonstration in which the sender indicates encrypted transmission and the receiver displays the decrypted distance. One example shown is:

```text
Decrypted Dist: 5.708
```

This is an example output, not a documented accuracy result. The report does not provide numerical measurements for latency, throughput, packet loss, distance accuracy, or cryptographic performance.

## Hardware described in the report

- Texas Instruments AWR1243 radar sensor
- 2 × ESP32 development boards
- 2 × 16×2 LCD modules with I2C interface
- Wi-Fi network
- USB cables or external power supply
- Jumper wires and prototype boards

The report mentions SPI for the radar interface and I2C for the LCD. Pin assignments, circuit diagrams, and power requirements for a reproducible build are not included here.

## Software and reproducibility

The report mentions Arduino IDE, ESP-IDF, embedded C/C++, AES encryption/decryption, and UDP networking. The exact firmware, framework versions, library dependencies, AES mode, key provisioning, and configuration are not available in this repository yet. Consequently, build and run instructions are intentionally not provided until they can be verified against the original source files.

When adding firmware or configuration, do not commit Wi-Fi passwords, private AES keys, or other credentials. Use local, untracked configuration for secrets and document safe setup steps separately.

## Limitations and security considerations

- This is an academic prototype, not a production or safety-certified system.
- The report does not provide quantitative performance benchmarks or a detailed real-world validation protocol.
- The AES mode, key-management approach, and cryptographic validation are not specified. AES-128 alone does not establish that the overall communication is authenticated or secure against tampering or replay.
- Source code and complete, reproducible hardware/software setup instructions are not currently included.
- Further engineering, testing, and independent safety and security review would be required before any operational use.

## Potential future work

- Publish the verified sender and receiver firmware and build instructions.
- Document wiring, radar configuration, and LCD pin assignments.
- Specify and review the encryption mode, authentication, key provisioning, and replay protections.
- Measure and report distance error, end-to-end latency, throughput, and packet loss using a documented test procedure.
- Explore multi-radar processing and improved visualization.

## Project team and acknowledgments

**Project team**
- Vivekanand Naik
- Sunil Dyamakkanavar
- Chetan Havanagi
- Samarth G

**Project guides**
- Prof. Shraddha Hiremath
- Prof. Preeti Pillay

**Institution:** KLE Technological University, School of Electronics and Communication Engineering.

## License

No license has been selected. Until a license is added, reuse and redistribution permissions are not specified. Review third-party dependencies and ownership before choosing a license.
