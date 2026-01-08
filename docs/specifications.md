# Hardware Specification Document

## 1. Introduction
### 1.1 Purpose
This document specifies the hardware requirements and design for the BLE Sensor project.

### 1.2 Scope
This specification covers the microcontroller, sensors, power management, and connectivity modules.

## 2. System Overview
### 2.1 Block Diagram
[Placeholder for Block Diagram]

### 2.2 Key Components
- Microcontroller Unit (MCU)
- Bluetooth Low Energy (BLE) Module
- Temperature and Humidity Sensor
- Power Management Unit (PMU)

## 3. Component Specifications

### 3.1 Microcontroller
- **Architecture**: ARM Cortex-M4 or equivalent
- **Clock Speed**: 64 MHz minimum
- **Memory**: 512KB Flash, 64KB RAM
- **I/O Ports**: GPIO, I2C, SPI, UART

### 3.2 Connectivity (BLE)
- **Standard**: Bluetooth 5.0 or higher
- **Range**: Up to 10 meters
- **Antenna**: PCB Trace

### 3.3 Sensors
#### 3.3.1 Environmental Sensor
- **Type**: Temperature & Humidity
- **Range**: -40°C to +60°C, 0-100% RH
- **Accuracy**: ±1°C / ±1%RH
- **Interface**: I2C/SPI

### 3.4 Power Management
- **Input Voltage**: 5V DC
- **Battery**: Li-Po 3.7V
- **Charging**: USB-C charging circuit
- **Fuel Gauge**: Low-Power over I2C/SPI
- **Battery Life Target** : >6 months

## 4. Mechanical Specifications
- **Dimensions**: 40mm x 40mm x 15mm (approx.)
- **Enclosure Material**: PLA or better
- **Enclosure Complexity**: Must be easily 3D printed

## 5. Environmental Requirements
- **Operating Temperature**: -20°C to +60°C

## 6. Revision History
| Version | Date       | Author | Description |
|---------|------------|--------|-------------|
| 1.0     | 2026-01-08 | Hastte | Initial Draft |
