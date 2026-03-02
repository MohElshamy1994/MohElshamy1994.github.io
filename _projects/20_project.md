---
layout: page
title: Custom CNC Machine Controller — PIC Microcontroller
description: Custom-built multi-axis CNC controller using PIC microcontrollers — receives G-code from PC via parallel port, generates stepper motor sequences for X/Y/Z axis motion control
img: assets/img/13- CNC Machine/2.jpg
importance: 15
category: work
related_publications: false
---

## Project Overview

Designed and built a **custom CNC machine controller** from scratch using PIC microcontrollers. The system receives G-code motion commands from a PC via the parallel port (LPT), decodes step and direction signals, and drives stepper motors for multi-axis (X/Y/Z) CNC motion. The entire controller — including the PIC firmware, driver board, and parallel port interface — was designed and hand-etched as custom PCBs.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/13- CNC Machine/2.jpg" title="Custom PIC Controller Board — Three PIC MCUs and Stepper Driver ICs" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/13- CNC Machine/1.jpg" title="Full System — Controller, Driver Board, Parallel Port Interface, Power Supply" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Custom hand-etched PIC controller board with three Microchip PIC DIP40 microcontrollers and stepper driver IC arrays (left). Full system setup showing the PIC controller board, CNC stepper driver board, parallel port interface board, stepper motor, and power supply (right).
</div>

---

## Key Features

- **PIC Microcontroller Based** — three Microchip PIC DIP40 MCUs handling axis stepping sequences independently
- **Parallel Port (LPT) Interface** — receives step/direction signals from PC CNC software via DB25 connector
- **G-Code Compatible** — works with standard PC CNC software sending step/direction pulses
- **Multi-Axis Control** — independent X, Y, Z stepper motor channels
- **Custom Stepper Driver** — transistor/IC-based driver arrays on hand-etched PCB for each stepper coil
- **Screw Terminal Outputs** — robust motor wiring connections per axis
- **Separate Power Supply** — dedicated SMPS for stepper motor power rail

---

## System Architecture

```
PC (CNC Software / G-Code)
        │
        │ Parallel Port (LPT / DB25)
        ▼
Parallel Port Interface Board
(Step + Direction signals per axis)
        │
        ▼
PIC Microcontroller Board
(3× PIC DIP40 — one per axis)
(Decodes step pulses → generates stepper sequences)
        │
        ▼
Stepper Driver Board
(Transistor/IC arrays — drives coils)
        │
        ▼
Stepper Motors (X / Y / Z axes)
```

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| PC Interface | Parallel port (LPT) DB25 — step/direction signals from CNC software |
| Controller | 3× Microchip PIC DIP40 MCUs — one per axis, stepping sequence generation |
| Driver ICs | ULN2003 / transistor arrays — stepper coil current switching |
| Stepper Motors | Multi-axis motion — X, Y, Z CNC axes |
| PCBs | Hand-etched custom copper boards |
| Power | Dedicated SMPS — motor and logic power rails |

---

## Technologies & Tools

- PIC microcontroller (Assembly / C) — stepper pulse generation firmware
- Parallel port LPT communication — PC to controller interface
- Custom PCB etching — hand-fabricated controller and driver boards
- Stepper motor driver design
- CNC G-code motion control concepts

---

## Key Achievements

✅ Built a complete CNC controller from scratch using PIC microcontrollers  
✅ Implemented parallel port interface for G-code compatibility with standard PC CNC software  
✅ Designed and hand-etched all custom PCBs — controller, driver, and interface boards  
✅ Independent PIC per axis for reliable multi-axis stepper control  
✅ Full system validated with stepper motor motion under PC command  
