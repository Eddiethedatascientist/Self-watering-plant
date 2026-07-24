# Self-watering-plant repository description
This repository holds the source code for the the self watering plant embedded systems, which the code is loaded into a raspberry pico to control the entire systems.

# Smart Self-Watering Plant System

A smart plant watering system built using **Raspberry Pi Pico** and **MicroPython**.

The system automatically waters a plant based on soil moisture while monitoring the available water level to prevent the pump from running dry.
<img width="1542" height="2047" alt="full package" src="https://github.com/user-attachments/assets/b69a7a5c-7dde-4fc2-89f8-17e943638890" />


## Project Overview

This project was developed as an embedded systems project.

The Raspberry Pi Pico continuously monitors both the soil moisture and the water reservoir level. Based on these sensor readings, it decides whether the water pump should be activated.

The system also provides visual feedback through LEDs to indicate its current operating status.

---

## Features

- Automatic plant watering
- Soil moisture monitoring
- Water reservoir level detection
- Pump protection against dry running
- LED status indicators
- Implemented entirely in MicroPython
<img width="1542" height="2047" alt="embedded 2" src="https://github.com/user-attachments/assets/3a8a5759-f520-4fb6-aabe-e33abc39d951" />
---

## Hardware Components

- Raspberry Pi Pico
- Capacitive Soil Moisture Sensor V1.0
- Ultrasonic Distance Sensor
- Water Pump (5V)
- 4 LEDS
- Breadboards and 5V power supply
- Relay
- Resistors
- Jumper cables
<img width="1152" height="2048" alt="embedded 1" src="https://github.com/user-attachments/assets/8e87bf27-e4ff-4b76-acfb-4355fe047368" />

## System Logic

The watering process follows these rules:

1. Read the soil moisture sensor.
2. Measure the water level using the ultrasonic sensor.
3. If the soil is dry **and** there is sufficient water in the reservoir:
   - Turn the water pump ON.
4. If the soil is already wet:
   - Turn the pump OFF.
5. If the water reservoir is empty:
   - Keep the pump OFF regardless of soil moisture.
6. 4 LEDs lights are adjusted based on the current conditions


+----------------------+        +----------------------+
| Soil Moisture Sensor |        | Ultrasonic Sensor    |
+----------+-----------+        +----------+-----------+
           \                         /
            \                       /
             \                     /
              v                   v
           +---------------------------+
           |     Raspberry Pi Pico     |
           +-------------+-------------+
                         |
          +--------------+--------------+
          |                             |
          v                             v
 +-------------------+        +-------------------+
 |    Water Pump     |        |   Status LEDs     |
 +-------------------+        +-------------------+

<img width="1277" height="671" alt="simulation" src="https://github.com/user-attachments/assets/f53ad549-e148-42de-b470-c4269c4aadf9" />

---

## LED Indicators

The LEDs provide instant feedback about the system status.

Examples include:

- Pump ON
- Pump OFF
- Water available
- Water reservoir empty

---

## Technologies

- MicroPython
- Raspberry Pi Pico
- Embedded Programming
- Sensor Integration

---

## My Contribution

I was responsible for the embedded software implementation.

My work included:

- Programming the Raspberry Pi Pico using MicroPython
- Reading and processing sensor data
- Implementing the automatic watering logic
- Controlling the water pump
- Managing the LED status indicators

---

## Learning Outcomes

Through this project I gained experience in:

- Embedded programming
- Sensor interfacing
- Real-time decision making
- Hardware and software integration
- MicroPython development
- State-based control logic

---

## Future Improvements

Possible future improvements include:

- OLED display
- Mobile application
- Wi-Fi monitoring
- Data logging
- Remote control
- Adjustable moisture thresholds

---

## Author

Eddie Nguyen

Computer Science and Engineering

University of Oulu
