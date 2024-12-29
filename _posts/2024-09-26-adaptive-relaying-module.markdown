---
layout: post
title: Adaptive Relaying Module
date: 2024-09-26 10:00:00 +0300
description: A deep dive into the senior design project I’m developing with my team at UCI, focusing on dynamic fault detection, inter-device communication, and robust circuit mapping.
img: adaptive.png
tags: [UCI, Engineering, Automation, Raspberry Pi]
---

As part of my senior design project for my Computer Science and Computer Engineering degree at UCI, I’m working alongside three other students to develop a system designed to enhance power grid reliability by automating relay settings, detecting and isolating faults, and efficiently rerouting power during disruptions.

This project runs over two quarters (Fall 2024–Winter 2025) and tackles the complex challenges of protective relaying and fault isolation in power distribution systems.

![Test Bench]({{site.baseurl}}/assets/img/adaptive-relaying.jpg)

## Key Highlights

1. Inter-Device Communications

   A reliable communication framework is essential to coordinate the test bench's modules. My primary responsibility has been implementing and refining the communication protocols between the Raspberry Pi 5 and the Pi Pico-based modules, which include:

   - Pico-Based Circuit Breakers: These monitor power line currents and control relay states.

   - Automatic Reclosers: These manage relay state transitions to maintain grid stability.

   - Vacuum Reclosers: These handle relay operations and current monitoring.

   Initially, I tested Wi-Fi for communication but found it unreliable in environments with multiple devices. I then explored Bluetooth and implemented a Python class on the Raspberry Pi that creates individual objects for each Pico, enabling efficient read/write operations over Bluetooth. While functional, Bluetooth still has inconsistencies, prompting me to develop a UART-based wired backup solution for additional reliability.

2. Wiring and Test Bench Design

   Our prototype simulates real-world power distribution lines using 18AWG wiring, ceramic resistors, and relay modules. The design includes elements like feeder relays, vacuum reclosers, and current sensors. Wiring has been a meticulous process, ensuring safety and functionality while handling voltage requirements for different components.

3. Software

   Dynamic Circuit Mapping and Fault Isolation:

   We’ve built a circuit mapping program in Python that visualizes circuit configurations in real time using data from CSV files. This module actively updates short-circuit duty values, helping us pinpoint fault locations and adjust settings dynamically. Future enhancements will incorporate fault probabilities and segment-specific data for greater accuracy.

   Module Control:

   I developed and refined the code that powers the individual modules of our adaptive relaying system. Using C++ and MicroPython, I created software to control relays, monitor current readings via INA219 sensors, and ensure seamless interaction with the central Raspberry Pi 5. Each module—whether a circuit breaker, automatic recloser, or vacuum recloser—operates autonomously while communicating critical data to the central system. My work included designing modular, reusable code structures to simplify updates and debugging, laying the foundation for a scalable and reliable protection system. This software ensures the test bench operates accurately and adapts dynamically during fault simulations.

## Continuation

In the Winter quarter, we’ll focus on:

- Automated Protection Settings: Developing algorithms to modify relay settings dynamically.
- Expanded Testing: Incorporating fault simulations to verify the system’s real-time adaptability.
- Scalability: Ensuring the system can handle complex grid configurations and multiple fault scenarios.

This project has been an incredible opportunity to apply my skills in embedded systems, automation, and data-driven decision-making, while solving real-world engineering challenges. I’m excited to see how our efforts will contribute to safer, smarter power systems.

### Technologies Used

- Languages: Python
- Frameworks & Libraries: Pandas, Matplotlib, MicroPython
- Platforms: Raspberry Pi Pico W, Raspberry Pi 5
- Tools: Visual Studio Code, Thonny IDE, Bluetooth communication standards (IEEE 802.15.1)

![Poster]({{site.baseurl}}/assets/img/yyy.jpg)
