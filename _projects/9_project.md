---
layout: page
title: Tatweer T-CAN — CAN Bus Debugger
description: Compact dual-channel CAN bus analyzer and debugger for automotive diagnostics, built around ESP32 and MCP2515, deployed and tested in real vehicles
img: assets/img/03-Can Bus Debugger for Cars/5.png
importance: 4
category: work
related_publications: false
---

## Project Overview

Designed and built the **Tatweer T-CAN**, a compact dual-channel CAN bus debugger for automotive diagnostics and development. The device connects directly to a vehicle's CAN bus wiring harness, captures and decodes CAN frames in real time, and transmits data wirelessly via Wi-Fi. It was successfully tested and deployed inside real vehicles.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/03-Can Bus Debugger for Cars/5.png" title="Tatweer T-CAN — Final Product" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/03-Can Bus Debugger for Cars/4.png" title="Installed in Vehicle" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final Tatweer T-CAN unit (left) and the device installed and connected to a vehicle's CAN wiring harness during in-car testing (right).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/03-Can Bus Debugger for Cars/2.png" title="PCB — Top View with ESP32" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/03-Can Bus Debugger for Cars/1.png" title="PCB — Bottom View" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/03-Can Bus Debugger for Cars/3.png" title="Size Comparison" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    PCB top view showing the ESP32-WROVER-E module and dual CAN channels (left), PCB bottom view with MCP2515 CAN controller (center), and size comparison showing the ultra-compact form factor (right).
</div>

---

## Key Features

- **Dual CAN Channels**: CAN0 and CAN1 for simultaneous multi-bus monitoring
- **ESP32-WROVER-E**: Wi-Fi connectivity for wireless frame streaming and remote access
- **MCP2515 CAN Controller**: Reliable SPI-based CAN frame decode and transmission
- **OBD-II Compatible**: Direct connection to vehicle wiring harnesses via multi-wire connector
- **USB Connectivity**: USB-C for power and firmware updates; micro-USB for auxiliary functions
- **Compact Enclosure**: Tiny black housing (Tatweer T-CAN branding) fits inside dashboards
- **Real-Vehicle Tested**: Validated by deployment and testing inside actual cars

---

## Hardware Architecture

| Component | Role |
|---|---|
| ESP32-WROVER-E | Main processor + Wi-Fi for wireless data streaming |
| MCP2515 | CAN controller (SPI interface), handles CAN0 & CAN1 |
| SPI Bus | Connects ESP32 to MCP2515 |
| Multi-wire connector | Interfaces with vehicle CAN H/L lines and power |
| USB-C port | Power input and firmware flashing |

---

## Technologies & Tools

- Altium Designer — PCB schematic and layout
- ESP32 (Arduino / ESP-IDF) — firmware development
- MCP2515 CAN library — frame parsing and filtering
- CAN bus protocol — ISO 11898 standard
- In-vehicle testing and validation

---

## Key Achievements

✅ Dual-channel CAN bus capture and decode in real time  
✅ Wireless data streaming via ESP32 Wi-Fi  
✅ Ultra-compact form factor fitting inside vehicle dashboards  
✅ Successfully deployed and validated in real vehicles  
