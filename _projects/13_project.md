---
layout: page
title: Medical Chair Controller
description: Custom electronic control circuit for a medical chair — motor-driven positioning with LCD display, push-button interface, and multi-channel actuator outputs
img: assets/img/06-Medical Chair/P4.jpg
importance: 8
category: work
related_publications: false
---

## Project Overview

Designed a **custom electronic control circuit** for a motorized medical chair, enabling precise position control of chair movements (recline, elevation, tilt) through a simple push-button interface with real-time status displayed on a 20×4 LCD screen.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/06-Medical Chair/P4.jpg" title="Medical Chair Controller — Front View with LCD" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/06-Medical Chair/Picture3.jpg" title="Medical Chair Controller — PCB Back View" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Front view showing the 20×4 LCD display, motor driver IC, DC-DC converter, push-button interface, and labeled screw terminal outputs (left). PCB bottom view showing clean trace routing and solder joints (right).
</div>

---

## Key Features

- **20×4 LCD Display** — real-time status feedback and position indication
- **Multi-Channel Motor Outputs** — 16 labeled output terminals driving chair actuators (recline, lift, tilt)
- **Push-Button Interface** — 4 tactile buttons for intuitive chair position control
- **DC-DC Buck Converter** — on-board regulated power supply for logic and motor drive
- **Motor Driver IC** — DIP package driver IC for multi-directional motor control
- **Screw Terminal Outputs** — secure connections to chair actuators and external systems
- **Compact Single-Board Design** — controller and display integrated on one PCB stack

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Display | 20×4 character LCD (204ZPA) with blue backlight |
| MCU | Microcontroller managing button input, display, and output logic |
| Motor Drive | DIP motor driver IC — bi-directional actuator control |
| Power | DC-DC buck converter — regulated rail for all subsystems |
| User Input | 4 push buttons for position commands |
| Outputs | 16-channel screw terminal bank for actuator wiring |

---

## Technologies & Tools

- PCB design — schematic capture and custom layout
- Embedded C / Arduino — firmware for motor sequencing and LCD control
- DC-DC power supply design
- Motor driver and actuator interfacing

---

## Key Achievements

✅ Designed a complete motor control solution for a medical chair  
✅ Integrated 20×4 LCD for real-time position and status feedback  
✅ 16-channel output bank supporting multiple independent actuators  
✅ Compact single-board design combining control, display, and power  
