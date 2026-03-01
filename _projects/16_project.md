---
layout: page
title: Elevator Floor Announcement System
description: Intelligent elevator sound system that announces floor numbers and elevator status — compatible with all Egyptian commercial elevator controllers, with 7-segment floor display and audio output
img: assets/img/09-Elevator Sound System/1.jpg
importance: 11
category: work
related_publications: false
---

## Project Overview

Designed and built an **elevator floor announcement and display system** that automatically announces the current floor number and elevator status (going up, going down, door opening) via a speaker, while simultaneously displaying the floor on a 2-digit 7-segment display. The system is fully compatible with all Egyptian commercial elevator controllers (including MAGIC and similar brands), connecting directly to the existing elevator signal wiring without any modification to the controller itself.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/09-Elevator Sound System/1.jpg" title="Final Board — Powered Up with Floor Display Active" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/09-Elevator Sound System/4.jpg" title="Live Testing with Egyptian Commercial Elevator Controller" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final assembled board powered up with the 7-segment floor display active and speaker connected (left). Live testing setup interfaced directly with a real Egyptian commercial elevator controller — floor number displayed and announcements played in real time (right).
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/09-Elevator Sound System/3.jpg" title="PCB Layout Design" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/09-Elevator Sound System/2.jpg" title="Assembled Board — Overview" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    PCB layout showing elevator signal inputs (OUT FROM ELEVATOR), segment chaining (OUT TO ANOTHER SEG), emergency input (EMERG I/P), and speaker output (left). Assembled production board (right).
</div>

---

## Key Features

- **Floor Announcement** — pre-recorded audio pronunciations of each floor number played via on-board audio amplifier and speaker
- **Elevator Status Announcements** — going up, going down, and door opening voice messages
- **2-Digit 7-Segment Display** — real-time floor number display for passengers
- **Universal Compatibility** — interfaces directly with all Egyptian commercial elevator controllers (MAGIC, and other brands) without any controller modification
- **Multi-Floor Support** — optocoupler-isolated inputs for each floor signal, supporting multi-floor buildings
- **MicroSD Audio Storage** — floor announcements stored on MicroSD card for easy customization of language and messages
- **Audio Amplifier** — on-board amplifier with heatsink driving the speaker at sufficient volume for elevator cabins
- **Emergency Input** — dedicated EMERG I/P for emergency announcement triggering
- **Segment Chaining** — OUT TO ANOTHER SEG connector for multi-segment display expansion
- **Drop-in Installation** — connects to existing elevator wiring with no changes to the elevator controller

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| MCU | DIP microcontroller — floor detection logic, audio playback control, display drive |
| Floor Inputs | Optocoupler-isolated input array — one per floor, reads elevator controller signals |
| Audio | MicroSD card reader — stores floor announcement audio files |
| Amplifier | Audio power amplifier with heatsink — drives speaker output |
| Speaker | Round speaker driver — cabin audio announcement output |
| Display | 2-digit 7-segment display — real-time floor number |
| Emergency | EMERG I/P terminal — emergency voice trigger |
| Interface | Screw terminal banks — OUT FROM ELEVATOR, OUT TO ANOTHER SEG, SPEAKER |

---

## Technologies & Tools

- PCB design — custom schematic and layout
- Embedded C / Assembly — MCU firmware for floor detection, audio sequencing, and display control
- Audio amplifier design
- Optocoupler isolation for elevator signal interfacing
- Real-world testing with Egyptian commercial elevator controllers

---

## Key Achievements

✅ Designed a complete elevator floor announcement system from scratch  
✅ Achieved full compatibility with all Egyptian commercial elevator controllers  
✅ MicroSD-based audio for easy floor announcement customization  
✅ Integrated floor display, audio amplifier, and elevator interface on a single board  
✅ Successfully tested live with a real elevator controller and speaker output  
✅ Supports multi-floor buildings with optocoupler-isolated per-floor inputs  
