# Appendix — Reference

[← Back to Table of Contents](./README.md) · [Previous: Operations](./10-operations.md)

---

## Pinout

*Complete pin mapping for the main MCU.*

| Pin | Function | Direction | Notes |
|-----|----------|-----------|-------|
| {GPIO 12} | {I2C SDA} | {Bidirectional} | {4.7K pullup to 3.3V} |
| {GPIO 13} | {I2C SCL} | {Output} | {4.7K pullup to 3.3V} |
| {GPIO 25} | {Stepper STEP} | {Output} | {3.3V logic} |
| {GPIO 26} | {Stepper DIR} | {Output} | {3.3V logic} |

## Schematics

*Reference to schematic files in the repo.*

- Full schematic: `hardware/schematic.pdf`
- PCB layout: `hardware/pcb/`
- KiCad project: `hardware/kicad/`

## Datasheets

*Links or local copies of key component datasheets.*

| Component | Datasheet |
|-----------|-----------|
| {MCU} | {Link or `datasheets/{filename}.pdf`} |
| {Sensor} | {Link or local path} |
| {Motor driver} | {Link or local path} |

## 3D Models

*CAD files for the mechanical design.*

| Part | Format | File |
|------|--------|------|
| {Full assembly} | {STEP} | `cad/{name}.step` |
| {Enclosure} | {STL} | `stl/{name}.stl` |
| {Bracket} | {STL} | `stl/{name}.stl` |

## Communication Protocol Reference

*Complete command/message reference if the device has a serial/network interface.*

### Commands

| Command | Parameters | Response | Description |
|---------|-----------|----------|-------------|
| {`HOME`} | {none} | {`OK`} | {Home all axes} |
| {`MOVE`} | {`X Y [speed]`} | {`OK` or `ERR:{code}`} | {Move to position} |
| {`STATUS`} | {none} | {JSON status} | {Report current state} |

### Error Codes

| Code | Meaning | Recovery |
|------|---------|----------|
| {E01} | {Description} | {How to fix} |
| {E02} | {Description} | {How to fix} |

## Glossary

| Term | Definition |
|------|-----------|
| {Term} | {What it means in this project} |

## Revision History

| Rev | Date | Changes |
|-----|------|---------|
| {A} | {YYYY-MM-DD} | {Initial release} |
| {B} | {YYYY-MM-DD} | {What changed} |

## Links

- {Project repository}
- {Forum / community}
- {Related projects}

---

[← Back to Table of Contents](./README.md)
