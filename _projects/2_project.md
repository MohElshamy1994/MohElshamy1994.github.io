---
layout: page
title: Solar MPPT Controller
description: Maximum Power Point Tracking controller for solar panel systems
img: assets/img/3.jpg
importance: 2
category: work
related_publications: false
---

## Project Overview

Designed a high-efficiency Maximum Power Point Tracking (MPPT) controller for solar panel installations, optimizing energy harvest across varying environmental conditions.

## Key Features

- **MPPT Algorithm**: Perturb & Observe (P&O) with adaptive step size
- **High Efficiency**: >97% conversion efficiency
- **Wide Input Range**: 12V-48V solar panel input
- **Battery Management**: Intelligent charging for lead-acid and lithium batteries
- **Protection Systems**: Overvoltage, overcurrent, reverse polarity, and thermal protection

## Technical Implementation

### Hardware Architecture
- **Power Stage**: Synchronous buck converter with high-frequency switching (100kHz)
- **Control**: STM32 microcontroller for MPPT algorithm execution
- **Sensing**: High-precision voltage and current sensing circuits
- **Display**: LCD interface for real-time monitoring
- **Communication**: UART interface for data logging

### PCB Design Highlights
- **4-layer PCB** with dedicated power and ground planes
- **Thermal Management**: Copper pours and thermal vias for heat dissipation
- **High-Current Traces**: Proper trace width calculations for 20A+ currents
- **Low-Noise Analog Section**: Separated from switching noise sources

### Control Algorithm
- Implemented adaptive MPPT algorithm in embedded C
- Real-time voltage and current sampling at 10kHz
- Dynamic duty cycle adjustment for optimal power extraction
- Battery state-of-charge (SoC) estimation

## Performance Metrics

- **Tracking Efficiency**: 99.5% under stable conditions
- **Conversion Efficiency**: 97.2% at rated load
- **Response Time**: <100ms to changing irradiance
- **Temperature Range**: -20°C to +70°C operation

## Technologies Used

**Hardware**: Altium Designer, STM32, Synchronous Buck Converter, Current Sensing  
**Software**: Embedded C, MPPT Algorithms  
**Testing**: Power Analyzer, Thermal Camera, Environmental Chamber
