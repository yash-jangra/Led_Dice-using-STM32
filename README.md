# STM32 LED Dice Simulator

This project simulates a dice roll using an STM32 microcontroller. When a button is pressed, a random dice value (between 1 and 6) is generated, and the result is displayed using LEDs connected to the GPIO pins of the microcontroller.

## Table of Contents
- [Introduction](#introduction)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Pin Configuration](#pin-configuration)
- [Project Setup](#project-setup)
- [Code Overview](#code-overview)
- [Usage](#usage)
- [License](#license)

## Introduction
This project demonstrates the use of an STM32 microcontroller to simulate a dice roll. The program uses a button interrupt to trigger the dice roll, generates a random number using the standard C library, and lights up the corresponding LEDs to display the result.

## Hardware Requirements
- STM32F4xx series microcontroller (tested on STM32F411CEU6)
- 7 LEDs connected to GPIO pins PA1 through PA7
- Push button connected to GPIO pin PA0
- Resistors for LEDs (typically 220Ω)
- Breadboard and jumper wires

## Software Requirements
- STM32CubeIDE
- HAL Library

## Pin Configuration
- **PA0**: Push button (configured as external interrupt)
- **PA1-PA7**: LEDs (configured as output)
  
![image](https://github.com/user-attachments/assets/76a67704-1c11-41f3-926c-5c0a9afdcd12)

Refer this while setting up your external LEDs on Breadboard

## Project Setup
1. Clone the repository to your local machine.
2. Open the project in STM32CubeIDE.
3. Configure the GPIO pins as specified above.
4. Build and flash the project to your STM32 board.

## Code Overview
- **main.c**: Contains the main program logic for the dice simulation.
- **ALL_OFF()**: Turns off all LEDs.
- **HAL_GPIO_EXTI_Callback()**: Interrupt handler for the button press.

## Usage
1. Press the button connected to PA0.
2. The LEDs will light up according to the randomly generated dice value.
3. The result will be displayed for 3 seconds before turning off.

## License
This project is licensed under the MIT License.
