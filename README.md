# ATmega328P Data Logger

A compact, battery-backed data logger board built around the ATmega328P-AU. It has a real-time clock for timestamping and 2 Mbit of external I²C EEPROM for storage, and it breaks out I²C, UART, GPIO and ICSP headers for sensors and programming. Designed end-to-end in **KiCad 10**.

![3D view](3D%20view.png)

## Features

- **MCU:** ATmega328P-AU (TQFP-32) with a 16 MHz crystal and 22 pF load capacitors
- **Real-time clock:** DS1337 with a 32.768 kHz crystal, battery backup, and pull-ups on its SQW/INTA outputs
- **Storage:** 2 × 24LC1025 (1 Mbit each, 2 Mbit / 256 KB total) I²C EEPROMs, write-protect tied to GND
- **I²C bus:** 4.7 kΩ pull-ups on SDA/SCK, shared by the RTC and both EEPROMs
- **Indicators:** power LED and a status LED on SCK (D13)
- **Programming:** standard 2×3 ICSP header, with a 10 kΩ pull-up on RESET
- **Power:** battery input with decoupling on every IC, plus AREF filter capacitor
- **Mechanical:** four mounting holes, one in each corner

## Connectors

| Ref | Interface | Pins |
|-----|-----------|------|
| J1 | I²C | GND, VCC, SDA, SCK |
| J2 | GPIO | D2–D8, GND, VCC |
| J3 | Serial / UART | GND, VCC, RX, TX |
| J4 | ICSP | MISO, VCC, SCK, MOSI, RESET, GND |
| Battery | Power input | VCC, GND |

## Schematic

Hierarchical design, split into functional blocks:

- **MCU:** ATmega328P, crystal, reset circuit, LEDs, AREF filter
- **Real time clock:** DS1337, 32.768 kHz crystal, pull-ups, decoupling
- **EEPROM:** two 24LC1025 with address pins, write-protect and I²C pull-ups
- **Connectors:** I²C, UART, GPIO and ICSP (separate sub-sheet)
- **Mounting:** four mounting holes

**Sheet 1: MCU, RTC, EEPROM**

![Schematic sheet 1](Mcu%20sheet%201.png)

**Sheet 2: Connectors**

![Schematic sheet 2](Mcu%20sheet%202%20.png)

## PCB

- Layers: 2-layer
- Board size: [XX mm × XX mm]
- Components: mostly SMD (0603/0805 passives, TQFP-32, SOIC-8), through-hole headers
- Copper fills, silkscreen labelling for all connectors, DRC clean

![PCB layout](Layout%20Design.png)

## Repository Structure

```
.
├── ATMEGA328P-AU/               # MCU symbol / footprint / 3D model files
├── Footprints/                  # Custom footprint library
├── Gerbers/                     # Manufacturing outputs (Gerber + drill files)
├── symbols-downloaded/          # Downloaded symbol libraries
├── Mcu - data logger.kicad_pro  # KiCad project file
├── Mcu - data logger.kicad_sch  # Top-level schematic
├── Connectors.kicad_sch         # Connectors sub-sheet
├── Mcu - data logger.kicad_pcb  # PCB layout
├── sym-lib-table                # Project symbol library table
├── report.txt                   # Gerber/drill generation report
├── 3D view.png
├── Layout Design.png
├── Mcu sheet 1.png
├── Mcu sheet 2 .png
└── README.md
```

## Tools

- KiCad 10.0.6
- Git / GitHub for version control

## Author

**Siddharth Kote**
siddharthkote129@gmail.com
## Author

[Your Name] — [LinkedIn / email]

