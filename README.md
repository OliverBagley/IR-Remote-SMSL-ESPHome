# ESPHome SMSL IR Blaster

A compact ESPHome-powered infrared blaster for controlling **SMSL amplifiers** via **Home Assistant**, with optional **BME680 environmental monitoring**.

Designed to be:
- ✅ Fully stateless (no IR desync issues)
- ✅ OTA-safe for ESP8266 (ESP-01 1MB)
- ✅ Reliable even when using the physical remote
- ✅ Simple and low-maintenance

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
- IR LED + N-channel MOSFET driver
- BME680 sensor (I²C)
- 3.3V power supply

---

## 📁 Files

| File | Description |
|------|------------|
| `ir-blaster.yaml` | Main ESPHome firmware |
| `lovelace-remote.yaml` | Home Assistant dashboard control card |
| `images/` | Optional wiring diagrams & photos |

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

---

## 📷 Optional Enhancements

- Custom enclosure
- Multiple IR LEDs for room coverage
- Additional appliance control (TV, DAC, etc.)
- Long-press volume via Home Assistant automations

---

## 📜 License
MIT License
