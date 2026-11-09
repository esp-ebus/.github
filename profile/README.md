# esp-ebus

ESP-based Wi-Fi eBUS adapter

**Warning: Do not power your adapter from a power supply on eBus terminals - you will burn the transmit circuit (receive may still work)!**

To get more info navigate to [wiki](https://github.com/esp-ebus/esp-ebus-firmware/wiki)

`esp-ebus-firmware` is an open-source firmware for [EBUS to WiFi Adapter Module](https://danman.eu/ebus-adapter).  
It turns the adapter into a **network-connected eBUS interface** with TCP, MQTT, HTTP, and Home Assistant support — suitable for monitoring and controlling eBUS-based heating systems.

---

## What This Project Does

- 🔌 Connects to **eBUS heating systems** (Vaillant and other eBUS-compatible HVAC equipment)
- 📡 Connects the physical eBUS line to a network over **Wi-Fi**
- 🌍 Exposes eBUS traffic over **TCP sockets** compatible with tools like `ebusd`
- 📊 Publishes data to **MQTT** for smart home integration
- 🏠 Supports **Home Assistant autodiscovery**
- ⚙️ Provides a **web interface** for configuration and diagnostics

### Two firmware variants

- **Bridge** (`esp32-c3`, default) — transparent bus interface for external
  software like `ebusd` on another host. No autonomous participation.
- **INTERNAL** (`esp32-c3-internal`) — autonomous participant: polls,
  commands, MQTT/HA on-device, no external software needed.

Details: wiki [5. Bridge mode](https://github.com/danielkucera/esp-ebus/wiki/5.-Bridge-mode) and
[6. INTERNAL firmware](https://github.com/danielkucera/esp-ebus/wiki/6.-INTERNAL-firmware-current).

---

## Smart Home Integration

- Native **MQTT support**
- **Home Assistant autodiscovery**
- Seamless integration into existing automation setups
- Suitable for dashboards, logging, and energy optimization

---

## Required Hardware

This firmware **requires a compatible eBUS adapter board**, which provides:

- Proper **eBUS level shifting and electrical protection**
- Safe **bus power handling**
- Signal conditioning (PWM / comparator circuitry)
- Reliable physical connection to the eBUS line

Supported hardware revisions include multiple ESP32-based eBUS adapter boards maintained alongside this project.

> ❌ Flashing this firmware onto a generic ESP8266/ESP32 module **will not work**.

---

## Why Choose esp-ebus?

- ✅ Designed for **real eBUS adapter hardware**
- 🔓 Fully **open source**
- ⚡ Low-power, always-on operation
- 🔧 Flexible: bridge mode or INTERNAL standalone mode
- 🧩 Compatible with existing eBUS tools and ecosystems

---

