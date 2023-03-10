# Basestation / repeater for Meshtastic

**NOTE:** The project has just be started. I put it on Github early to enable sharing of ideas and collaboration

## Description
The goal of this project is to design a custom PCB to serve as a basestation and/or repeater for [Meshtastic](https://www.meshtastic.org/). Ideally, it would be put in a weatherproof enclosure outdoors.

### Design choices so far
- Espressif ESP32-WROOM-S3-1U
- Ebyte E22-900M30S (SX1262, 30dBm PA, SPI)
- 2 stage linear regulators to prevent noise
  - LM1084-5.0 (max. 27V in, max 5A out) as first stage
  - AMS117-3.3 as second stage
- Connector for optional GPS with selectable 5v/3.3V power

## ToDo
Fix variant.h
