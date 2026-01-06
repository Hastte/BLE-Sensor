# Schematic Files

This directory contains circuit schematics for the BLE-Sensor board.

## File Types

Depending on the EDA tool used, this directory may contain:

### KiCad
- `*.kicad_sch` - Schematic file
- `sym-lib-table` - Symbol library table
- `*.lib` - Custom symbol libraries

### Altium Designer
- `*.SchDoc` - Schematic document
- `*.SchLib` - Schematic library

### EAGLE
- `*.sch` - Schematic file
- `*.lbr` - Library file

## Circuit Overview

The BLE-Sensor schematic includes the following sections:

### Power Supply
- Battery input
- Voltage regulation (if needed)
- Power distribution
- Decoupling capacitors

### Microcontroller (STM32WB10)
- MCU with all connections
- Crystal oscillator (if external)
- Reset circuit
- Boot configuration
- SWD programming interface

### RF Section
- Antenna matching network
- RF output
- Balun or matching components
- Following STM32WB reference design

### Sensors
- Temperature sensor interface
- Humidity sensor interface
- I2C or SPI connections
- Pull-up resistors

### Programming/Debug
- SWD header (SWDIO, SWCLK, GND, VCC)
- UART pins (optional)
- Reset button (optional)

### Indicators
- Status LED (optional)
- Current limiting resistor

## Design Guidelines

### General
- Follow STM32WB10 datasheet recommendations
- Use recommended reference designs
- Include proper decoupling
- Label all nets clearly

### Power
- Calculate power requirements
- Size voltage regulator appropriately
- Add input protection
- Use ferrite beads for analog supply filtering

### RF Design
- Follow ST application notes for RF layout
- Use recommended antenna matching
- Keep RF traces short and controlled impedance
- Minimize ground plane discontinuities

### Sensors
- Check sensor datasheets for circuit requirements
- Add proper pull-ups for I2C
- Consider ESD protection
- Provide adequate filtering

## Schematic Review Checklist

- [ ] All components have values
- [ ] All components have footprints assigned
- [ ] Power supply is adequate
- [ ] Decoupling capacitors on all ICs
- [ ] Pull-up/pull-down resistors where needed
- [ ] No unconnected pins (or marked as NC)
- [ ] Net names are clear and consistent
- [ ] Reference designators are unique
- [ ] ERC (Electrical Rule Check) passes
- [ ] Schematic matches reference designs

## Getting Started

1. Open the schematic in your EDA tool
2. Review each section of the circuit
3. Check component values and ratings
4. Run ERC (Electrical Rule Check)
5. Generate netlist for PCB layout
6. Export BOM

## Documentation

Export schematic as PDF for documentation:
- Include all sheets
- Use readable zoom level
- Print in landscape orientation
- Include title block information

## Notes

- Always check latest component datasheets
- Verify part numbers before ordering
- Consider component availability and lead times
- Include test points for debugging
