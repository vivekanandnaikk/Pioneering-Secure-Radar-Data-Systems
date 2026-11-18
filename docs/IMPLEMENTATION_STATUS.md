# Implementation Status

## Repository status

This repository is currently a documentation foundation. It does not contain source code or verified implementation artifacts.

## Report-described work

The supplied academic report describes:

- A Texas Instruments AWR1243 radar sensor.
- A sender ESP32 that receives radar-derived positional data and calculates object distance.
- AES-128 encryption on the sender.
- Wi-Fi and UDP communication to a receiver ESP32.
- Receiver-side decryption and I2C LCD output.
- A displayed example of `Decrypted Dist: 5.708`.

These statements describe the report and should not be treated as independently reproduced repository evidence.

## Not yet present

- Sender firmware.
- Receiver firmware.
- Radar configuration or data parsing code.
- AES implementation and key configuration.
- Wi-Fi and UDP configuration.
- LCD integration code.
- Board selection, library versions, and dependency manifest.
- Wiring or circuit documentation.
- Hardware photographs or extracted report figures.
- Repeated test logs or benchmark evidence.
- Original project report or approved redistribution copy.

## Missing implementation details

The report does not establish:

- Whether AWR1243 integration was fully physical and operational in the final demonstration.
- Whether Arduino IDE, ESP-IDF, or both were used for final firmware.
- The AES mode or library implementation.
- The key size, key-generation process, key provisioning, or key storage.
- Whether UDP packets include integrity or replay protection.
- The transmitted data format or packet size.
- End-to-end unit conversion for the displayed distance.
- The exact ESP32 board, radar board, LCD module, or pin assignments.

## Verification needed

Before publishing firmware or setup instructions, verify the original source against this checklist:

1. Confirm final hardware usage.
2. Separate sender and receiver source files.
3. Identify programming language and build environment.
4. Pin and document every hardware connection.
5. Document radar input and distance calculation units.
6. Document the AES mode and authentication properties.
7. Replace demonstration secrets with documented safe configuration.
8. Provide dependency versions and build commands.
9. Record the sender/receiver network setup.
10. Include a hardware test procedure and representative results.

## Reproducibility policy

Do not claim a feature or result unless source code, configuration, or test artifacts in this repository can support it. Do not publish unverified distance accuracy, latency, throughput, or packet-loss figures.
