---
layout: page
title: Solar Panel Sun Tracking System
description: Dual-axis sun tracking controller that continuously orients a solar panel toward the sun to maximize power output — ATmega2560 based with MOSFET motor drivers, OLED display, and light sensor feedback
img: assets/img/11-Tracking system for solar cell system/Picture7.jpg
importance: 13
category: work
related_publications: false
---

## Project Overview

Designed and built a **dual-axis solar panel sun tracking system** that continuously rotates the solar panel to face the sun throughout the day, maximizing the harvested solar energy. The system uses light sensors to detect the sun's position and drives motor actuators to correct the panel's azimuth and elevation angles in real time. An ATmega2560 microcontroller manages the tracking algorithm, MOSFET power stage, OLED display, and user interface.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/11-Tracking system for solar cell system/Picture9.jpg" title="PCB Design — Altium 3D Render" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/11-Tracking system for solar cell system/Picture7.jpg" title="Assembled Board with MOSFET Motor Drivers" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Altium Designer 3D render showing the ATmega2560, OLED display, MOSFET driver array, backup power section, and motor terminal blocks (left). Real assembled board with heatsink-mounted MOSFETs and Nichicon 2200µF/50V power capacitors for motor drive (right).
</div>

---

## Key Features

- **Dual-Axis Tracking** — azimuth and elevation motor control for full sun tracking throughout the day
- **Light Sensor Feedback** — LDR/photodiode sensor array detects sun position and drives correction
- **MOSFET Motor Driver Stage** — high-current MOSFET H-bridge array with heatsinks for reliable motor drive
- **ATmega2560 MCU** — manages tracking algorithm, sensor reading, display, and motor control
- **OLED Display** — real-time status, tracking mode, and system information
- **Large Power Capacitors** — Nichicon 2200µF/50V × 2 for motor inrush current handling
- **Backup Power Section** — ensures continuous operation during supply interruptions
- **Push-Button Interface** — manual control and settings adjustment
- **Rotary Encoder** — parameter configuration
- **Screw Terminal Outputs** — direct motor and sensor wiring connections

---

## How It Works

Four light sensors (LDRs) are placed in a cross pattern on the solar panel. The MCU compares the light intensity across each pair:
- If the east sensor reads more light than the west → rotate panel east (azimuth correction)
- If the north sensor reads more than the south → tilt panel accordingly (elevation correction)

The MCU drives the MOSFET H-bridges to run the motors until the sensors are balanced — meaning the panel is now directly facing the sun. This loop runs continuously, ensuring maximum perpendicular irradiance on the panel throughout the day.

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| MCU | ATmega2560 — tracking algorithm, motor control, display |
| Sensors | LDR / photodiode array — sun position detection |
| Motor Driver | MOSFET H-bridge array with heatsinks — dual-axis motor drive |
| Power | Nichicon 2200µF/50V capacitors — motor inrush filtering; backup power rail |
| Display | OLED — tracking status and system info |
| User Interface | Push buttons + rotary encoder — manual control and settings |
| Outputs | Screw terminal blocks — motor connections and sensor wiring |

---

## Technologies & Tools

- Altium Designer — PCB schematic and layout
- Embedded C (AVR/Arduino) — sun tracking algorithm, PID motor control, display driver
- MOSFET H-bridge power stage design
- LDR light sensor signal conditioning

---

## Key Achievements

✅ Designed a complete dual-axis sun tracking controller from scratch  
✅ Implemented real-time light-sensor-based tracking algorithm  
✅ Designed high-current MOSFET motor driver stage with thermal management  
✅ Integrated OLED display, manual controls, and backup power on a single board  
✅ Maximizes solar panel power output by maintaining optimal sun-facing angle  
