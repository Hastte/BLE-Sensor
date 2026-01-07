# Hardware Specifications

## BLE-Sensor Board Specifications

### Microcontroller
- **Model**: STM32WB10CCU6
- **Core**: ARM Cortex-M4 @ 64 MHz
- **BLE**: Bluetooth 5.0 Low Energy
- **Flash**: 320 KB
- **RAM**: 48 KB
- **Package**: UFQFPN48

### Sensor
#### Temperature & Humidity Sensor
- **Model**: TI HDC1080
- **Range**: -20°C to +70°C
- **Temperature Accuracy**: ±0.5°C
- **Humidity Accuracy**: ±2%RH
- **Interface**: I2C

### Power Supply
#### Battery
 - **Type**: Single 3.7V LiPo Battery 
 - **Connectivity**: PHR-2 ; 2 PinFemale Housing 
#### Charging IC
- **Model**: TP4054
- **Input Voltage**: 4.2V - 6.5V
- **Charging Voltage**: 4.2V ±1%
- **Maximum Charging Current**: 500mA

#### Fuel Gauge
- **Model**: STC3115
- **Operating Voltage**: 2.7V - 4.5V
- **Voltage Accuracy Measurement**: ±0.25%
- **ADC Current Accuracy**: ±0.5%
- **Current Consumption**: 100μA
- **Connectivity**: I2C

#### Power Path 
- **Output Voltage**: 
   - **USB-C connected**: V_USB-0.2 V
   - **If USB-C NOT connected**: V_BAT

#### Regulator
- **Model**: TPS6303
- **Type**: Buck-Boost Converter
- **Input Voltage**: 1.8V - 5.5V
- **Output Voltage**: 3.3V ±1%
- **Maximum Output Current**: 300mA
- **Minimum/Maximum Efficiency**: 65%/90%
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
