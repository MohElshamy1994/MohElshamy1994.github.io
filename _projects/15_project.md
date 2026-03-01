---
layout: page
title: Parallel PID Controller Kit
description: Analog parallel PID controller educational kit designed for Menoufia University (Faculty of Engineering) — with companion Position & Speed Control board, hardware P/I/D tuning potentiometers, and motor driver stage
img: assets/img/08-PID Controller Kit/Real.jpg
importance: 10
category: work
related_publications: false
---

## Project Overview

Designed a **parallel analog PID controller educational kit** for the Faculty of Engineering at Menoufia University. The kit provides a hands-on hardware platform for learning and demonstrating closed-loop PID control, with independent hardware-adjustable Proportional, Integral, and Derivative stages, a feedback section, and an integrated motor driver. A companion **Position & Speed Control Kit** was also designed to interface with motors and encoders.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/08-PID Controller Kit/3D.png" title="Parallel PID Controller Kit — PCB Design Render" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    PCB design render of the Parallel PID Controller Kit showing the labeled Setpoint (SP), Proportional (P), Derivative (D), Feedback (FB), Current Sensing (C.S), and Driver sections — each with dedicated tuning potentiometers.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/08-PID Controller Kit/Real.jpg" title="Manufactured PCBs — PID Kit (left) and Position & Speed Control Kit (right)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Manufactured black PCBs — the main Parallel PID Controller Kit (left) and the companion Position & Speed Control Kit with Motor and Encoder interfaces (right).
</div>

---

## Key Features

- **Parallel PID Architecture** — independent analog P, I, and D signal paths summed at the output for true parallel implementation
- **Hardware Tuning** — dedicated trim potentiometers for Setpoint (SP), P, I, D, and feedback gain — adjustable in real time
- **Error Signal Display** — visual error indicator for real-time control observation
- **Current Sensing (C.S)** — built-in current monitoring for the controlled plant
- **Integrated Driver Stage** — on-board motor/actuator driver for direct plant connection
- **ON/OFF Control** — system enable switch for safe operation
- **Companion Position & Speed Control Kit** — second board with Motor and Encoder IP interfaces for position and velocity control experiments

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Setpoint (SP) | Potentiometer-set reference input |
| Proportional (P) | Analog op-amp stage with trim pot gain adjustment |
| Integral (I) | Analog integrator stage with trim pot time constant |
| Derivative (D) | Analog differentiator stage with trim pot tuning |
| Feedback (FB) | Sensor feedback conditioning and summation |
| Error | Error signal computation and visual indicator |
| C.S | Current sensing for load monitoring |
| Driver | Motor/actuator driver stage for plant control |
| Companion Kit | Position & Speed Control board — Motor + Encoder interfaces |

---

## Technologies & Tools

- Altium Designer — PCB schematic and layout
- Analog circuit design — op-amp based P, I, D stages
- Motor driver and power stage design
- Control systems theory — parallel PID implementation

---

## Key Achievements

✅ Designed a complete analog parallel PID controller for university education  
✅ Hardware-adjustable P, I, D gains for real-time closed-loop experimentation  
✅ Integrated current sensing and motor driver on a single board  
✅ Designed companion Position & Speed Control Kit for motor/encoder experiments  
✅ Manufactured and delivered to Menoufia University Faculty of Engineering  
