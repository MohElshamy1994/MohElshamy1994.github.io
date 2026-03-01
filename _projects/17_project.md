---
layout: page
title: 200W Pure Sine Wave Inverter
description: DC-to-AC pure sine wave inverter converting 12V battery to 220V/50Hz AC using SPWM — verified on oscilloscope and load tested with multiple AC bulbs
img: assets/img/10-SineWaveInverter_200Watt/2.jpg
importance: 12
category: work
related_publications: false
---

## Project Overview

Designed and built a **200W pure sine wave inverter** converting 12V DC (battery) to 220V AC at 50Hz using Sinusoidal Pulse Width Modulation (SPWM). The output waveform was verified on an oscilloscope confirming a clean pure sine wave, and the inverter was successfully load tested powering multiple AC LED bulbs simultaneously.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/10-SineWaveInverter_200Watt/2.jpg" title="Pure Sine Wave Verified on Oscilloscope" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/10-SineWaveInverter_200Watt/1.jpg" title="Load Test — Multiple AC Bulbs Powered" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Clean 50Hz pure sine wave output captured on UNI-T oscilloscope confirming correct SPWM operation (left). Successful load test powering multiple AC LED bulbs from a 12V battery — demonstrating full 200W output capability (right).
</div>

---

## Key Features

- **Pure Sine Wave Output** — SPWM-generated clean sine wave, suitable for sensitive AC loads
- **200W Output Power** — sufficient for lighting, small appliances, and electronics
- **12V DC Input** — operates from standard automotive or sealed lead-acid batteries
- **220V / 50Hz Output** — standard Egyptian/European AC mains voltage and frequency
- **SPWM Control** — microcontroller-generated sinusoidal PWM for low harmonic distortion
- **H-Bridge Power Stage** — MOSFET H-bridge for efficient DC switching
- **Step-Up Transformer** — boosts the switched DC to 220V AC
- **Oscilloscope Verified** — sine wave output confirmed on UNI-T oscilloscope
- **Load Tested** — validated powering multiple AC LED bulbs under real load

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| DC Input | 12V battery (automotive / sealed lead-acid) |
| SPWM Generation | Microcontroller — sinusoidal PWM signal generation at 50Hz |
| Power Stage | MOSFET H-bridge — high-frequency switching of DC input |
| Transformer | Step-up transformer — low-voltage switched AC → 220V AC output |
| Output Filter | LC filter — smooths SPWM switching into clean sine wave |
| Verification | UNI-T oscilloscope — waveform capture and frequency confirmation |

---

## Technologies & Tools

- Embedded C — SPWM table generation and timer configuration
- Power electronics design — H-bridge MOSFET gate drive, dead-time control
- Transformer design and selection
- Oscilloscope measurement and waveform analysis

---

## Key Achievements

✅ Generated a pure sine wave at 220V / 50Hz from a 12V DC source  
✅ Verified clean sinusoidal output on an oscilloscope  
✅ Successfully powered multiple AC LED bulbs under full load  
✅ Implemented SPWM with correct dead-time to prevent shoot-through  
✅ Achieved 200W output power rating  
