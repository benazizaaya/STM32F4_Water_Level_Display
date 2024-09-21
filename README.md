# STM32F4 Water Level Measurement with LCD Display

This repository contains a project for measuring water levels using the **MH Water Level Sensor** and displaying the results on a **16x2 LCD** connected via **I2C** to the **STM32F407VG6 Discovery board**. The project continuously monitors the water level and displays the current level on the LCD in real time.

## Hardware Components
- **STM32F407VG6 Discovery Board** 
- **MH Water Level Sensor** 
- **16x2 I2C LCD Display** 
- **Wires and Breadboard**

## Features
- Measure water level using the MH Water Level Sensor.
- Display the water level readings on an LCD via I2C protocol.
- The system calculates and displays real-time water levels.

## Wiring Diagram
- **MH Water Level Sensor**:
  - VCC → 3.3V on STM32
  - GND → GND on STM32
  - Signal (S) → PA0 (or any available ADC pin)

- **I2C LCD**:
  - VCC → 5V on STM32
  - GND → GND on STM32
  - SDA → PB7 (I2C1 SDA pin on STM32)
  - SCL → PB6 (I2C1 SCL pin on STM32)

## Code Overview
The code is written in C using the **STM32 HAL** libraries. It utilizes the **ADC** to read the analog value from the MH Water Level Sensor. This value is then converted into a meaningful water level and displayed on the **I2C-based 16x2 LCD**.

### Main Steps in the Code:
1. **ADC Initialization**: The STM32 ADC is initialized to read the analog voltage from the water level sensor.
2. **I2C Initialization**: The I2C bus is initialized to communicate with the LCD.
3. **LCD Display**: The current water level is calculated and displayed on the LCD in real-time.
4. **Continuous Monitoring**: The code continuously monitors the water level, refreshing the LCD display with the updated value.

## Installation
1. Clone this repository.
2. Open the project in **STM32CubeIDE** or another compatible STM32 IDE.
3. Make sure you have configured the **ADC** for the correct pin and the **I2C** for the LCD.
4. Compile and flash the code to your STM32F407VG6 Discovery board.

## Usage
1. Connect the MH Water Level Sensor and LCD to the STM32F407VG6 Discovery board as per the wiring diagram.
2. Power up the STM32 board.
3. The water level reading will be continuously shown on the LCD

############################### Editor : Benaziza Aya #############################
