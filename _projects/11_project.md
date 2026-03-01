---
layout: page
title: Multi-Protocol Data Logger Kit
description: Industrial data logger supporting RS485, RS232, GPRS, and Wi-Fi with 16 digital inputs, 16 analog inputs, backup battery, and smart charger — designed in Altium Designer
img: assets/img/04- Data Logger Device/2.jpg
importance: 6
category: work
related_publications: false
---

## Project Overview

Designed a complete **industrial data logger kit** providing a unified solution for multi-protocol communication and data acquisition. The kit integrates RS485, RS232, GPRS, and Wi-Fi connectivity alongside 16 digital inputs, 16 analog inputs, onboard MicroSD logging, backup battery with smart charging, and comprehensive protection circuits — all designed in Altium Designer.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/04- Data Logger Device/3D.jpg" title="Data Logger — Altium Designer 3D Render" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Altium Designer 3D render showing the full board layout — Wi-Fi module, MCU, relay, GPRS module, RS232 DB9 connector, 16-channel digital inputs bank, and all screw terminal I/O connections.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/04- Data Logger Device/2.jpg" title="Data Logger — Top View" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/04- Data Logger Device/3.jpg" title="Data Logger — Detail View" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/04- Data Logger Device/4.jpg" title="Data Logger — Full Board Overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Assembled data logger kit showing the GPRS A6 module, ESP8266 Wi-Fi module, relay outputs, MCU, RS232 DB9 connector, MicroSD adapter, backup power section, and 16-channel screw terminal banks for digital and analog I/O.
</div>

---

## Key Features

### Communication Protocols
- **RS485** — industrial serial communication via screw terminal interface
- **RS232** — standard serial via DB9 connector
- **GPRS** — cellular data transmission for remote monitoring
- **Wi-Fi** — wireless local connectivity via ESP8266 module

### I/O Capabilities
- **16 Digital Inputs** — screw terminal bank for discrete signal acquisition
- **16 Analog Inputs** — screw terminal bank for sensor and signal monitoring
- **MicroSD Card** — onboard data logging and local storage

### Power System
- **Backup Battery** — ensures continuous operation during power outages
- **Smart Battery Charger** — intelligent charging with battery level indication LEDs

### Protection
- **Short Circuit Protection** — safeguards all output and input channels
- **Reverse Polarity Protection** — prevents damage from incorrect wiring
- **ESD Protection** — on all external-facing interfaces

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Main MCU | QFP microcontroller — I/O control, protocol handling, logging |
| Wi-Fi | ESP8266 module — wireless data transmission |
| Cellular | GPRS module — remote data upload |
| Serial | RS232 via DB9, RS485 via screw terminals |
| Storage | MicroSD card adapter for local data logging |
| Digital I/O | 16-channel screw terminal bank |
| Analog I/O | 16-channel screw terminal bank |
| Power backup | Battery + smart charger with level indicators |

---

## Technologies & Tools

- **Altium Designer** — full schematic capture and PCB layout
- Embedded C — firmware for data acquisition and multi-protocol communication
- RS485 / RS232 / GPRS / Wi-Fi protocol implementation
- Industrial protection design (ESD, reverse polarity, short circuit)

---

## Key Achievements

✅ Unified multi-protocol platform (RS485, RS232, GPRS, Wi-Fi) on a single board  
✅ 16 digital + 16 analog inputs for comprehensive industrial data acquisition  
✅ Onboard MicroSD logging for offline and standalone operation  
✅ Smart battery charger with level indication for reliable backup power  
✅ Full protection suite — ESD, reverse polarity, and short circuit  
✅ Designed entirely in Altium Designer  
