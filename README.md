# HCSR04 Distance Measurement with 7 Segment Display
This project uses an HCSR04 ultrasonic sensor to measure distance and displays the distance on a 7 segment display. The 7 segment display shows the last digit of the measured distance (x % 10).

## Getting Started
To get started with this project, you will need the following hardware and software components:
- STM32 microcontroller (tested on STM32F407G-DISC1)
- HCSR04 ultrasonic sensor
- 7 segment display
- Jumper wires
- Breadboard
- STM32CubeIDE (tested on version 1.8.0)

## How It Works
The HCSR04 sensor measures distance by sending out an ultrasonic pulse and measuring the time it takes for the pulse to bounce back. The STM32f4 board sends a trigger signal to the sensor using a GPIO pin and waits for the echo signal to return. The time difference between the trigger and echo signals is used to calculate the distance using the formula:
>**distance = speed of sound * time / 2**

The STM32 board receives the distance measurement from the sensor and extracts the last digit using the modulo operator (distance % 10). The STM32 board then sends the last digit to the 7 segment display, which shows the digit using the appropriate segments.

## Usage
- Open the project in STM32CubeIDE.
- Build the project and flash it onto the STM32F4 board.
- The HCSR04 sensor will start measuring the distance and the 7-segment display will show the last digit of the distance.
