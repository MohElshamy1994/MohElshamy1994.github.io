---
layout: page
title: Digital PID Controller — Hardware in the Loop & Standalone
description: DC motor speed control using two approaches — MATLAB-based hardware-in-the-loop PID and a fully standalone from-scratch PID algorithm running entirely on Arduino, both with quadrature encoder feedback and no library dependencies
img: assets/img/12- Digital PID - Hardware in the loop/4.jpg
importance: 14
category: work
related_publications: false
---

## Project Overview

This project demonstrates **two complete implementations** of a digital PID speed controller for a DC motor with quadrature encoder feedback — both developed from scratch without any Arduino PID library:

1. **Hardware-in-the-Loop (HIL)**: The PID algorithm runs in MATLAB. The Arduino acts as the hardware interface — reading the encoder and sending speed data to MATLAB via serial, while receiving the computed PWM control signal back from MATLAB to drive the motor. This setup enables rapid tuning and real-time visualization in MATLAB.

2. **Standalone Arduino PID**: The complete PID algorithm runs entirely on the Arduino itself — no PC or MATLAB needed during operation. The Arduino reads the encoder, computes all P, I, and D terms in real time, and drives the motor directly through the Cytron MDD10A motor driver.

Both implementations share the same modular code architecture and were validated on the same hardware platform.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/12- Digital PID - Hardware in the loop/1.jpg" title="Hardware Test Rig — Arduino Mega, Cytron MDD10A, DC Motor with Encoder" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/12- Digital PID - Hardware in the loop/2.jpg" title="Full Setup with External Power Supply" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hardware platform: Arduino Mega + Cytron MDD10A dual-channel motor driver + DC geared motor with quadrature encoder, connected to PC for HIL testing and standalone validation.
</div>

---

## Implementation 1 — Hardware in the Loop (MATLAB PID)

In this mode, **MATLAB runs the PID control loop**:
- Arduino reads encoder counts via hardware interrupts and sends speed over serial to MATLAB
- MATLAB computes the PID output at each timestep and sends the PWM duty cycle back to Arduino
- Arduino drives the motor via the Cytron MDD10A based on the received PWM value
- MATLAB plots the response in real time for tuning and analysis

This allows fast gain tuning (Kp, Ki, Kd) and instant step response visualization without re-flashing the Arduino.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/3.jpg" title="HIL — Multi-Setpoint Response (1000 then 500)" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/Picture10.jpg" title="HIL — Steady-State Speed Profile" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    HIL results — multi-setpoint step response tracking from 1000 to 500 counts (left); steady-state speed showing flat, stable output with minimal ripple (right). Orange = setpoint, Blue = actual speed.
</div>

---

## Implementation 2 — Standalone Arduino PID

In this mode, **the full PID algorithm runs on the Arduino**:
- Encoder speed measured locally using hardware interrupt-driven quadrature counting
- PID computation (P + I + D terms) executed in a fixed-period timer interrupt
- PWM output sent directly to the Cytron MDD10A motor driver
- No PC required during operation — fully embedded, autonomous control

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12- Digital PID - Hardware in the loop/4.jpg" title="Standalone Arduino PID — Clean Step Response (0 to 1000)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Standalone Arduino PID step response — speed ramps from 0 to setpoint 1000 with minimal overshoot (~2.5%) and fast settling (~3 seconds). Orange = setpoint, Blue = actual speed.
</div>

---

## PID Algorithm (From Scratch — No Library)

Both implementations use the same positional PID form:

- **Proportional**: `Kp × e(t)`
- **Integral**: `Ki × Σe(t) × dt` — with anti-windup clamping
- **Derivative**: `Kd × (e(t) − e(t−1)) / dt` — on error to avoid derivative kick on setpoint change

Encoder speed: quadrature A/B phase signals read via hardware interrupts, counts measured per fixed time window.

---

## Hardware Setup

| Component | Role |
|---|---|
| Arduino Mega | Encoder reading, PWM output; PID host in standalone mode |
| Cytron MDD10A | Dual-channel 10A DC motor driver — bidirectional PWM drive |
| DC Geared Motor | Controlled plant |
| Quadrature Encoder | Speed feedback via hardware interrupts |
| PC + MATLAB | HIL mode only — PID computation and real-time plotting |
| External Power Supply | Separate motor power rail |

---

## Results

| Metric | HIL (MATLAB PID) | Standalone (Arduino PID) |
|---|---|---|
| Step response overshoot | Low | ~2.5% |
| Settling time | Fast | ~3 seconds |
| Steady-state error | Near zero | Near zero |
| Multi-setpoint tracking | ✅ Validated | ✅ Validated |
| PC required at runtime | Yes (MATLAB) | No — fully autonomous |

---

## Key Achievements

✅ Two complete PID implementations — MATLAB HIL and fully standalone on Arduino  
✅ All PID math written from scratch — no Arduino or MATLAB PID toolbox libraries  
✅ Interrupt-driven quadrature encoder for accurate real-time speed feedback  
✅ Anti-windup protection for stable control across setpoint changes  
✅ Clean step response with minimal overshoot and near-zero steady-state error  
✅ Modular, reusable architecture applicable to any DC motor control application  
