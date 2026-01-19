---
layout: page
title: Industrial Data Logger
description: Multi-channel data acquisition system for industrial monitoring
img: assets/img/6.jpg
importance: 4
category: work
related_publications: false
---

## Project Overview

Designed a ruggedized industrial data logger for real-time monitoring and recording of multiple sensor inputs in harsh industrial environments.

## System Specifications

- **Analog Inputs**: 8 channels, 16-bit ADC resolution
- **Digital Inputs**: 16 channels, optically isolated
- **Sampling Rate**: Up to 10kHz per channel
- **Storage**: SD card (up to 32GB) + internal flash
- **Communication**: RS-485, Ethernet, USB
- **Power**: 12-24V DC input with wide tolerance

## Hardware Architecture

### Signal Conditioning

- **Analog Front-End**: Programmable gain amplifiers (PGA)
- **Filtering**: Anti-aliasing filters for each channel
- **Isolation**: Galvanic isolation for industrial noise immunity
- **Protection**: Overvoltage clamps and current limiting

### Data Processing

- **MCU**: STM32F4 series (168MHz, floating-point unit)
- **Memory**: External SRAM for data buffering
- **RTC**: Real-time clock with battery backup
- **Watchdog**: Hardware and software watchdog timers

### PCB Design Considerations

- **6-layer stackup** for optimal signal integrity
- **Analog/Digital Separation**: Isolated ground planes
- **Shielding**: Guard traces around sensitive analog signals
- **Connector Selection**: Industrial-grade screw terminals and M12 connectors

## Features

- **Real-time Display**: Local LCD for immediate data visualization
- **Configurable Triggers**: Threshold-based event recording
- **Data Export**: CSV format for easy analysis
- **Remote Access**: Web interface for configuration and monitoring
- **Alarm System**: Relay outputs for threshold violations

## Industrial Applications

- Temperature and pressure monitoring in manufacturing
- Vibration analysis for predictive maintenance
- Environmental monitoring (air quality, humidity)
- Process control and quality assurance
- Energy consumption tracking

## Technologies Used

**Hardware**: Altium Designer, STM32F4, 16-bit ADC, RS-485, Ethernet PHY  
**Software**: Embedded C, FatFS, LwIP TCP/IP Stack  
**Testing**: Calibration equipment, Environmental chamber
