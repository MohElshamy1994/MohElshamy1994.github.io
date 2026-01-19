---
layout: page
title: IoT Smart Home Controller
description: Multi-protocol IoT controller for home automation
img: assets/img/5.jpg
importance: 3
category: work
related_publications: false
---

## Project Overview

Developed a versatile IoT smart home controller supporting multiple communication protocols for comprehensive home automation control.

## Key Features

- **Multi-Protocol Support**: Wi-Fi, Bluetooth, Zigbee, and RF433MHz
- **Voice Control Integration**: Compatible with Alexa and Google Home
- **Mobile App Control**: Custom Android/iOS application
- **Sensor Integration**: Temperature, humidity, motion, and door sensors
- **Actuator Control**: Relays, dimmers, and motor controllers

## Hardware Design

### Core Components
- **Main Controller**: ESP32 (dual-core with Wi-Fi/BT)
- **Secondary MCU**: STM32 for real-time control tasks
- **Communication**: Zigbee module, RF transceiver
- **Power**: 5V/3.3V dual rail with LDO regulators
- **I/O Expansion**: GPIO expanders for 32+ control channels

### PCB Specifications
- **4-layer PCB design** with controlled impedance
- **Antenna Design**: On-board PCB antenna with matching network
- **ESD Protection**: TVS diodes on all exposed interfaces
- **Compact Form Factor**: 60mm x 40mm

## Software Architecture

- **Firmware**: FreeRTOS-based multi-tasking
- **Communication Stack**: MQTT protocol for cloud connectivity
- **OTA Updates**: Over-the-air firmware update capability
- **Local Storage**: EEPROM for configuration persistence

## Applications

- Lighting control (on/off, dimming, color)
- HVAC system automation
- Security system integration
- Energy monitoring and optimization
- Scene and schedule management

## Technologies Used

**Hardware**: Altium Designer, ESP32, STM32, Zigbee, RF433  
**Software**: Embedded C, FreeRTOS, MQTT  
**Tools**: Network Analyzer, RF Spectrum Analyzer
