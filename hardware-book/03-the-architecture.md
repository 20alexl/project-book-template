# Chapter 3 — The Architecture

[← Back to Table of Contents](./README.md) · [Previous: The Design](./02-the-design.md) · [Next: Bill of Materials →](./04-bom.md)

---

> The full system overview. Mechanical, electrical, and software as one picture.
> Someone should understand how all the layers connect after reading this chapter.

## System Overview

*High-level block diagram showing all layers.*

```
┌─────────────────────────────────────────┐
│             SOFTWARE LAYER              │
│  {Firmware / OS / Application}          │
├─────────────────────────────────────────┤
│            ELECTRICAL LAYER             │
│  {MCU} ── {Sensors} ── {Actuators}     │
│     │                                   │
│  {Power Supply} ── {Comms}              │
├─────────────────────────────────────────┤
│           MECHANICAL LAYER              │
│  {Frame / Enclosure / Mounts}           │
└─────────────────────────────────────────┘
```

## Mechanical

### Structure

*Frame, enclosure, mounting. What holds everything together?*

**Materials:** {e.g. 3D printed PLA, 2020 aluminum extrusion, laser-cut acrylic}

**Key dimensions:** {Overall size, mounting holes, clearances}

### Moving Parts

*If applicable: actuators, linkages, joints, bearings.*

| Part | Type | Travel / Range | Notes |
|------|------|---------------|-------|
| {e.g. Z-axis} | {e.g. Lead screw + stepper} | {e.g. 200mm} | {e.g. 8mm lead, 2mm pitch} |

## Electrical

### Block Diagram

```
{Power} ──▶ {Regulator} ──▶ {MCU}
                              │
                    ┌─────────┼─────────┐
                    ▼         ▼         ▼
               {Sensor 1} {Sensor 2} {Actuator}
```

### Key Components

| Component | Part | Role | Interface |
|-----------|------|------|-----------|
| {MCU} | {e.g. ESP32-S3} | {Brain} | {—} |
| {Sensor} | {e.g. BME280} | {Temperature/humidity} | {I2C, 0x76} |
| {Actuator} | {e.g. NEMA17} | {Z-axis motion} | {Step/Dir via TMC2209} |
| {Power} | {e.g. LM7805} | {5V regulation} | {—} |

### Power Budget

| Component | Voltage | Current (typical) | Current (peak) |
|-----------|---------|-------------------|----------------|
| {MCU} | {3.3V} | {80mA} | {240mA} |
| {Sensor} | {3.3V} | {1mA} | {3mA} |
| {Actuator} | {12V} | {500mA} | {1.5A} |
| **Total** | | **{total}** | **{total}** |

## Software

*High-level software architecture. Detailed in Chapter 6.*

```
├── Main loop / RTOS tasks
├── Hardware abstraction (drivers)
├── Application logic
└── Communication (WiFi / Serial / BLE)
```

## How They Connect

*Trace a complete operation through all three layers. "When the user presses the button, here's what happens mechanically, electrically, and in software."*

---

[Next: Bill of Materials →](./04-bom.md)
