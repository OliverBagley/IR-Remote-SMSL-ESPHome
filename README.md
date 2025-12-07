# ESPHome SMSL IR Blaster

A compact ESPHome-powered infrared blaster for controlling **SMSL amplifiers** via **Home Assistant**, with optional **BME680 environmental monitoring**.

Designed to be:
- Fully stateless
- Simple and low-maintenance
- Easy to automate via standard Homeassistant automations, scenes and scripts

---

## ✅ Features

- SMSL amplifier IR control:
  - Power
  - Volume Up / Down
  - Up / Down (alias of volume)
  - Left / Right / OK
  - Input
  - EQ
  - Mute

- Home Assistant integration via ESPHome API  
- Web interface (ESPHome WebServer v3)  
- Optional **BME680 environmental sensor**:
  - Temperature
  - Humidity
  - Pressure
  - Gas Resistance (air quality)

- Optimised for **ESP8266 with 1MB flash (OTA safe)**

---

## 🛠 Hardware Used

- ESP8266 (ESP-01 1MB / D1 Mini)
- IR LED + N-channel MOSFET / Transistor driver
- BME680 sensor - I²C - _(Optional)_
- 3.3V power supply

---

## 📁 Files

| File | Description |
|------|------------|
| `ir-blaster.yaml` | Main ESPHome firmware |
| `ir-blaster-bme.yaml` | Main ESPHome firmware & BME680 |
| `lovelace-remote.yaml` | Home Assistant dashboard control card |
| `images/` | Photos of built device *future addition* |

---

## 🚀 Installation

1. Flash `ir-blaster.yaml` to your ESP8266 using ESPHome.
2. Add the device to Home Assistant.
3. Import `lovelace-remote.yaml` into your dashboard.
4. Point the IR LED at your SMSL amplifier.
5. Done ✅

---

## ⚠️ Design Notes

- This project is intentionally **stateless**.
- No volume, EQ, or power state is tracked internally.
- This prevents desync if the physical remote is used.
- All buttons always send raw IR commands.
- Intentionally kept simple to avoid over-engineering and complex state handling.

---

## 📜 License
MIT License
