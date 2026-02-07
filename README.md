# 🚗 CAN-Based Collision Avoidance System (STM32F407)

## 📌 Project Overview
This project implements a **CAN-based collision avoidance system** for automotive safety applications using **STM32F407 Discovery Boards**.

Multiple sensors are used to detect unsafe driving conditions, and real-time data is exchanged between distributed nodes using the **CAN protocol**. Based on the received data, the system controls **motor operation and safety indicators** such as a buzzer.

This project was developed as part of the **PG Diploma in Embedded Systems & Design (PG-DESD)** at **Sunbeam Institute of Information Technology, Pune**.

---

## 🛠 Hardware Used
- STM32F407 Discovery Board (TX & RX nodes)
- Ultrasonic Sensor (HC-SR04) – Distance Measurement
- MQ-3 Gas Sensor
- FSR (Force Sensitive Resistor)
- CAN Transceiver (MCP2551)
- Motor Driver Module (L298N)
- DC Motor
- Buzzer
- USB-to-UART (TTL) Converter (CP2102)
- Breadboard and jumper wires

---

## 💻 Software & Tools
- STM32CubeIDE
- STM32 HAL Drivers
- Embedded C
- CAN Protocol
- UART (Minicom) for debugging

---

## 📡 System Architecture
- **TX Node (STM32F407)**  
  Reads sensor data (Ultrasonic, MQ-3, FSR) and transmits it over CAN.

- **RX Node (STM32F407)**  
  Receives CAN data and controls motor operation and safety alerts.

---

## 📦 CAN Data Frame Format
| Byte Index | Data |
|-----------|------|
| 0–1 | Distance (cm) |
| 2 | Gas sensor status |
| 3 | FSR status |
| 4–5 | FSR ADC value |

---

## ⚙️ Working Logic
- Distance below threshold → Motor OFF + alert
- Safe distance → Motor ON
- Gas detected → Safety alert via buzzer
- Force detected (FSR) → Status indication
- Live sensor data displayed on UART terminal

---

## 🎥 Demo & Output
- **Hardware setup images** available in `/Hardware`
- **UART terminal output screenshots** available in `/Media`
- **Working demo video link** available in `/Media/Working_Video_Link.txt`

---

## 📚 Author
**Sumit Bhisale**  
PG Diploma in Embedded Systems & Design (PG-DESD)  
Sunbeam Institute of Information Technology, Pune  
