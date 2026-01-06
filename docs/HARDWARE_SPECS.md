# Hardware Specifications

## BLE-Sensor Board Specifications

### Microcontroller
- **Model**: STM32WB10CCU6
- **Core**: ARM Cortex-M4 @ 64 MHz
- **BLE**: Bluetooth 5.0 Low Energy
- **Flash**: 320 KB
- **RAM**: 48 KB
- **Package**: UFQFPN48

### Sensors
#### Temperature Sensor
- **Type**: Digital temperature sensor
- **Range**: -40°C to +85°C
- **Accuracy**: ±0.5°C
- **Interface**: I2C or SPI

#### Humidity Sensor
- **Type**: Digital humidity sensor
- **Range**: 0% to 100% RH
- **Accuracy**: ±3% RH
- **Interface**: I2C or SPI

### Power Supply
- **Input Voltage**: 3.0V - 3.6V
- **Battery**: CR2032 coin cell or similar
- **Regulator**: LDO regulator (if needed)
- **Current Consumption**:
  - Active mode: < 10 mA
  - Sleep mode: < 10 μA
  - Stop mode: < 5 μA

### BLE Radio
- **Frequency**: 2.4 GHz ISM band
- **Output Power**: Up to +6 dBm
- **Sensitivity**: -96 dBm
- **Range**: Up to 10m (open space)
- **Antenna**: PCB antenna or external connector

### Interfaces
- **Programming**: SWD (Serial Wire Debug)
- **Debug**: UART (optional)
- **Sensor Interface**: I2C or SPI
- **Power**: Battery connector

### Physical Specifications
- **Dimensions**: TBD (target: < 30mm x 30mm)
- **PCB Thickness**: 1.6mm
- **PCB Layers**: 2 or 4 layers
- **Operating Temperature**: -20°C to +60°C
- **Storage Temperature**: -40°C to +85°C

### Environmental Ratings
- **RoHS Compliant**: Yes
- **Operating Humidity**: 10% to 90% RH (non-condensing)

### Connectors
- **Battery Connector**: 2-pin JST or solder pads
- **SWD Header**: 4-pin (SWDIO, SWCLK, GND, VCC)
- **Optional UART**: 2-pin header

## Electrical Characteristics

### Power Consumption Estimates
| Mode | Current | Notes |
|------|---------|-------|
| Active (BLE TX) | 8-10 mA | During BLE transmission |
| Active (Sensor Read) | 2-5 mA | During sensor measurement |
| Sleep | < 10 μA | Between measurements |
| Stop | < 5 μA | Deep sleep mode |

### Battery Life Estimation
With CR2032 battery (220 mAh):
- Measurement every 10 seconds: ~6-12 months
- Measurement every 60 seconds: 12-18 months
- Depends on BLE connection time and advertising

## Design Considerations

### RF Design
- Follow STM32WB reference design for RF section
- Proper impedance matching for antenna
- Keep RF traces away from noisy signals
- Ground plane under RF section

### Power Design
- Adequate decoupling capacitors
- Low-noise power supply for analog sensors
- Battery polarity protection
- Low-dropout regulator if needed

### Layout Guidelines
- Separate analog and digital grounds
- Short traces for high-speed signals
- Proper SWD header placement
- Easy access for programming

## Revision History
- v1.0 - Initial specification (TBD)

## Notes
- Specifications subject to change during development
- Actual performance may vary based on implementation
- Refer to component datasheets for detailed specifications
