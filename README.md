# IoT-Smart-Traffic-Light-System-with-Pedestrian-Control
code
#include<stdio.h>
int main() {
int red = 2;
int yellow = 3;
int green = 4;
int pedestrian = 5;
int button = 8;

void setup() {
  pinMode(red, OUTPUT);
  pinMode(yellow, OUTPUT);
  pinMode(green, OUTPUT);
  pinMode(pedestrian, OUTPUT);
  pinMode(button, INPUT_PULLUP);
}

void loop() {

  // Normal state
  digitalWrite(green, HIGH);
  digitalWrite(yellow, LOW);
  digitalWrite(red, LOW);
  digitalWrite(pedestrian, LOW);

  // Wait for button press
  if (digitalRead(8) == LOW) {

    // Green to Yellow
    digitalWrite(green, LOW);
    digitalWrite(yellow, HIGH);
    delay(1000);

    // Yellow to Red
    digitalWrite(yellow, LOW);
    digitalWrite(red, HIGH);

    // Pedestrian crossing
    digitalWrite(pedestrian, HIGH);
    delay(5000);

    // End crossing
    digitalWrite(pedestrian, LOW);

    // Keep red on briefly
    delay(1000);

    // Red to Yellow
    digitalWrite(red, LOW);
    digitalWrite(yellow, HIGH);
    delay(1000);

    // Yellow to Green
    digitalWrite(yellow, LOW);
    digitalWrite(green, HIGH);

    // Cars move for a while
    delay(8000);
  }
}
the project over view 
https://www.tinkercad.com/things/j0sZiwLGkkR-smashing-allis 
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

