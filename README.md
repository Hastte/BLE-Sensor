# BLE-Sensor
A low-power BLE humidity and temperature sensor board based on STM32WB10

## Overview
This repository contains the complete design files for a Bluetooth Low Energy (BLE) enabled environmental sensor board. The sensor measures temperature and humidity and transmits data wirelessly via BLE.

### Key Features
- **Microcontroller**: STM32WB10 (BLE-enabled MCU)
- **Sensors**: Temperature and Humidity
- **Connectivity**: Bluetooth Low Energy (BLE)
- **Power**: Low-power design for battery operation

## Repository Structure
```
BLE-Sensor/
├── hardware/          # Hardware design files
│   ├── pcb/          # PCB layout files
│   └── schematics/   # Circuit schematics
├── firmware/         # Embedded firmware
│   ├── src/          # Source files
│   └── inc/          # Header files
├── docs/             # Documentation
│   └── images/       # Images and diagrams
├── tools/            # Utility scripts and tools
├── LICENSE           # License information
└── README.md         # This file
```

## Getting Started

### Hardware
The hardware design files are located in the `hardware/` directory. See the [Hardware README](hardware/README.md) for more information on the PCB design and bill of materials.

### Firmware
The firmware source code is in the `firmware/` directory. See the [Firmware README](firmware/README.md) for build instructions and dependencies.

### Documentation
Additional documentation can be found in the `docs/` directory, including:
- Hardware specifications
- Assembly instructions
- User guide

## Contributing
Contributions are welcome! Please feel free to submit issues or pull requests.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For questions or support, please open an issue on GitHub.
