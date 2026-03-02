---
layout: page
title: Complete Home Automation IoT System
description: Wi-Fi controlled home automation system with up to 16 relay channels — evolved through 3 versions from prototype to professional wall-installed PCB, controlling all home lighting and appliances via smartphone
img: assets/img/14- Complete Home Automation IOT Project/V3/2.jpg
importance: 16
category: work
related_publications: false
---

## Project Overview

Designed and deployed a **complete Wi-Fi home automation system** capable of controlling up to 16 independent relay channels (lighting circuits, appliances, fans, etc.) via smartphone over a local Wi-Fi network. The project evolved through 3 versions — from a hand-etched prototype to a professionally manufactured and wall-installed production board.

### Version 3 — Final Production Board

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/14- Complete Home Automation IOT Project/V3/2.jpg" title="V3 — Final 16-Channel Production PCB (Top)" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/14- Complete Home Automation IOT Project/V3/1.jpg" title="V3 — Production PCB Bottom View" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    V3 final production board — 16-channel relay board with DIN-rail compatible screw terminals, ULN2003 driver ICs, and ESP8266 Wi-Fi module socket. Top view (left) and bottom view showing clean professional PCB trace routing (right).
</div>

---

## Design Evolution

### Version 1 — Prototype

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/14- Complete Home Automation IOT Project/V1/5.jpg" title="V1 — Prototype with ESP8266, 8 Relays, and Router" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    V1 prototype — hand-etched PCB with ESP8266 (Wemos D1), 8-channel relay bank, screw terminals, and TP-Link Wi-Fi router for local network hosting.
</div>

- Hand-etched PCB
- 8 relay channels
- ESP8266 (Wemos D1) for Wi-Fi control
- External TP-Link router for network
- Basic relay switching validated

### Version 2 — Wall Installation

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/14- Complete Home Automation IOT Project/V2/1.jpg" title="V2 — Installed in Wall Electrical Box" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/14- Complete Home Automation IOT Project/V2/3.jpg" title="V2 — 16 Channels Active with Green LEDs" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    V2 installed inside a recessed wall electrical enclosure — SMPS power supply, 16 relay channels across two boards, ESP8266 module, and fully wired home circuits with color-coded cabling. Green status LEDs confirm active relay channels.
</div>

- Expanded to 16 relay channels (two relay boards)
- Installed in a wall-recessed metal electrical enclosure
- Dedicated SMPS for clean power
- Full home circuit wiring with color-coded cables
- Green channel-status LEDs

### Version 3 — Professional Manufactured PCB

- Single-board 16-channel design — all relays on one custom manufactured PCB
- ULN2003 IC arrays for reliable relay driver isolation
- DIN-rail compatible screw terminal blocks on all sides
- ESP8266 module socket for easy replacement
- Clean professional PCB fabrication — green solder mask, silkscreen

---

## Key Features

- **16 Independent Relay Channels** — control lighting circuits, fans, appliances, and more
- **Wi-Fi Control** — ESP8266 based, controllable from any smartphone on the local network
- **ULN2003 Driver Isolation** — protects MCU from relay coil back-EMF
- **SMPS Power Supply** — reliable regulated power for relay coils and logic
- **Wall Installation Ready** — V2 and V3 designed for in-wall electrical enclosure mounting
- **Scalable Architecture** — modular relay board design expandable per floor/room

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Wi-Fi Controller | ESP8266 (Wemos D1 / NodeMCU) — HTTP/MQTT relay control |
| Relay Driver | ULN2003 IC arrays — relay coil isolation and switching |
| Relays | 16× blue relays — 250VAC / 10A rated per channel |
| Power | SMPS — 5V/12V regulated rails for logic and relay coils |
| Outputs | Screw terminal blocks — live/neutral circuit connections per channel |
| Status | Green LEDs — per-channel visual confirmation |

---

## Key Achievements

✅ Designed and deployed a complete Wi-Fi home automation system  
✅ Evolved from 8-channel prototype to 16-channel professional manufactured PCB  
✅ Successfully installed in wall electrical enclosure with full home circuit wiring  
✅ Controlled all home lighting and appliances via smartphone over Wi-Fi  
✅ Three design iterations progressively improving reliability and installation quality  
