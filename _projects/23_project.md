---
layout: page
title: Hospital Medical Gas Pressure Alarm System
description: PIC-based alarm system monitoring hospital medical gas pipeline lines (Oxygen, Vacuum, Air-4-bar, Air-7-bar) — detects pressure faults, provides LCD status display, visual LED indicators, and audible alarm with fault-cleared feedback
img: assets/img/16- Gas pressure alarm device for hospital/1.jpg
importance: 18
category: work
related_publications: false
---

## Project Overview

Designed and programmed a **hospital medical gas pipeline alarm system** that continuously monitors the pressure status of critical gas lines — Oxygen, Vacuum, Air at 4-bar, and Air at 7-bar. When a fault (pressure drop or line failure) is detected on any line, the system immediately triggers a visual LED alarm and an audible buzzer alert. When the fault is cleared and the line returns to normal, the system provides a confirmation feedback. All line statuses are displayed in real time on a 20×4 LCD. Programmed in **C language on a PIC microcontroller**.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/16- Gas pressure alarm device for hospital/1.jpg" title="System Running — All Gas Lines Normal (Green LED)" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/16- Gas pressure alarm device for hospital/2.jpg" title="Hardware Overview — PIC Controller, LCD, Speaker, Sensor Board" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System running with all 4 gas lines reporting NORMAL — bright green LED array and LCD showing "Oxygen Normal / Vacuum Normal / Air-4-bar Normal / Air-7-bar Normal" (left). Hardware layout showing PIC controller board, 20×4 LCD, audio amplifier board, speaker, and screw terminal sensor inputs (right).
</div>

---

## Monitored Gas Lines

| Gas Line | Pressure | Status Display |
|---|---|---|
| Oxygen (O₂) | Medical supply pressure | Normal / Fault |
| Vacuum | Suction line pressure | Normal / Fault |
| Air (Low) | 4-bar medical air | Normal / Fault |
| Air (High) | 7-bar medical air | Normal / Fault |

---

## Key Features

- **4-Channel Monitoring** — simultaneously monitors Oxygen, Vacuum, Air-4-bar, and Air-7-bar lines
- **Fault Detection** — instantly detects pressure drop or line failure on any channel
- **Fault-Cleared Feedback** — confirms when a faulty line returns to normal pressure
- **20×4 LCD Display** — real-time per-line status ("Normal" / "Fault") for all 4 gas lines
- **Visual LED Alarm** — bright green = all normal; fault triggers alarm LED state
- **Audio Alarm** — speaker/buzzer sounds immediately on fault detection
- **PIC Microcontroller** — programmed in C for reliable real-time monitoring
- **Screw Terminal Inputs** — robust connections to pressure sensor signals from each gas line

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| MCU | PIC microcontroller — C language firmware, 4-channel monitoring loop |
| Display | 20×4 LCD — real-time gas line status per channel |
| Visual Alarm | LED indicator array — green (normal) / alarm state on fault |
| Audio Alarm | Speaker + audio amplifier board — audible alert on fault |
| Inputs | Screw terminal blocks — pressure sensor signal inputs per gas line |
| Feedback | Fault-cleared confirmation — LCD and LED update when line recovers |

---

## Technologies & Tools

- PIC Microcontroller — C language firmware
- 20×4 LCD driver
- Pressure sensor signal conditioning
- Audio amplifier circuit for speaker output
- Custom PCB design

---

## Key Achievements

✅ Monitors all 4 critical hospital medical gas pipeline lines simultaneously  
✅ Instant fault detection with visual LED and audible alarm  
✅ Fault-cleared feedback confirms safe line recovery  
✅ Real-time LCD status display for all gas lines  
✅ Programmed entirely in C on a PIC microcontroller — no library dependencies  
✅ Designed for reliable continuous operation in a hospital environment  
