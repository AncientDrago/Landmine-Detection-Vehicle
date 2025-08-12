# Landmine-Detection-Vehicle
A low-cost, semi-autonomous robotic system designed to detect buried landmines using a metal detector and NodeMCU microcontroller. This project aims to support humanitarian demining efforts and defense applications by providing a scalable, wireless-enabled detection platform.

   
## 📌 Table of Contents
- [Project Overview](#project-overview)
- [System Architecture](#system-architecture)
- [Hardware Components](#hardware-components)
- [Software & Firmware](#software--firmware)
- [Setup Instructions](#setup-instructions)
- [Applications](#applications)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)


## 🧭 Project Overview

This vehicle combines a metal detector circuit with a NodeMCU (ESP8266) to identify metallic objects beneath the surface. It is mounted on a mobile platform capable of navigating terrain and transmitting detection alerts wirelessly. The system is designed to be modular, affordable, and adaptable for real-world deployment.


## 🛠️ System Architecture

```plaintext
Metal Detector → NodeMCU → Wi-Fi Transmission
                          ↓
                Motor Driver → DC Motors
                          ↓
                LED / Web Dashboard development


## 🔩 Hardware Components

| Component              | Description                                                                 | Suggested Model / Specs             |
|------------------------|-----------------------------------------------------------------------------|-------------------------------------|
| **NodeMCU ESP8266**    | Microcontroller with built-in Wi-Fi for data processing and transmission    | NodeMCU v1.0 (ESP-12E)              |
| **Metal Detector**     | Analog sensor circuit to detect buried metallic objects                     | DIY Inductive Coil or Commercial Kit |
| **Motor Driver**       | Controls direction and speed of DC motors                                   | L298N Dual H-Bridge                 |
| **DC Motors**          | Provides mobility to the vehicle                                            | 1000RPM Gear Motors              |
| **Chassis & Wheels**   | Mechanical structure for mounting components and enabling movement          | 2WD or 4WD Robot Chassis Kit        |
| **Power Supply**       | Powers NodeMCU, motors, and sensors                                         | 12V Li-ion Battery / 9V Battery Pack|
| **LEDs / Buzzer**      | Visual or audio alert when metal is detected                                | 5mm Red LED / Piezo Buzzer          |
| **Optional: Ultrasonic Sensor** | For obstacle avoidance and autonomous navigation               | HC-SR04                             |


💻 Software & Firmware
--Platform: Arduino IDE
-Libraries Used:
--ESP8266WiFi.h – for Wi-Fi communication



---

## 📄 Supporting Files

### `docs/setup_instructions.md`

```markdown
# 🛠️ Setup Instructions

## 1. Hardware Assembly
- Mount motors and wheels to the chassis.
- Connect the metal detector output to NodeMCU analog pin (A0).
- Wire the L298N motor driver to the NodeMCU digital pins and motors.
- Add LEDs or a buzzer for detection alerts.

## 2. Firmware Upload
- Open Arduino IDE.
- Install ESP8266 board manager.
- Upload `detection_vehicle.ino` from `firmware/`.

## 3. Power Supply
- Use 12V battery for motors and 5V regulated supply for NodeMCU.
- Ensure common ground between all components.

## 4. Testing
- Place metallic objects under the surface.
- Monitor serial output or LED/buzzer alerts.

