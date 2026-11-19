---
layout: page
title: Virtual Fence Livestock Collar
description: Precision-ranching collar that keeps cattle inside virtual boundaries, with LoRaWAN and cellular/satellite connectivity for remote rangelands
importance: 1
category: research
related_publications: false
---

## Project Overview

As part of NMSU's **Precision Ranching** team, I am developing the hardware for a **virtual fence livestock collar**. The collar tracks each animal's position and gives a cue when it approaches a boundary drawn on a map, so ranchers can manage grazing without building or moving physical fences.

The main engineering challenge is connectivity: Southwestern rangelands often have no cellular coverage, so the collar combines a long-range LoRaWAN link with a cellular/satellite fallback.

## Hardware & Connectivity

- **MCU and cellular/satellite:** Nordic **nRF9151** (LTE-M / NB-IoT with non-terrestrial-network satellite support)
- **LoRaWAN:** Semtech **SX1262**-based radio module driven over SPI, with a PCB antenna
- **Network back end:** LoRaWAN gateways with a **ChirpStack** network server
- **Power:** battery-powered design with on-board charge management, built for long field deployments

## Prototyping & Manufacturing

- In-house **SMT assembly** with custom reflow profiles (SAC305)
- **3D-printed enclosures**: flexible resin for prototypes, TPU as the production target for a rugged, animal-safe fit

## My Role

I lead the collar's electronics: schematic capture and PCB layout, radio and antenna integration, power design, bench testing, and the path toward a manufacturable, certifiable product.
