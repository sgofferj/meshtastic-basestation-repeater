# Basestation / repeater for Meshtastic

**NOTE:** The project has just been started. I put it on Github early to enable sharing of ideas and collaboration

## Description
The goal of this project is to design a custom PCB to serve as a basestation and/or repeater for [Meshtastic](https://www.meshtastic.org/). Ideally, it would be put in a weatherproof enclosure outdoors.

Other than most Meshtastic repeater projects, this project does not focus on the lowest possible power usage to enable easy solar power supply but on ruggedness, coverage and range. The LM1084-5.0 primary input regulator e.g. has a voltage input range of 6.3 to 27V and a max. power out of 5A. That's pretty much overkill but allows the repeater to be safely powered by a wide range of power sources including easy to find 12V plug packs, cars, trucks, industrial and military equipment (which typically runs on 24V), etc. Double input protection (so far) should make it pretty robust against transients (technical failures, thunderstorms, etc.).

### Design choices so far
- Espressif ESP32-WROOM-S3-1U
- Ebyte E22-900M30S (SX1262, 30dBm PA, SPI)
- 2 stage linear regulators to prevent noise
  - LM1084-5.0 (max. 27V in, max 5A out) as first stage
  - AMS117-3.3 as second stage
- Double input protection
  - SR540 as reverse polarity protection
  - 1N5361 as TSD
- Connector for optional GPS with selectable 5v/3.3V power

## ToDo
Fix variant.h
