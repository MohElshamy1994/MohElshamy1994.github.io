---
layout: page
title: Contactless Elevator Floor Selector
description: Touchless elevator floor selection system using capacitive proximity sensing — designed in Altium Designer and programmed with Arduino IDE
img: assets/img/05- contactless switches/Picture2.jpg
importance: 7
category: work
related_publications: false
---

## Project Overview

Designed a **contactless elevator floor selection system** that allows passengers to select floors without physically touching any button. Using capacitive proximity sensing, the system detects hand gestures near the panel and triggers the corresponding floor relay — eliminating the need for physical contact, which is especially valuable in hygiene-sensitive environments.

Designed in **Altium Designer** and programmed with **Arduino IDE**.

<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/05- contactless switches/Picture2.jpg" title="Contactless Elevator Floor Selector — Assembled Board" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Assembled board showing the multi-channel capacitive sensing array with blue sensitivity trim potentiometers, central MCU, transistor output stage, and screw terminal connections to elevator control wiring.
</div>

---

## Key Features

- **Contactless Operation** — capacitive proximity sensors detect hand presence without physical touch
- **Multi-Channel** — supports multiple floors, each with an independent sensing channel
- **Adjustable Sensitivity** — blue trim potentiometers allow per-channel calibration for reliable detection
- **Transistor Output Stage** — drives existing elevator relay wiring directly
- **Screw Terminal Outputs** — easy integration with existing elevator control panels
- **Arduino-based Firmware** — flexible and easily configurable logic

---

## How It Works

Each floor button is replaced by a capacitive sensor. When a hand is brought close to the sensor zone, the capacitance change is detected by the MCU. After debounce confirmation, the corresponding output transistor is triggered — simulating a button press to the elevator controller — without any physical contact.

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Sensing | Capacitive proximity sensors — one per floor channel |
| Sensitivity | Blue trim potentiometers for per-channel threshold tuning |
| MCU | Arduino-compatible QFP microcontroller |
| Output | Transistor array driving elevator relay inputs |
| Connections | Green screw terminal blocks for elevator wiring integration |

---

## Technologies & Tools

- **Altium Designer** — schematic and PCB layout
- **Arduino IDE** — firmware development
- Capacitive sensing and signal conditioning
- Multi-channel transistor output design

---

## Key Achievements

✅ Enabled fully touchless elevator floor selection  
✅ Multi-channel design supporting multiple floors on a single board  
✅ Per-channel sensitivity adjustment for reliable real-world performance  
✅ Drop-in integration with standard elevator control wiring  
✅ Designed in Altium Designer and programmed with Arduino IDE  
