# Firmware

This directory contains the embedded firmware for the BLE-Sensor board.

## Directory Structure
- `src/` - Source code files (.c)
- `inc/` - Header files (.h)

## Overview

The firmware is designed to run on the STM32WB10 microcontroller and implements:
- BLE communication stack
- Sensor data acquisition (temperature & humidity)
- Power management for low-power operation
- BLE advertising and data transmission

## Build Requirements

### Toolchain
- **Compiler**: ARM GCC toolchain (`arm-none-eabi-gcc`)
- **Build System**: Make or CMake
- **Debugger**: STLink or compatible debugger

### Dependencies
- STM32WB HAL library
- STM32WB BLE stack
- CMSIS library

## Building the Firmware

```bash
# Navigate to the firmware directory
cd firmware/

# Build the project
make all

# Flash to the device
make flash
```

## Development Setup

### IDE Options
- STM32CubeIDE (recommended)
- Visual Studio Code with Cortex-Debug extension
- Keil MDK
- IAR Embedded Workbench

### Debugging
Use STLink or JLink debugger for programming and debugging:

```bash
# Using OpenOCD
openocd -f interface/stlink.cfg -f target/stm32wbx.cfg

# Using GDB
arm-none-eabi-gdb firmware.elf
```

## Firmware Features

### BLE Services
- Environmental Sensing Service
  - Temperature characteristic
  - Humidity characteristic
- Device Information Service
  - Manufacturer name
  - Model number
  - Firmware version

### Power Modes
- Active mode (during measurement and BLE transmission)
- Sleep mode (between measurements)
- Stop mode (deep sleep)

## Configuration

Configuration parameters can be modified in the header files:
- `config.h` - General configuration
- `ble_config.h` - BLE parameters
- `sensor_config.h` - Sensor settings

## Getting Started

1. Set up the ARM GCC toolchain
2. Install required libraries (HAL, BLE stack)
3. Build the project
4. Flash to the STM32WB10 board
5. Monitor output via debugger or BLE connection

## Programming

### Using STLink
```bash
st-flash write firmware.bin 0x8000000
```

### Using OpenOCD
```bash
openocd -f interface/stlink.cfg -f target/stm32wbx.cfg \
  -c "program firmware.elf verify reset exit"
```

## Notes
- Ensure correct BLE stack version for STM32WB10
- Follow ST guidelines for RF and antenna design
- Configure low-power modes for battery operation
