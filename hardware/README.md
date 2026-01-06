# Hardware Design

This directory contains all hardware design files for the BLE-Sensor board.

## Directory Structure
- `pcb/` - PCB layout files and Gerber files
- `schematics/` - Circuit schematics and design files

## Hardware Specifications

### Main Components
- **MCU**: STM32WB10 - BLE-enabled microcontroller
- **Sensors**: 
  - Temperature sensor (TBD)
  - Humidity sensor (TBD)
- **Power Supply**: Battery-powered with voltage regulation
- **Connectivity**: BLE antenna (PCB or external)

### PCB Specifications
- **Layers**: TBD (typically 2 or 4 layers)
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

## Getting Started

1. Open the schematic files in your preferred EDA tool
2. Review the circuit design
3. Check the PCB layout
4. Generate manufacturing files (Gerbers, BOM, etc.)

## Notes
- Always verify component footprints before ordering PCBs
- Check power supply voltage levels
- Verify antenna design and RF layout guidelines for BLE operation
