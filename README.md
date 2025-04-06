# FPV Drone PCB Full PCB + Assembly - Work in Progress

A complete open-source FPV drone with integrated flight controller, power distribution board, and ESC on a single PCB.

## Overview

This project aims to create a FPV drone with a custom all-in-one (AIO) PCB that combines the flight controller, power distribution, and ESC functionality. Built around the STM32F411CEU6 microcontroller, this drone follows BetaFlight design requirements while providing a clean and efficient build.

## Features

- **Integrated PCB Design**
  - Flight Controller: STM32F411CEU6 (ARM Cortex M4)
  - Power Distribution: High-current paths with filtering
  - ESC: BLHeli_S/BLHeli_32 compatible 4-in-1 design
  - OSD: Integrated MAX7456 chip for on-screen display

- **Sensors**
  - MPU6500 gyroscope/accelerometer (3.3V, SPI interface)
  - BMP280 barometer for altitude hold
  - Optional GPS with integrated magnetometer

- **Power System**
  - MP2393GTL-Z DC-DC buck converter for efficient power regulation
  - Support for 3S-6S LiPo batteries (11.1V-22.2V)
  - XT-60 connector for battery input
  - 30A per motor capability (120A max total)

- **Connectivity**
  - Multiple UART ports for peripherals
  - FTDI programming interface
  - SPI for high-speed sensor communication

## Bill of Materials

| Component | Description | Specification |
|-----------|-------------|---------------|
| Frame | 3D printed carbon fiber | 5" freestyle/racing frame |
| Motors | Brushless | SpeedyBee 1800KV (recommended) |
| Battery | LiPo | 4S 1500mAh 100C (recommended) |
| Propellers | 5-inch | Matched to motor and frame |
| Camera | FPV | CCD or CMOS based on preference |
| Video Transmitter | 5.8GHz | Power output based on needs |
| Receiver | Radio control | Compatible with your transmitter |
| Antenna | 5.8GHz | Circular polarized |

## Hardware Design

### Flight Controller
- STM32F411CEU6 microcontroller
- 8MHz external crystal oscillator (YXC X50328MSB4SI)
- MPU6500 gyroscope/accelerometer
- Multiple UART ports for peripherals
- Soft-mounted sensor design

### Power Distribution
- 2oz copper for high current paths
- Filtering capacitors for clean power
- Voltage and current sensing
- Reverse polarity protection

### ESC (Electronic Speed Controller)
- BLHeli_S/BLHeli_32 compatible
- 30-35A per motor capability
- Thermal management design
- Signal filtering for noise reduction

## Software Compatibility

This drone design is compatible with:
- BetaFlight (recommended for racing/freestyle)
- INAV (for GPS functions)
- Ardupilot (for autonomous capabilities)
- PX4 (for professional applications)

## Build Requirements

### Tools
- Soldering iron and solder
- Heat shrink tubing
- Hex drivers/screwdrivers
- LiPo battery charger
- Multimeter
- KiCAD for PCB design modifications
- Zip ties
- Double-sided foam tape

### Electronics Knowledge
- Basic soldering skills
- Understanding of power systems
- Familiarity with microcontrollers
- Ability to flash firmware

## Calculations

### Power System
- Max Current = 4 motors × 30A = 120A
- Required C Rating = 120A / 1.5Ah = 80C minimum
- Flight time estimate = (1500mAh) ÷ (Average current draw) × 60 × 0.8

### Weight Budget
- Target all-up-weight: ~500g (5" freestyle quad)
- Battery weight: ~120-150g (4S 1500mAh)
- Component weight distribution accordingly

## Testing Procedures

1. Power system verification (voltage output, regulation)
2. Motor/ESC testing with servo tester
3. Sensor calibration and verification
4. Radio range and failsafe testing
5. Controlled hover tests
6. Full flight testing

## Project Timeline

1. Research and planning: 2-4 weeks
2. Component acquisition: 1-2 weeks
3. PCB design and fabrication: 4-6 weeks
4. Assembly: 1-2 weeks
5. Testing and calibration: 1-2 weeks

Total estimated project time: 9-17 weeks

## Collaboration

This project is in collaboration with ESB8. All PCB designs, firmware modifications, and build documentation are developed jointly to ensure the highest quality and performance.

## License

This project is released under the MIT License. All design files, including schematics, PCB layouts, and firmware modifications are open source and available for personal and commercial use with attribution.

## Resources

- [BetaFlight Documentation](https://betaflight.com/docs/getting-started/installation)
- [STM32F4 Reference Manual](https://www.st.com/resource/en/reference_manual/rm0383-stm32f411xce-advanced-armbased-32bit-mcus-stmicroelectronics.pdf)
- [ESB8 GitHub Repository](https://github.com/esb8)
- [Project GitHub Repository](https://github.com/your-username/esb8-fpv-drone)

## Contributing

We welcome contributions to this project! If you have suggestions, bug reports, or want to contribute code, please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---
*This FPV drone project aims to combine and create a full documentation on the latest in drone technology with custom-designed electronics to create a high-performance, reliable platform for racing, freestyle, or aerial photography.*
