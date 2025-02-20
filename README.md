# Embedded Systems C Project with FreeRTOS

This project demonstrates various technologies and techniques in embedded systems C programming using FreeRTOS. It's designed to run on a microcontroller platform and interfaces with sensors, MQTT communication, and real-time operating system concepts.

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Project Structure](#project-structure)
4. [Key Components](#key-components)
5. [Setup and Configuration](#setup-and-configuration)
6. [Usage](#usage)

## Features

- Real-time sensor data acquisition (temperature, pressure, humidity)
- MQTT communication with Ubidots cloud platform
- FreeRTOS task management and inter-task communication
- Event-driven architecture using semaphores and event groups
- Configurable sensor enabling/disabling via MQTT subscriptions
- Automatic and manual data publishing modes
- RTC (Real-Time Clock) integration for timestamping

## Technologies Used

- C programming language
- FreeRTOS
- MQTT protocol
- STM32 HAL (Hardware Abstraction Layer)
- WiFi networking
- I2C sensor communication (temperature, pressure, humidity sensors)

## Project Structure

The project consists of several key components:

- `userApp.c`: Main application file containing task definitions and MQTT setup
- FreeRTOS configuration files
- Sensor driver files (`tsensor`, `psensor`, `hsensor`)

## Key Components

### User Application (`userApp.c`)
This file contains the main application logic, including:
- Task creation for sensor data acquisition and MQTT publishing.
- Interrupt handling for user inputs and timer events.
- Communication with the Ubidots cloud platform via MQTT.

### Sensor Interfaces
The project includes interfaces for various sensors:
- **Temperature Sensor**: Reads temperature data.
- **Pressure Sensor**: Reads atmospheric pressure.
- **Humidity Sensor**: Reads humidity levels.

### MQTT Communication
The application establishes a connection to an MQTT broker to publish sensor data and subscribe to control topics.

## Setup and Configuration

1. Clone the repository:

2. Open the project in your preferred IDE (e.g., STM32CubeIDE).

3. Configure your network settings in the `userApp.c` file to connect to your WiFi network.

4. Build the project and upload it to your microcontroller.

## Usage

Once the application is running on the microcontroller:
1. The system will automatically connect to the specified WiFi network.
2. It will establish a connection to the MQTT broker.
3. The sensors will begin collecting data, which will be published to the cloud.
4. You can control sensors via MQTT messages sent to subscribed topics.

---

Feel free to modify any sections as needed or add additional information relevant to your project!
