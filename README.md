# 🔗 BLE IoT Sensor Gateway with ESP32 and ThingSpeak

This project uses two ESP32 boards where one acts as a **BLE server** (with DHT11 & LDR sensors) and the other as a **BLE client gateway** to send real-time sensor data to **ThingSpeak** via Wi-Fi.

## 🚀 Features

- BLE communication between two ESP32 boards.
- Real-time temperature, humidity, and light level monitoring.
- Data logging to ThingSpeak IoT cloud.
- Serial monitoring for debugging.

---

## 🧰 Hardware Requirements

- 2× ESP32 Dev Boards
- DHT11 Sensor
- LDR + 10kΩ resistor
- Breadboard & Jumper Wires
- Power bank or USB power source
- Optional: PC with Arduino IDE for serial monitoring

---

## 🛠️ Software Requirements

- [Arduino IDE](https://www.arduino.cc/en/software)
- ESP32 Board Support via Board Manager
- Libraries:
  - `WiFi.h`
  - `HTTPClient.h`
  - `BLEDevice.h` & `BLEUtils.h`
  - `Adafruit_Sensor.h`, `DHT.h` (for DHT11)

---

## 📡 ThingSpeak Setup

1. Create a free account on [ThingSpeak](https://thingspeak.com).
2. Create a new channel with:
   - **Field 1**: Temperature & Humidity
   - **Field 2**: LDR Value
3. Copy your **Write API Key**.
4. Paste it in the code where specified (`#define THINGSPEAK_API_KEY`).

---

## 🔌 How to Operate

### 1. Update Wi-Fi Credentials
Before powering the devices, update the `WIFI_SSID` and `WIFI_PASSWORD` in the gateway code:
```cpp
#define WIFI_SSID "User"
#define WIFI_PASSWORD "1234567890"
