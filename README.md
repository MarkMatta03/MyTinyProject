**README.md**
================

Table of Contents
-----------------

* [Project Overview](#project-overview)
* [Hardware Requirements](#hardware-requirements)
* [Software Requirements](#software-requirements)
* [Project Structure](#project-structure)
* [Code Explanation](#code-explanation)
* [Usage](#usage)
* [Troubleshooting](#troubleshooting)
* [Demonstration Video](#demonstration-video)

### Project Overview

This project is a simple digital clock with a voltage display feature. It uses an mbed-enabled microcontroller to drive a 4-digit 7-segment display via a shift register. The clock can be reset using a button, and the voltage reading from a potentiometer can be displayed when another button is pressed.

### Hardware Requirements

* mbed-enabled microcontroller (e.g., NUCLEO-F401RE)
* 4-digit 7-segment display (common anode)
* Shift register (e.g., 74HC595)
* 3 buttons (active low)
* 1 potentiometer
* Jumper wires
* Breadboard

### Software Requirements

* mbed OS
* C++ compiler (e.g., ARM Compiler)

### Project Structure

* `main.cpp`: The main source file containing the clock and voltage display logic.

### Code Explanation

The code is written in C++ and uses the mbed OS API. It initializes the shift register pins, button inputs, and potentiometer input. The `updateTime` function increments the seconds and minutes counters every second. The `displayNumber` function displays a 4-digit number on the 7-segment display with optional decimal point.

The main loop checks for button presses and displays either the time or the voltage reading accordingly.

### Usage

1. Connect the hardware components as described in the code comments.
2. Build and flash the code to the mbed-enabled microcontroller.
3. Press the reset button (S1) to reset the clock.
4. Press the voltage display button (S3) to display the voltage reading from the potentiometer.
5. Release the voltage display button to return to displaying the time.

### Troubleshooting

* Ensure that the shift register is properly connected to the microcontroller and the 7-segment display.
* Check that the button inputs are configured correctly (active low).
* Verify that the potentiometer is connected to the correct analog input pin.

### Demonstration Video

Watch a demonstration of the project in action: [Digital Clock with Voltage Display](https://drive.google.com/file/d/1iVbgcvUSfVfV6eocwDie0zYAPwV4wspX/view?usp=sharing)

**Example Use Cases**

* Use this project as a simple digital clock with a voltage display feature.
* Modify the code to display other types of data (e.g., temperature, humidity) using different sensors.
* Add more features (e.g., alarm, timer) to the clock.

**Commit Message Guidelines**

* Follow the standard professional guidelines for commit messages, such as:
	+ Use the imperative mood (e.g., "Add feature" instead of "Added feature").
	+ Keep the first line concise (<50 characters).
	+ Use a blank line to separate the summary from the body.
	+ Use bullet points in the body to list changes or features.
