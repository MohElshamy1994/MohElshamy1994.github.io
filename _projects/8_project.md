---
layout: page
title: Low Power Industrial IoT Controller
description: Industrial-grade IoT kit with handmade SMPS, ESP8266, and ATmega2560 for analog and digital signal interfacing — assembled in China
img: assets/img/02-Low Power IOT system/IOT Device.png
importance: 3
category: work
related_publications: false
---

## Project Overview

Designed and developed an **industrial-grade IoT controller kit** intended as a versatile platform for IoT system integration in industrial environments. The board combines a handmade switched-mode power supply (SMPS), an ESP8266 Wi-Fi module, and an ATmega2560 microcontroller into a single compact PCB capable of interfacing with both analog and digital signals. The complete assembly was manufactured in China to production quality standards.

### Assembled Production Board

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/02-Low Power IOT system/IOT Device.png" title="Low Power Industrial IoT Controller - Production Board" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fully assembled production board showing the ESP8266 Wi-Fi module, ATmega2560 microcontroller, handmade SMPS section, and extensive analog/digital I/O connectors.
</div>

---

## Key Features & Functionality

### Signal Interfacing
- **Analog Input Handling**: Dedicated analog input terminal blocks for sensor and signal acquisition
- **Digital I/O**: Multiple digital input/output ports for actuator control and digital sensing
- **Screw Terminal Connectors**: Industrial-grade terminal blocks for robust field wiring
- **Expansion Headers**: Multi-pin headers for additional modules and peripheral connections

### Wireless Connectivity
- **ESP8266 Wi-Fi Module**: AI-Thinker ESP8266MOD running at 2.4 GHz for wireless data transmission
- **IoT Ready**: Direct integration with cloud platforms, MQTT brokers, and local networks
- **OTA Capability**: Supports over-the-air firmware updates via Wi-Fi

### Processing Power
- **ATmega2560 Microcontroller**: High-pin-count AVR MCU handling real-time signal processing, control logic, and peripheral management
- **Dual-MCU Architecture**: ESP8266 handles Wi-Fi/cloud communication while ATmega2560 manages I/O and control
- **Crystal Oscillator**: External crystal for precise timing and reliable operation

### Power Supply
- **Handmade SMPS**: Custom-designed switched-mode power supply built directly on the PCB
  - Buck converter topology with power inductor (330µH)
  - Large bulk capacitors (680µF / 35V) for energy storage and filtering
  - Schottky diodes (SS34) for efficient rectification and low-loss operation
  - Low-dropout regulation for sensitive digital circuits
- **Industrial Input Range**: Designed to accept a wide DC input voltage range suitable for industrial environments

---

## Technical Implementation

### Hardware Architecture

**PCB Design:**
- Single-board integration of power, processing, and I/O functions
- Compact layout optimized for industrial enclosure mounting
- Clearly labeled board silkscreen for easy field assembly and maintenance
- Manufactured and assembled professionally in China

**Core Components:**

| Component | Part | Role |
|---|---|---|
| Wi-Fi Module | ESP8266MOD (AI-Thinker) | Wireless connectivity & IoT communication |
| Microcontroller | ATmega2560 | Real-time I/O control & signal processing |
| Power Inductor | 330µH | SMPS energy storage element |
| Bulk Capacitor | 680µF / 35V | Input filtering & energy reservoir |
| Schottky Diode | SS34 | SMPS rectification & protection |

**I/O Capabilities:**
- Screw terminal blocks along the left and bottom edge for analog signal wiring
- Pin headers on the right side for digital expansion and module stacking
- Push-button switches for local user input and reset control
- Test points for in-circuit measurement and debugging

### Power Supply Design

The on-board SMPS is a key design element, replacing a bulky external power brick with an integrated, efficient regulator:

- **Topology**: Buck (step-down) converter
- **Energy Storage**: 330µH power inductor with low DC resistance
- **Filtering**: 680µF electrolytic capacitor provides stable rail voltage
- **Rectification**: SS34 Schottky diode minimizes forward voltage drop and switching losses
- **Output**: Clean regulated DC rail powering both the ESP8266 and ATmega2560 subsystems

### Dual-MCU Communication

The ESP8266 and ATmega2560 communicate over a serial (UART) link:
- ATmega2560 handles all real-time I/O operations, sensor reading, and actuator control
- ESP8266 receives processed data from ATmega2560 and forwards it to the cloud or receives remote commands to pass back
- This separation of concerns ensures reliable real-time performance alongside robust wireless connectivity

---

## Applications

- Industrial sensor data acquisition and remote monitoring
- Smart factory I/O nodes
- Agricultural and environmental monitoring stations
- Building automation and HVAC control
- Prototype platform for IoT product development

---

## Technologies & Tools

**Hardware Design:**
- PCB design and layout (schematic capture, routing)
- Switched-mode power supply design and component selection
- Signal integrity considerations for mixed analog/digital board

**Hardware Components:**
- ESP8266MOD (AI-Thinker) — 802.11 b/g/n Wi-Fi SoC
- ATmega2560 — 8-bit AVR microcontroller, 256KB Flash, 8KB SRAM
- Custom SMPS: 330µH inductor, 680µF/35V capacitor, SS34 Schottky diodes
- Industrial screw terminal blocks and expansion headers

**Software:**
- Arduino / AVR-GCC for ATmega2560 firmware
- Arduino ESP8266 core / AT firmware for Wi-Fi communication
- MQTT / HTTP protocols for IoT cloud integration

**Manufacturing:**
- Full PCB assembly (PCBA) completed in China
- SMD and through-hole components professionally soldered

---

## Key Achievements

✅ Designed a self-contained industrial IoT platform on a single PCB  
✅ Built a custom SMPS directly on-board, eliminating the need for external power supplies  
✅ Integrated dual-MCU architecture balancing real-time control with wireless connectivity  
✅ Supported both analog and digital signal interfacing for versatile industrial use  
✅ Achieved professional-grade assembly quality through China manufacturing  
