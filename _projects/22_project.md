---
layout: page
title: Smart Wi-Fi Touch Switch
description: IoT touch switch that replaces any standard wall switch — touch-sensitive panel with LED indication, relay-based load switching, and remote control from anywhere in the world via smartphone
img: assets/img/15- Smart Wifi Toutch Switch - IOT/2.jpg
importance: 17
category: work
related_publications: false
---

## Project Overview

Designed a **smart Wi-Fi touch switch** that replaces any standard wall switch, upgrading it to a touch-sensitive panel controllable from a smartphone — from anywhere in the world. The system combines a sleek aluminum touch switch panel with green LED status indicators, an ESP8266 Wi-Fi module, a microcontroller for touch detection and command processing, and a relay board for actual load switching. No rewiring needed — it plugs directly into existing switch wiring.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/15- Smart Wifi Toutch Switch - IOT/2.jpg" title="Smart Touch Switch Panel — Green LEDs Active" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/15- Smart Wifi Toutch Switch - IOT/1.jpg" title="Controller Board — ESP8266, MCU, Relay Board, and SMPS" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Aluminum touch switch panel with dual touch zones and green LED status indicators — active channels glowing (left). Controller system: SMPS power supply, ESP8266 Wi-Fi + MCU controller board, and 8-channel relay switching board (right).
</div>

---

## Key Features

- **Touch-Sensitive Panel** — sleek aluminum wall switch panel replaces any standard switch
- **Green LED Indication** — per-channel status LEDs show ON/OFF state at a glance
- **Wi-Fi Remote Control** — ESP8266 enables ON/OFF control from smartphone anywhere in the world
- **Relay Switching** — 8-channel relay board handles actual AC load switching
- **Drop-in Replacement** — connects to existing switch wiring, no structural changes needed
- **Local Touch + Remote App** — works both as a physical touch switch and a remote IoT switch
- **SMPS Power Supply** — reliable regulated power for the entire system

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Touch Panel | Aluminum wall plate with capacitive/resistive touch zones + green LED indicators |
| Wi-Fi | ESP8266 (ESP-01) — remote control via smartphone from anywhere |
| MCU | DIP microcontroller — touch detection, relay logic, Wi-Fi command handling |
| Relay Board | 8× relays + screw terminals — AC load switching per channel |
| Power | SMPS — regulated DC supply for logic and relay coils |

---

## Technologies & Tools

- ESP8266 — Wi-Fi firmware, HTTP/MQTT remote switching
- Embedded C — touch detection and relay sequencing
- Custom PCB design — controller and relay boards
- Touch interface and LED indicator design

---

## Key Achievements

✅ Designed a complete drop-in smart switch replacing any standard wall switch  
✅ Touch-sensitive panel with green LED status indicators for intuitive use  
✅ Wi-Fi remote control from anywhere in the world via smartphone  
✅ 8-channel relay board for multi-circuit load switching  
✅ Seamlessly combines local touch control and remote IoT operation  
