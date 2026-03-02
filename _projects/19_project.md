---
layout: page
title: Digital PID Controller — Hardware in the Loop
description: From-scratch digital PID speed controller for a DC motor with quadrature encoder feedback — modular algorithm with no Arduino library dependencies, validated with MATLAB step response plots
img: assets/img/12- Digital PID - Hardware in the loop/4.jpg
importance: 14
category: work
related_publications: false
---

## Project Overview

Implemented a **modular digital PID speed controller** for a DC motor with quadrature encoder feedback, developed entirely from scratch without using any Arduino PID library. The controller was validated using hardware-in-the-loop testing — real-time serial data streamed to MATLAB for step response analysis, demonstrating clean tracking, minimal overshoot, and near-zero steady-state error across multiple setpoint changes.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/12- Digital PID - Hardware in the loop/1.jpg" title="Hardware Setup — Arduino Mega, Cytron MDD10A, DC Motor with Encoder" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/12- Digital PID - Hardware in the loop/2.jpg" title="Full Test Rig with Power Supply" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hardware-in-the-loop test rig: Arduino Mega + Cytron MDD10A dual-channel motor driver + DC geared motor with quadrature encoder, connected to PC for real-time monitoring (left and right).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/4.jpg" title="Clean Step Response — Setpoint 0 to 1000" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/3.jpg" title="Multi-Setpoint Response — 1000 then 500" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/Picture10.jpg" title="Steady-State Speed — Flat Response with Minimal Ripple" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Step response from 0 to 1000 counts showing minimal overshoot and fast settling (left). Multi-setpoint test tracking 1000 then stepping to 500 — demonstrating accurate tracking across setpoint changes (center). Steady-state speed response showing flat, stable speed with minimal ripple (right).
</div>

---

## Key Features

- **From-Scratch PID Algorithm** — full P, I, and D term implementation in C++ without any Arduino PID library
- **Quadrature Encoder Feedback** — interrupt-driven encoder counting for accurate real-time speed measurement
- **Modular Code Architecture** — PID, encoder, and motor driver modules separated for reusability and maintainability
- **Anti-Windup** — integral windup protection to prevent saturation during large setpoint changes
- **PWM Motor Drive** — via Cytron MDD10A dual-channel 10A DC motor driver
- **Hardware-in-the-Loop Testing** — real-time serial data streamed to MATLAB for step response plotting and tuning
- **Validated Performance** — clean step response, minimal overshoot, fast settling, near-zero steady-state error

---

## PID Algorithm Implementation

All three terms implemented from scratch using the positional PID form:

- **Proportional (P)**: `Kp × error(t)`
- **Integral (I)**: `Ki × Σerror × dt` — with anti-windup clamping
- **Derivative (D)**: `Kd × (error(t) - error(t-1)) / dt` — acting on error change to avoid derivative kick

Encoder speed computed from quadrature interrupt counts per fixed time window, giving precise RPM/counts-per-second feedback.

---

## Hardware Setup

| Component | Role |
|---|---|
| Arduino Mega | PID computation, encoder interrupt reading, PWM output |
| Cytron MDD10A | Dual-channel 10A DC motor driver — bidirectional PWM drive |
| DC Geared Motor | Plant — controlled motor with shaft encoder |
| Quadrature Encoder | Speed feedback — A/B phase signals read via hardware interrupts |
| PC + MATLAB | Serial data capture and step response plotting |
| External Power Supply | Motor power rail — separate from logic supply |

---

## Results

| Metric | Result |
|---|---|
| Step response overshoot | ~2.5% (setpoint 0 → 1000) |
| Settling time | ~3 seconds |
| Steady-state error | Near zero |
| Multi-setpoint tracking | Accurate tracking on step changes (1000 → 500) |
| Steady-state ripple | Minimal — flat speed profile |

---

## Technologies & Tools

- Arduino Mega / C++ — custom PID and encoder firmware
- Cytron MDD10A — dual-channel motor driver
- MATLAB — serial data logging and step response analysis
- Hardware interrupts — quadrature encoder counting
- PWM control — variable speed motor drive

---

## Key Achievements

✅ Implemented a complete digital PID controller from scratch — no library used  
✅ Interrupt-driven quadrature encoder feedback for accurate speed measurement  
✅ Anti-windup protection for stable control across large setpoint changes  
✅ Validated with MATLAB hardware-in-the-loop step response analysis  
✅ Achieved minimal overshoot, fast settling, and near-zero steady-state error  
✅ Modular, reusable code architecture for any DC motor control application  
