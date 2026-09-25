# MCU Data Logger — PCB Design

### 📊 Microcontroller-Based Data Logging System

**MCU Data Logger** is an electronics hardware project designed to collect, store, and manage data using a microcontroller-based system.

The design integrates **ESP32, external EEPROM, GPS, 4G LTE communication, and regulated power circuitry** into a single hardware platform.

This repository contains the **KiCad 9 schematic and PCB design files** for the project.

---

## 🔧 Hardware

| Component                   | Purpose                                |
| --------------------------- | -------------------------------------- |
| **ESP32 Development Board** | Main microcontroller                   |
| **24LC1025 EEPROM**         | External non-volatile data storage     |
| **NEO-6M GPS**              | Location / GPS data                    |
| **A7670C 4G LTE Module**    | Cellular communication                 |
| **HT7333**                  | 3.3V voltage regulation                |
| **Resistors & Capacitors**  | Supporting and filtering components    |
| **Connectors**              | External module and signal connections |

---

## 📐 Schematic Design

The complete circuit schematic was designed in **KiCad 9**, integrating the MCU, memory, communication modules, and power circuitry.

### Key Design Work

* Schematic capture
* Component selection
* Symbol management
* Footprint assignment
* Net labeling
* Power and ground connections
* UART communication
* I²C communication with EEPROM
* 3.3V regulated power supply
* ERC checking and troubleshooting

---

## 🖥️ PCB Design

The project follows a complete **KiCad PCB design workflow**:

```text
Schematic
    ↓
Symbol & Footprint Assignment
    ↓
ERC
    ↓
PCB Layout
    ↓
Component Placement
    ↓
Net Classes & Design Rules
    ↓
Routing
    ↓
DRC
    ↓
Gerber Generation
```

### PCB Design Work

* PCB layout
* Component placement
* Footprint management
* Custom footprint integration
* Track routing
* Net Classes
* Trace width and clearance configuration
* Power and signal routing
* Ground connections
* ERC troubleshooting
* DRC validation

---

## 🔌 Main Interfaces

```text
ESP32
 │
 ├── I²C ──────→ 24LC1025 EEPROM
 │
 ├── UART ─────→ NEO-6M GPS
 │
 └── UART ─────→ A7670C 4G LTE
```

### Communication

* **I²C** — EEPROM communication
* **UART** — GPS communication
* **UART** — 4G LTE communication
* **GPIO** — Control and status signals

---

## 🛠️ Tools & Technologies

### PCB Design

**KiCad 9**

* Schematic Capture
* PCB Layout
* Footprint Management
* Component Placement
* Routing
* Net Classes
* Design Rules
* ERC / DRC

### Electronics

* ESP32
* EEPROM
* GPS
* 4G LTE
* Voltage Regulation
* UART
* I²C
* Power & Signal Routing

### Version Control

* Git
* GitHub

---


## 🎯 Skills Demonstrated

`KiCad 9` `PCB Design` `Schematic Capture` `PCB Layout`
`Footprints` `Component Placement` `Routing` `Net Classes`
`ERC` `DRC` `UART` `I²C` `Power Supply Design` `Git` `GitHub`

---

### 👨‍💻 Author

**Siddharth Kote**

Electronics & Communication Engineering Graduate

Focused on **PCB Design, Electronics Hardware & KiCad Development**.
