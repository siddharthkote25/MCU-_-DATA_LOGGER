# MCU Data Logger — PCB Design

### 📊 Microcontroller-Based Data Logging System

**MCU Data Logger** is an electronics hardware project designed to collect, store, and manage data using a microcontroller-based system.

The design integrates an **ESP32, external EEPROM, GPS, 4G LTE module, and regulated power circuitry**.

This repository contains the **KiCad 9 schematic and PCB design files** developed for the project.

---

## 🔧 Hardware

| Component                   | Purpose                                |
| --------------------------- | -------------------------------------- |
| **ESP32 Development Board** | Main microcontroller                   |
| **24LC1025 EEPROM**         | Non-volatile data storage              |
| **NEO-6M GPS**              | GPS data                               |
| **A7670C 4G LTE Module**    | Cellular communication                 |
| **HT7333**                  | 3.3V voltage regulation                |
| **Resistors & Capacitors**  | Supporting and filtering components    |
| **Connectors**              | External module and signal connections |

---

## 📐 Schematic Design

The circuit was designed in **KiCad 9** and organized into multiple schematic sheets to keep the design structured and easy to manage.

### Schematic — Sheet 1

![MCU Data Logger Schematic Sheet 1](./Mcu%20sheet%201.png)

### Schematic — Sheet 2

![MCU Data Logger Schematic Sheet 2](./Mcu%20sheet%202%20.png)

---

## 🔌 Main Interfaces

```text
                         ┌──────────────────┐
                         │      ESP32       │
                         │ Main Controller  │
                         └────────┬─────────┘
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
             I²C                 UART                UART
              │                   │                   │
       ┌──────▼──────┐     ┌──────▼──────┐     ┌─────▼──────┐
       │  24LC1025   │     │   NEO-6M    │     │  A7670C    │
       │   EEPROM    │     │     GPS     │     │   4G LTE   │
       └─────────────┘     └─────────────┘     └────────────┘
```

* **I²C** — EEPROM communication
* **UART** — GPS communication
* **UART** — 4G LTE communication
* **GPIO** — Control and status signals

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

## 🛠️ Tools & Technologies

### PCB Design

**KiCad 9**

`Schematic Capture` • `PCB Layout` • `Footprint Management`
`Component Placement` • `Routing` • `Net Classes`
`Design Rules` • `ERC` • `DRC`

### Electronics

`ESP32` • `EEPROM` • `GPS` • `4G LTE`
`UART` • `I²C` • `Voltage Regulation`
`Power & Signal Routing`

### Version Control

`Git` • `GitHub`

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


