---
layout: page
title: Smart Driving Test — Automotive Power Management Controller
description: UAE government project — centralized automotive power sequencing and protection board for smart driving test vehicles, managing startup, shutdown, fault isolation, and surge protection across all onboard subsystems
img: assets/img/04-Smart Driving Test – Automotive Power Management Controller/3.png
importance: 5
category: work
related_publications: false
---

## Project Overview

Designed a **centralized automotive power control and sequencing board** for a UAE government smart driving test vehicle. The board manages power delivery to all onboard subsystems — the test computer, router, sensors, and peripherals — with controlled startup/shutdown sequencing, fault isolation, and full automotive-grade protection.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/04-Smart Driving Test – Automotive Power Management Controller/3D.jpg" title="PDU V1.0 — Altium Designer 3D Render" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Altium Designer 3D render of the PDU V1.0 (TATWEER Innovation Lab) — showing all relay channels, blade fuse banks, MCU section, power stage, digital outputs (DQ32–DQ49), analog inputs (A1–A8), ignition input, and battery connectors.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/04-Smart Driving Test – Automotive Power Management Controller/3.png" title="Production Board — Full View" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/04-Smart Driving Test – Automotive Power Management Controller/4.png" title="Board powered up in enclosure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Assembled production board with 12+ relay channels, blade fuse banks, MCU, and DC-DC converter (left); board powered up in its installation enclosure with active relay and green status LEDs (right).
</div>

---

## Key Features

- **Intelligent Power Sequencing**: Controlled startup and shutdown of each subsystem with programmable delays to prevent brownout and boot instability
- **Multi-Channel Fused Outputs**: Individual blade fuse per channel for fault isolation and easy field maintenance
- **Relay-Based Switching**: Automotive relays route high-current loads; sequenced by MCU to prevent inrush spikes
- **Automotive Protection**: TVS diodes, surge suppression, and reverse polarity protection handle load dump (40–60V transients) and cold crank dips
- **On-Board DC-DC Conversion**: Buck converter provides regulated 5V/3.3V rails for MCU, logic, and communication circuits
- **Intelligent MCU Core**: Central microcontroller manages sequencing logic, ignition detection, fault monitoring, and watchdog supervision

---

## Power Sequencing Logic

**Startup:**
Ignition ON → Validate battery voltage → Enable DC-DC logic rail → Relay 1 (Router) ON with delay → Relay 2 (Main computer) ON → Relay 3 (Sensors) ON → Signal "System Ready"

**Shutdown:**
Ignition OFF → Send shutdown signal to computer → Wait configurable timeout → Cut high-power domains → Enter standby

This prevents file system corruption, ECU misbehavior, and data loss on power-off.

---

## Hardware Architecture

| Stage | Implementation |
|---|---|
| Input | 12V automotive battery, fuse + TVS + reverse polarity protection |
| Switching | Automotive relays (12V coil), MCU-controlled per domain |
| Fused outputs | Individual blade fuse channels, dedicated output terminals |
| DC-DC | Buck converter — 5V & 3.3V rails for logic |
| MCU | QFP microcontroller — sequencing, fault detection, watchdog |
| Interface | Terminal blocks, diagnostic/programming header |

---

## Technologies & Tools

- Altium Designer — multi-layer PCB design
- Embedded C — power sequencing firmware, fault detection logic
- Automotive EMC & protection design (load dump, cold crank, ESD)
- High-current trace sizing and thermal copper pour design

---

## Key Achievements

✅ Delivered a UAE government-grade automotive power controller  
✅ Implemented intelligent multi-channel power sequencing with relay control  
✅ Designed comprehensive automotive protection (TVS, fuses, reverse polarity)  
✅ Integrated MCU-based fault detection and watchdog supervision  
✅ Enabled safe, stable boot and shutdown of all vehicle subsystems  
