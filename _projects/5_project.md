---
layout: page
title: Battery Management System (BMS)
description: Intelligent BMS for lithium-ion battery packs
img: assets/img/11.jpg
importance: 5
category: work
related_publications: false
---

## Project Overview

Developed a comprehensive Battery Management System (BMS) for lithium-ion battery packs used in electric vehicles and energy storage applications.

## Core Functions

- **Cell Monitoring**: Individual cell voltage and temperature monitoring
- **State Estimation**: Real-time SoC (State of Charge) and SoH (State of Health)
- **Balancing**: Active cell balancing for optimal pack performance
- **Protection**: Overvoltage, undervoltage, overcurrent, and thermal protection
- **Communication**: CAN bus interface for system integration

## Hardware Design

### Monitoring Circuit

- **AFE IC**: Specialized battery management IC (e.g., BQ76940, LTC6811)
- **Cell Count**: Supports 4S to 16S configurations
- **Voltage Accuracy**: ±5mV per cell
- **Temperature Sensors**: NTC thermistors on each cell group
- **Current Sensing**: High-precision shunt-based measurement

### Control & Processing

- **MCU**: STM32 with CAN interface
- **Balancing**: MOSFET-based active balancing circuit
- **Power Supply**: Isolated DC-DC converter from battery pack
- **Safety**: Hardware-level cutoff relays

### PCB Design Features

- **High-Voltage Isolation**: Proper creepage and clearance distances
- **Thermal Management**: Heat sinks for balancing MOSFETs
- **EMI Considerations**: Filtered power supply and shielded traces
- **Robust Connectors**: High-current battery terminals

## Safety Features

- **Multi-level Protection**:
  - Hardware overcurrent detection
  - Software-based predictive algorithms
  - Thermal runaway prevention
  - Short circuit protection

- **Fault Diagnostics**:
  - Cell voltage imbalance detection
  - Temperature anomaly alerts
  - Communication error handling
  - Self-test routines

## Performance Specifications

- **Voltage Range**: 12V - 60V (configurable)
- **Current Rating**: Up to 100A continuous
- **Balancing Current**: 200mA per cell
- **SoC Accuracy**: ±2%
- **Operating Temperature**: -20°C to +60°C

## Applications

- Electric vehicles (EV)
- E-bikes and e-scooters
- Renewable energy storage systems
- UPS and backup power systems
- Marine and RV applications

## Technologies Used

**Hardware**: Altium Designer, Battery Management ICs, High-Current MOSFETs, CAN Bus  
**Software**: Embedded C, Kalman Filtering, SoC Estimation Algorithms  
**Testing**: Battery Cycler, Thermal Chamber, Load Banks
