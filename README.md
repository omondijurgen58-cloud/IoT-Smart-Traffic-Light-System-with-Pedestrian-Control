# IoT-Smart-Traffic-Light-System-with-Pedestrian-Control
Project Overview

This project is an IoT-based Smart Traffic Light System with Pedestrian Button Control using an Arduino microcontroller. It simulates a real-world traffic intersection where pedestrians can request crossing using a push button.

When the pedestrian button is pressed:

The pedestrian green LED turns ON
Vehicle traffic lights switch to RED
Vehicles stop for a fixed duration
Then the system automatically returns to normal traffic mode

This improves safety and simulates real smart-city traffic systems.

🎯 Objectives
To design an intelligent traffic light system with pedestrian control
To implement button-triggered interrupt-like behavior
To simulate real-world road crossing scenarios
To demonstrate IoT/embedded system automation
To document and visualize system behavior using GitHub
⚙️ Components Used
Arduino Uno
Red LED (Traffic)
Yellow LED (Traffic)
Green LED (Traffic)
Pedestrian Green LED
Push Button (Pedestrian request switch)
220Ω Resistors
Breadboard
Jumper wires
USB cable / power supply
Simulation software (Tinkercad / Proteus)
🧠 System Working Principle
🚗 Normal Mode (Traffic Flow)
🔴 Red ON → Vehicles stop
🟡 Yellow ON → Prepare to move/stop
🟢 Green ON → Vehicles move
🚶 Pedestrian Mode (Button Pressed)

When the pedestrian button is pressed:

🚦 Traffic lights switch to RED
🚶 Pedestrian GREEN LED turns ON
Pedestrians are allowed to cross safely
After a fixed delay, system returns to normal cycle
🔘 Pedestrian Button Function

The push button acts as a manual interrupt trigger:

If NOT pressed → normal traffic cycle continues
If pressed → system prioritizes pedestrian crossing
After delay → system resumes normal traffic operation
