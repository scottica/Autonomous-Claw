# Autonomous Robotic Claw


## 📌 Overview
An autonomous robotic claw system designed to detect and retrieve everyday objects with high precision. Built as a first-year engineering design project for UBC Applied Science (APSC), this system utilizes an Arduino microcontroller, ultrasonic distance sensing, and servo actuation to operate entirely hands-free. The project placed in the top 25% of all first-year APSC design teams.

## ✨ Key Features
* **Autonomous Object Detection:** Utilizes an ultrasonic sensor (using TRIG and ECHO pins) to constantly ping the environment. 
* **Distance-Triggered Actuation:** Custom C++ timing logic calculates the distance of an object in centimeters using pulse duration. When an object breaches the 100cm threshold, the servo automatically engages to close the claw.
* **Optimized Hardware Design:** Engineered with a highly durable physical casing and organized wiring layouts to maximize system reliability during repeated, high-speed physical testing. 
* **Sustainable Engineering:** Designed with modularity in mind, allowing the core electronic components to be successfully salvaged and reused by future engineering students.

## ⚙️ Technical Implementation
* **Language:** C++ (Arduino IDE)
* **Hardware:** Arduino Uno (or compatible microcontroller), Standard Servo Motor, Ultrasonic Distance Sensor (e.g., HC-SR04).
* **Control Logic:** The main loop utilizes `delayMicroseconds()` to generate clean trigger pulses, and `pulseIn()` to read the echo duration. The system dynamically writes 0° or 180° to the servo depending on the calculated spatial thresholds.

## 🚀 Usage
1. Flash the `.ino` code to the Arduino board.
2. Wire the Ultrasonic Sensor's TRIG to Pin 10 and ECHO to Pin 9.
3. Wire the Servo Motor control line to Pin 3.
4. Power the system. The claw will remain open (180 degrees) until an object is detected within 100cm, at which point it will swiftly close (0 degrees) to grasp the target.
