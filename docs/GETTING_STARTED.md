# Getting Started with BLE-Sensor

This guide will help you get started with the BLE-Sensor board.

## Prerequisites

### Hardware
- BLE-Sensor board (assembled)
- STLink programmer/debugger
- USB cable for STLink
- Battery or power supply (3.3V)
- Computer with USB port

### Software
- ARM GCC toolchain
- STM32CubeProgrammer or OpenOCD
- BLE scanner app (nRF Connect, LightBlue, etc.)

## Initial Setup

### 1. Hardware Connection
1. Connect the STLink programmer to the SWD interface on the board
2. Connect STLink to your computer via USB
3. Ensure the board is powered (battery or external supply)

### 2. Programming the Firmware
```bash
# Clone the repository
git clone https://github.com/Hastte/BLE-Sensor.git
cd BLE-Sensor/firmware

# Build the firmware
make all

# Flash to the device
make flash
```

### 3. Verification
1. The board should start advertising via BLE after programming
2. Open a BLE scanner app on your smartphone
3. Look for "BLE-Sensor" or similar device name
4. Connect to the device
5. Read temperature and humidity values

## Usage

### Reading Sensor Data
1. Open your BLE scanner app
2. Scan for BLE devices
3. Connect to the BLE-Sensor
4. Navigate to Environmental Sensing Service
5. Read temperature and humidity characteristics

### Power Modes
The sensor operates in low-power mode between measurements to maximize battery life:
- Measurement interval: Configurable (default: 10 seconds)
- Sleep mode: Active between measurements
- BLE advertising: Periodic

## Troubleshooting

### Device Not Found
- Check battery/power supply
- Verify firmware is programmed correctly
- Ensure BLE is enabled on your device
- Check if device is in range (< 10m typically)

### Cannot Program Device
- Verify STLink connections
- Check power supply to the board
- Ensure correct target selected in programmer
- Try pressing reset button

### Incorrect Readings
- Allow sensors to stabilize (30-60 seconds)
- Check sensor calibration
- Verify sensor connections

## Next Steps

- Explore firmware customization in `firmware/README.md`
- Review hardware design in `hardware/README.md`
- Check detailed documentation in `docs/`

## Support

For issues or questions:
- Check the documentation in `docs/`
- Open an issue on GitHub
- Review existing issues for solutions
