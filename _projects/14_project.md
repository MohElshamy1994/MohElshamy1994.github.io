---
layout: page
title: IoT High-Power Switch Controller
description: Wi-Fi controlled high-power switching board using NodeMCU (ESP8266) with relay, optocoupler isolation, and AC-DC converter modules for remote industrial load control
img: assets/img/07-HighPowerSwitches_IOT/2.jpg
importance: 9
category: work
related_publications: false
---

## Project Overview

Designed and built an **IoT-enabled high-power switching controller** capable of remotely switching industrial loads via Wi-Fi. The board combines a NodeMCU (ESP8266) for wireless control with relay and optocoupler-isolated switching stages, multiple AC-DC converter modules for galvanic isolation, and high-current screw terminal outputs. The system was tested live with an industrial-grade contactor.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/07-HighPowerSwitches_IOT/2.jpg" title="IoT High-Power Switch Board — Close-up" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/07-HighPowerSwitches_IOT/1.jpg" title="Live Testing with Industrial Contactor" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Board close-up showing NodeMCU, relay, optocoupler switches, and AC-DC converter modules (left). Live testing setup with the board driving an industrial contactor under real load conditions (right).
</div>

---

## Key Features

- **Wi-Fi Remote Control** — NodeMCU (ESP8266) enables wireless switching from any network-connected device
- **Relay Output** — SONCE SRD-05VDC relay for one isolated high-power channel
- **Optocoupler Isolation** — transistor/optocoupler switching stages for safe control of high-voltage loads
- **AC-DC Converter Modules** — per-channel isolated power supplies for robust galvanic separation
- **Multi-Channel Outputs** — multiple high-current screw terminal pairs for independent load control
- **Industrial Load Tested** — validated live against an industrial contactor under real operating conditions

---

## Hardware Architecture

| Block | Implementation |
|---|---|
| Wi-Fi Controller | NodeMCU (ESP8266) — HTTP / MQTT remote switching |
| Relay | SONCE SRD-05VDC-SL-C — isolated mechanical switch |
| Isolation | Optocoupler / transistor array — high-voltage control isolation |
| Power | AC-DC converter modules — per-channel galvanic isolation |
| Outputs | High-current screw terminals — direct industrial load connection |

---

## Technologies & Tools

- NodeMCU / Arduino IDE — ESP8266 firmware and Wi-Fi control logic
- PCB design — custom board layout
- Relay and optocoupler circuit design
- AC-DC power supply integration
- Industrial load testing and validation

---

## Key Achievements

✅ Built a Wi-Fi controlled multi-channel high-power switching system  
✅ Implemented galvanic isolation via optocouplers and AC-DC converters  
✅ Validated live with an industrial contactor under real load  
✅ Compact single-board design integrating control, isolation, and power  
