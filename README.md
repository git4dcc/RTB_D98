# RTB_D98
[![OpenDcc Forum Project](https://img.shields.io/badge/OpenDcc_Forum_Project-FF6699)](https://forum.opendcc.de)
[![Kicad_Libs](https://img.shields.io/badge/Kicad_Libs-29C7FF)](https:///../../../../git4dcc/RTB_SamacSys)
[![Apache License 2.0](https://img.shields.io/badge/license-Apache%20License%202.0-lightgray)](https://www.apache.org/licenses/LICENSE-2.0)

## This is a [OpenDcc](https://forum.opendcc.de/viewtopic.php?t=11034) forum project
The hard and software is based on the [D16](https://rtb4dcc.de/hardware/decoder/d16/) motor decoder. It implements a double-sided NEM-651 **function decoder** for use with DCC infrastructure. The hardware provides
- 10 auxiliary output ports
- single WS28xx connector (controlling up to 32 external neo pixels).

``Note: this repo is currently under construction and will be completed soon. (Feb 20, 2026)``

<details>
<summary>See also</summary>

- [RTB_D16 - NEM651](/../../../../git4dcc/RTB_D16)

</details>

<details>
<summary>User Guides</summary>

- User Guide - DE
- User Guide - EN

</details>

<img src="supplemental/images/D98_main.jpg" width=500>
<br>

The decoder has the following features,
- **NEM-651** connector
- **DCC**
  - DCC-A automatic logon
  - DCC-R protocol extension
  - Service Mode Programming
- **Railcom**
  - Channel 1/2
  - POM, xPOM, Long_1
  - DYN: QoS, Track-voltage, AUX-current, Temp, East/West
- double sided
- Dimension: 13 x 9 mm
- 7-20V track voltage
- heartbeat LED
- adjustable max AUX current (default 500mA)
- over temp protection
- Function output: LV/LR/AUX1/AUX2 open drain
- Function output: AUX3/AUX4/AUX5/AUX6/AUX7/AUX8 logic level (3.3V)
- Function output: LV/LR/AUX1/AUX2/AUX3/AUX4 (dimmable, 1.4kHz)
- WS28xx output: controls up to 32 WS28xx neo pixels
- optional external buffer capacitor (max. 1500uF)
- <10mA idle power consumption
- Firmware update over main tracks via DCC-R protocol


# Hardware
The current PCB layout uses SMD footprints with 0.5mm pitch and mainly 0402 parts. Reflow soldering is recommended, handsoldering nearly impossible.

<img src="supplemental/images/D98_top.jpg" width=400>   <img src="supplemental/images/D98_btm.jpg" width=400>

## PCB
- 6-layer PCB, FR4, 13 x 9 x 0.8mm (double sided)
- CPU: AVR64DA32
- Connector: NEM-651 (or solder)

## Kicad
[Schematic](doc/D98_schematic.pdf) | [Layout](doc/D98_layout.pdf) | [Gerber](gerber)

<details>
<summary>Dependency</summary>
<br>

:yellow_circle: Requires my Kicad project library [RTB_SamacSys](https://github.com/git4dcc/RTB_SamacSys) in the same directory tree.

</details>

## Firmware
Filename structure: { **pcb** }{ **code** }{ **version** }.hex

Example: **D98F0001**.hex

|   | Description |
| --- | --- |
| **pcb** | Name of matching hardware (**D98**) |
| **code** | Type of code contained (**R**=rom, **B**=bootloader, **F**=flash, **U**=bld update, **P**=UPDI factory code) |
| **version** | Release version (**####**) |

[Firmware files](firmware)

# Images
| top | bottom |
| --- | --- |
| <img src="supplemental/images/D98_top_connect.jpg" width=330> | <img src="supplemental/images/D98_btm_connect.jpg" width=330> |




# YouTube
Some YouTubes to see the D98 decoder in action.<br><br>

This project is intended for hobby use only and is distributed in accordance with the Apache License 2.0 agreement.
