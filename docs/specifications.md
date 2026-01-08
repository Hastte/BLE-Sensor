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
- Sensor Array
- Power Management Unit (PMU)

## 3. Component Specifications

### 3.1 Microcontroller
- **Architecture**: ARM Cortex-M4 or equivalent
- **Clock Speed**: 64 MHz minimum
- **Memory**: 512KB Flash, 64KB RAM
- **I/O Ports**: GPIO, I2C, SPI, UART

### 3.2 Connectivity (BLE)
- **Standard**: Bluetooth 5.0 or higher
- **Range**: Up to 50 meters line-of-sight
- **Antenna**: PCB Trace or Ceramic Chip Antenna

### 3.3 Sensors
#### 3.3.1 Environmental Sensor
- **Type**: Temperature & Humidity
- **Range**: -40°C to +85°C, 0-100% RH
- **Interface**: I2C

#### 3.3.2 Accelerometer
- **Axis**: 3-axis
- **Range**: ±2g/±4g/±8g/±16g
- **Interface**: SPI/I2C

### 3.4 Power Management
- **Input Voltage**: 3.3V - 5V DC
- **Battery**: CR2032 Coin Cell or Li-Po 3.7V
- **Charging**: USB-C charging circuit (if Li-Po)
- **Power Consumption**: < 10µA in sleep mode

## 4. Mechanical Specifications
- **Dimensions**: 40mm x 40mm x 15mm (approx.)
- **Enclosure Material**: ABS Plastic or Polycarbonate
- **IP Rating**: IP65 (Dust tight, water resistant)

## 5. Environmental Requirements
- **Operating Temperature**: -20°C to +70°C
- **Storage Temperature**: -30°C to +85°C

## 6. Regulatory & Compliance
- FCC / CE Certification requirements
- RoHS Compliance

## 7. Revision History
| Version | Date       | Author | Description |
|---------|------------|--------|-------------|
| 1.0     | 2026-01-08 | Hastte | Initial Draft |
