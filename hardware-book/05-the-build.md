# Chapter 5 — The Build

[← Back to Table of Contents](./README.md) · [Previous: Bill of Materials](./04-bom.md) · [Next: The Firmware →](./06-the-firmware.md)

---

> Step-by-step assembly. Write for someone who has built things before
> but has never seen this specific project.
> Photos or diagrams at key steps prevent expensive mistakes.

## Before You Start

- [ ] All parts from Chapter 4 acquired
- [ ] Tools from Chapter 4 ready
- [ ] Read Chapter 9 (Safety) if working with high voltage, motors, or batteries
- [ ] Clean, well-lit workspace with ESD protection if needed

## Assembly Order

*List the major phases. Order matters — some things must be assembled before others become inaccessible.*

1. {e.g. Frame assembly}
2. {e.g. Motion system}
3. {e.g. Electronics mounting}
4. {e.g. Wiring}
5. {e.g. Enclosure}

---

## Step 1: {Frame Assembly}

### Parts Needed

*List from BOM — reference by BOM number.*

- M1: Frame rails x4
- F1: M3x8 screws x16
- F2: T-nuts x16

### Instructions

1. {Step with detail}
2. {Step with detail}
3. {Step with detail}

> **Tip:** {Helpful advice that saves time or prevents mistakes.}

### Verify

*How to confirm this step is correct before moving on.*

- [ ] {e.g. Frame is square — measure diagonals, should be within 1mm}
- [ ] {e.g. All joints tight, no wobble}

---

## Step 2: {Motion System}

### Parts Needed

- {Parts from BOM}

### Instructions

1. {Step}
2. {Step}
3. {Step}

> **Warning:** {Something that will cause problems if done wrong.}

### Verify

- [ ] {Verification check}

---

## Step 3: {Electronics Mounting}

### Parts Needed

- {Parts from BOM}

### Instructions

1. {Step}
2. {Step}

### Verify

- [ ] {Check}

---

## Step 4: {Wiring}

### Wiring Diagram

```
*ASCII wiring diagram or reference to image*

{MCU Pin 12} ──── {Sensor SDA}
{MCU Pin 13} ──── {Sensor SCL}
{MCU Pin 25} ──── {Motor STEP}
{MCU Pin 26} ──── {Motor DIR}
{GND}        ──── {Common ground}
```

### Connections

| From | To | Wire | Notes |
|------|----|------|-------|
| {MCU GPIO 12} | {Sensor SDA} | {22AWG} | {Keep short, < 15cm} |
| {PSU 12V} | {Motor driver VIN} | {18AWG} | {Rated for motor current} |

> **Warning:** Double-check polarity before applying power. Reversed power will destroy {component}.

### Verify

- [ ] Continuity test on all connections
- [ ] No shorts between power and ground
- [ ] {Other verification}

---

## Step 5: {Enclosure}

### Parts Needed

- {Parts from BOM}

### Instructions

1. {Step}
2. {Step}

---

## Final Assembly Checklist

- [ ] All mechanical joints tight
- [ ] All wiring connected per diagram
- [ ] No loose wires or exposed conductors
- [ ] Power supply disconnected until Chapter 7 (calibration)
- [ ] {Any other final checks}

---

[Next: The Firmware →](./06-the-firmware.md)
