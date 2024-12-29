---
layout: post
title: Leading Control Systems for HyperXite
date: 2023-05-01 15:00:00 +0300
description: My work designing and implementing the control systems for HyperXite's Hyperloop pod.
img: oldteam.png
fig-caption: The HyperXite pod during a live demonstration.
tags: [Engineering, Hyperloop, Controls, Leadership, UC Irvine]
---

## About HyperXite

HyperXite is a student-led engineering team at UC Irvine, where members collaborate across disciplines to innovate in the fields of transportation and engineering. The team designs and builds advanced systems with a commitment to hands-on learning and technical excellence. For the 2023-24 season, we developed the ninth iteration of our Hyperloop pod, integrating cutting-edge technology to push the boundaries of high-speed transportation.

### My Role

I joined HyperXite as a **Control Systems Engineer**, responsible for designing and implementing key elements of the pod's control system. For the 2023-24 season, I was promoted to **Control Systems Lead**, where I directed the subteam in designing the finite state machine (FSM), building the graphical user interface (GUI), and integrating critical hardware and software components to ensure the pod operated safely and efficiently.

## Key Contributions

### Finite State Machine (FSM)

I developed the pod’s finite state machine in Python, which acts as the brain of the control system. The FSM determines the pod's operational state—such as start, stop, pre-drive, and drive—and controls transitions based on sensor inputs and system conditions. Safety was a priority, so the FSM incorporated checks for connectivity and fault detection. For instance, if a sensor detected an out-of-range value or the GUI disconnected, the FSM triggered an emergency stop to disable the motor and engage the braking system.

![fsm]({{site.baseurl}}/assets/img/fsm.png)

### Socket Communication Over Wi-Fi

I implemented a **Socket.IO server** to enable real-time communication between the HyperXite pod and the control station. The server facilitated data exchange over Wi-Fi, ensuring seamless updates between the **finite state machine (FSM)** and the GUI. Key data, including sensor readings, pod states, and error messages, were transmitted as JSON objects, allowing the operator to monitor and control the pod remotely.

To improve reliability, I optimized the socket implementation to handle high-frequency updates while minimizing latency. This communication system was essential for synchronizing the pod’s operations and providing the control team with critical insights during testing and demos.

### Wheel Encoder Optimization

I resolved an issue with the wheel encoder that was causing missed distance measurements due to timing mismatches. I implemented a faster thread within the FSM to read encoder data at a higher frequency. To ensure accessibility of the data, I converted the asynchronous thread into a synchronous one and used a mutex to extract updated values for distance and velocity, which were then integrated into the FSM and displayed on the GUI.

### Lidar Integration

To enhance safety, I integrated a **Lidar camera system** into the control system. The Lidar provided real-time depth maps to detect obstacles within the pod’s path, triggering an **emergency stop** if an object was within five feet. Initially using a Tau Lidar, I transitioned to a Garmin system with Rust integration for greater reliability. The depth data was processed by the **finite state machine (FSM)** and visualized on the GUI for operator monitoring, improving the pod’s overall safety.

### GUI Development

To enable remote control and monitoring of the pod, I led the design and implementation of a **graphical user interface (GUI)** using React and JavaScript. The GUI displays real-time data, including sensor readings, pod states, and error messages, providing operators with critical insights. I also worked with subteams to identify the most relevant data to display and refined the GUI’s design using Figma before implementing it. Communication between the GUI and the pod relied on a custom **Socket.IO server** in Python, which I developed to send and receive data seamlessly.

![gui]({{site.baseurl}}/assets/img/gui.png)

### Safety and Integration

I prioritized system safety and integration, ensuring that the pod’s braking, propulsion, and sensor systems worked cohesively. This included verifying the functionality of every subsystem and implementing robust error-handling mechanisms within the FSM to halt operations during faults.

### Technologies Used

- **Languages:** Python, JavaScript
- **Frameworks & Libraries:** React, Socket.IO, Figma, PyQt
- **Platforms:** Raspberry Pi OS, Vite
- **Tools:** Mutexes, Threading, Git, Visual Studio Code

---

## Leading the Control Systems Team

As the Control Systems Lead, I managed a team of engineers to deliver a cohesive and reliable control system for the pod. I coordinated efforts across hardware and software development, facilitated collaboration with other subteams, and documented workflows to ensure continuity for future HyperXite iterations.

My time with HyperXite was an incredible opportunity to apply my technical skills while leading a multidisciplinary team. Developing the control systems for a Hyperloop pod challenged me to think critically, prioritize safety, and innovate under tight deadlines. I’m proud to have contributed to advancing HyperXite’s mission and look forward to applying these experiences to future projects.
