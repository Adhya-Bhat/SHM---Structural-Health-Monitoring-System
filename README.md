# Structural Health Monitoring System using ESP32

A real-time Structural Health Monitoring (SHM) system built using ESP32, load cells, MPU6050, vibration sensing, and environmental monitoring. The system continuously monitors structural conditions such as load imbalance, tilt, vibration, temperature, and humidity, then visualizes the readings through a mobile-friendly Progressive Web App (PWA).

This project was designed for smart infrastructure monitoring applications such as:

* Bridges
* Dams
* Flyovers
* Industrial support structures
* Smart city infrastructure
* Disaster prevention systems

---

# Features

## Real-Time Monitoring

* Dual HX711 load cell monitoring
* MPU6050 tilt detection
* SW420 vibration sensing
* DHT11 environmental monitoring

## Intelligent Structural Alerts

The system detects:

* Structural overload
* Load imbalance
* Dangerous tilt
* Continuous vibration
* Sensor failures
* Environmental anomalies

## Mobile Dashboard

* Live graphs
* Mobile responsive UI
* Progressive Web App (PWA)
* Installable on phones
* QR-code-based quick access
* Demo simulation locations

## Fault Tolerance

* Sensor fault handling
* Connection diagnostics
* Startup stabilization logic
* False-alarm reduction

## Public Safety Alert Preview

The system generates automatic public safety warning messages when dangerous conditions are detected.

---

# Hardware Components

| Component              | Quantity |
| ---------------------- | -------- |
| ESP32                  | 1        |
| HX711 Module           | 2        |
| Load Cell              | 2        |
| MPU6050                | 1        |
| SW420 Vibration Sensor | 1        |
| DHT11                  | 1        |
| Breadboard / PCB       | 1        |
| Jumper Wires           | Multiple |
| Power Supply           | 1        |

---

# Pin Connections

## DHT11

| DHT11 | ESP32  |
| ----- | ------ |
| VCC   | 3.3V   |
| GND   | GND    |
| DATA  | GPIO 4 |

## Vibration Sensor

| SW420 | ESP32   |
| ----- | ------- |
| VCC   | 3.3V    |
| GND   | GND     |
| OUT   | GPIO 27 |

## HX711 Node 1

| HX711 | ESP32   |
| ----- | ------- |
| DT    | GPIO 32 |
| SCK   | GPIO 33 |

## HX711 Node 2

| HX711 | ESP32   |
| ----- | ------- |
| DT    | GPIO 25 |
| SCK   | GPIO 26 |

## MPU6050

| MPU6050 | ESP32   |
| ------- | ------- |
| SDA     | GPIO 21 |
| SCL     | GPIO 22 |
| VCC     | 3.3V    |
| GND     | GND     |

---

# Software Stack

## Embedded

* Arduino IDE
* ESP32 Arduino Core
* C++

## Web Dashboard

* HTML
* CSS
* JavaScript
* Canvas API
* Progressive Web App

## Communication

* WiFi
* HTTP Web Server

---

# Arduino Libraries Required

Install the following libraries before uploading:

```cpp
WiFi
WebServer
Wire
HX711
DHT sensor library
Adafruit MPU6050
Adafruit Unified Sensor
```

---

# Installation

## 1. Clone Repository

```bash
git clone https://github.com/yourusername/structural-health-monitor-esp32.git
```

---

## 2. Open Arduino Project

Open:

```bash
structural-health-monitor-esp32/src/structural_health_monitor.ino
```

---

## 3. Install ESP32 Board Package

Arduino IDE:

```text
File → Preferences
```

Additional Boards Manager URL:

```text
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```

Then:

```text
Tools → Board Manager → ESP32
```

Install ESP32 package.

---

## 4. Configure WiFi

Inside the code:

```cpp
const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";
```

---

## 5. Upload Code

Select:

```text
Board: ESP32 Dev Module
```

Then upload the sketch.

---

# Running the System

After boot:

```text
Dashboard: http://<ESP32-IP>
```

Example:

```text
http://192.168.0.105
```

Open the IP address on any phone or laptop connected to the same WiFi network.

---

# Dashboard Features

## Live Sensor Cards

* Node 1 Load
* Node 2 Load
* Vibration
* Tilt
* Temperature
* Humidity

## Real-Time Graphs

* Load trends
* Vibration activity
* Tilt monitoring
* Environmental changes

## Structural State Classification

| State   | Meaning                  |
| ------- | ------------------------ |
| Normal  | Safe readings            |
| Warning | Early anomaly detected   |
| Danger  | Structural risk detected |
| Waiting | Startup stabilization    |

---

# Alert System

The system automatically generates:

* Structural overload warnings
* Public safety notices
* Load imbalance alerts
* Tilt danger warnings
* Sensor connection diagnostics

---

# Example Use Cases

## Smart Bridges

Monitor:

* Traffic stress
* Uneven load
* Structural vibration
* Support tilt

## Dams

Monitor:

* Gate stress
* Support instability
* Abnormal vibration

## Industrial Infrastructure

Monitor:

* Machine support frames
* Steel structures
* Storage systems

---

# Future Improvements

## Cloud Integration

* MQTT

## AI-Based Analytics

* Predictive maintenance
* Failure prediction
* Anomaly detection
* Structural fatigue estimation

## Advanced Networking

* ESP-NOW
* LoRa
* Mesh communication

## Hardware Improvements

* Solar power
* Waterproof casing
* Battery backup
* Industrial-grade sensors

---

# Project Architecture

```text
Sensors
   ↓
ESP32 Data Acquisition
   ↓
Threshold Analysis
   ↓
Alert Generation
   ↓
Web Dashboard
   ↓
Public Safety Notifications
```

---

# Folder Structure

```text
SHM-Structural-Health-Monitoring-System/
│
├── README.md
├── LICENSE
├── .gitignore
├── src/
│   ├── structural_health_monitor_pwa.ino
│   ├── structural_health_monitor_basic_website.ino

```

---

# Demo Description

This project includes simulation modes for:

* KRS Dam
* Mandya Bridge
* Mysuru Flyover
* Cauvery Check Dam
* Krishna River Bridge

The simulated demo modes help demonstrate:

* Structural overload
* Dangerous tilt
* Vibration events
* Public safety alerts

without requiring physical damage conditions.

---

# Acknowledgements

* Espressif ESP32
* Adafruit Sensor Libraries
* Arduino Community
* Open-source IoT ecosystem

---

# Star the Repository

If you found this project useful, consider starring the repository.
