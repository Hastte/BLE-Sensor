# Hardware Design

This directory contains all hardware design files for the BLE-Sensor board.

## Directory Structure
- `pcb/` - PCB layout files and Gerber files
- `schematics/` - Circuit schematics and design files
## Hardware Specifications

### Main Components
- **MCU**: STM32WB10 - BLE-enabled microcontroller
- **Sensor**: HDC1080 - Temperature & Humidity sensor
- **Power Supply**: Battery-powered with voltage regulation
- **Connectivity**:
  - USB-C Port: Battery charging & Flashing
  - JTAG Connector: Flashing & Debugging  
### PCB Specifications
- **Layers**: 2
- **Dimensions**: TBD
- **PCB Technology**: TBD

## Bill of Materials (BOM)

A detailed bill of materials will be provided in the `BOM.csv` file once the design is finalized.

## Design Files

Hardware design files are typically created using:
- KiCad (recommended open-source option)
- Altium Designer
- EAGLE
- Or other PCB design tools

## Manufacturing

### PCB Fabrication
Gerber files for PCB manufacturing will be placed in the `pcb/gerbers/` directory.

### Assembly
Assembly instructions and pick-and-place files will be provided for manufacturing.
