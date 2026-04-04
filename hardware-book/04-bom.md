# Chapter 4 — Bill of Materials

[← Back to Table of Contents](./README.md) · [Previous: The Architecture](./03-the-architecture.md) · [Next: The Build →](./05-the-build.md)

---

> Every part needed to build one unit. Include sources and approximate costs.
> Someone should be able to order everything from this page.
>
> **First time building from a BOM?** Start with the summary table to understand scope and cost.
> The detailed tables below have exact part numbers and sources — order from those.
> Don't substitute parts unless the Substitutions section says it's safe.

## BOM Summary

| Category | Items | Approx Cost |
|----------|-------|-------------|
| Electronics | {N} | ${X} |
| Mechanical | {N} | ${X} |
| Fasteners | {N} | ${X} |
| 3D Printed | {N} | ${X} (filament) |
| **Total** | | **${X}** |

## Electronics

| # | Part | Specification | Qty | Source | Unit Cost | Notes |
|---|------|--------------|-----|--------|-----------|-------|
| E1 | {e.g. MCU} | {e.g. ESP32-S3-WROOM-1} | 1 | {e.g. Mouser, LCSC} | ${X} | |
| E2 | {e.g. Sensor} | {e.g. BME280 breakout} | 1 | {e.g. Adafruit} | ${X} | |
| E3 | {e.g. Motor driver} | {e.g. TMC2209 silent} | 1 | {e.g. Amazon} | ${X} | |
| E4 | {e.g. Power supply} | {e.g. 12V 5A barrel jack} | 1 | {e.g. Amazon} | ${X} | |

## Mechanical

| # | Part | Specification | Qty | Source | Unit Cost | Notes |
|---|------|--------------|-----|--------|-----------|-------|
| M1 | {e.g. Frame rail} | {e.g. 2020 extrusion 300mm} | 4 | {Source} | ${X} | |
| M2 | {e.g. Linear rail} | {e.g. MGN12H 200mm} | 2 | {Source} | ${X} | |
| M3 | {e.g. Bearing} | {e.g. 608ZZ} | 4 | {Source} | ${X} | |

## Fasteners

| # | Part | Specification | Qty | Notes |
|---|------|--------------|-----|-------|
| F1 | {e.g. M3x8 socket head} | {Stainless} | 20 | {Frame assembly} |
| F2 | {e.g. M3 T-nut} | {2020 profile} | 20 | {Frame joints} |
| F3 | {e.g. M5x16 button head} | {Stainless} | 8 | {Motor mounts} |

## 3D Printed Parts

| # | Part | Material | Infill | Time | File |
|---|------|----------|--------|------|------|
| P1 | {e.g. Motor mount} | {e.g. PETG} | {e.g. 40%} | {e.g. 2h} | `stl/{filename}.stl` |
| P2 | {e.g. Sensor bracket} | {e.g. PLA} | {e.g. 20%} | {e.g. 30m} | `stl/{filename}.stl` |
| P3 | {e.g. Enclosure top} | {e.g. PETG} | {e.g. 30%} | {e.g. 4h} | `stl/{filename}.stl` |

## PCBs

*If applicable — custom PCB details.*

| Board | Size | Layers | Fabrication | Files |
|-------|------|--------|-------------|-------|
| {e.g. Main board} | {e.g. 80x60mm} | {e.g. 2} | {e.g. JLCPCB} | `pcb/{name}/` |

## Tools Required

*What tools does someone need to build this?*

- {e.g. Soldering iron (temperature controlled)}
- {e.g. 3D printer (FDM, 200mm bed minimum)}
- {e.g. Hex key set (M2.5, M3, M4)}
- {e.g. Multimeter}
- {e.g. Wire strippers}

## Substitutions

*Common parts that can be swapped and what to watch out for.*

| Original | Acceptable Substitute | Watch Out For |
|----------|----------------------|--------------|
| {Part} | {Alternative} | {What might differ} |

---

[Next: The Build →](./05-the-build.md)
