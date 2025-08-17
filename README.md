# 🌡️ Temperature & Humidity Monitoring (MQTT)

An **IoT-based monitoring system** that measures **temperature** and **humidity** in real time and transmits the data via **MQTT protocol**.  
This project is built using **ESP32/Arduino + DHT sensor**, and the data can be visualized on a dashboard or integrated into automation systems.

---

## ✨ Features
- 📡 **MQTT Communication** – lightweight & reliable data transfer
- 🌡️ Real-time **temperature & humidity** readings
- 📊 Mobile App Dashboard
- 🔔 Threshold alerts & notifications (expandable)
- ⚡ Low-power, suitable for IoT networks

---

## 🛠️ Hardware & Tools
- **ESP32** (or Arduino with WiFi)
- **DHT11 / DHT22 Sensor**
- MQTT Broker (HiveMQ)
- Optional: Node-RED / Grafana for dashboard

---

## 🔗 System Architecture
```mermaid
flowchart LR
  Sensor[DHT11/DHT22 Sensor] --> |Data| ESP32
  ESP32 --> |MQTT Publish| Broker((MQTT Broker))
  Broker --> |Subscribe| Dashboard[Dashboard / App]
