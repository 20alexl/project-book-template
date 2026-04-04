# Chapter 7 — Calibration and Testing

[← Back to Table of Contents](./README.md) · [Previous: The Firmware](./06-the-firmware.md) · [Next: The Gotchas →](./08-the-gotchas.md)

---

> First power-on, verification, and tuning. This is where you find out if the build is correct.
> Go slow. Check at every step. It's cheaper to catch problems here.

## First Power-On Checklist

- [ ] Visual inspection complete (no shorts, loose wires, wrong polarity)
- [ ] Multimeter check: power rails correct voltage, no shorts to ground
- [ ] Connect power supply (start with current-limited if possible)
- [ ] Monitor current draw — should be {expected range}
- [ ] Check for: smoke, hot components, unexpected sounds
- [ ] Serial monitor connected — check boot output

## Sensor Verification

*Test each sensor individually.*

### {Sensor 1: e.g. Temperature}

**Test:** {What to do}

**Expected:** {What you should see}

**If wrong:** {Common causes and fixes}

### {Sensor 2}

**Test:** {What to do}

**Expected:** {What you should see}

**If wrong:** {Common causes}

## Actuator Verification

*Test each actuator individually, at low power/speed first.*

### {Actuator 1: e.g. Stepper Motor}

**Test:** {e.g. Send single-step commands, verify direction and step size}

**Expected:** {e.g. Smooth motion, correct direction, no skipped steps}

**If wrong:**
- {e.g. Wrong direction → swap A/B coil wires}
- {e.g. Skipping steps → increase current limit, check wiring}
- {e.g. No movement → check enable pin, verify driver power}

## Calibration Procedures

### {Calibration 1: e.g. Home Position}

**Purpose:** {What this calibration achieves}

**Procedure:**
1. {Step}
2. {Step}
3. {Step}

**Acceptance criteria:** {How to know it's calibrated correctly}

### {Calibration 2: e.g. Sensor Offset}

**Purpose:** {What this calibration achieves}

**Procedure:**
1. {Step}
2. {Step}

**Acceptance criteria:** {How to verify}

## Performance Validation

*Run the system through its intended use case and verify it meets specs.*

| Test | Method | Expected | Acceptable Range |
|------|--------|----------|-----------------|
| {e.g. Positioning accuracy} | {e.g. Dial indicator at 10 points} | {e.g. ±0.1mm} | {e.g. ±0.2mm} |
| {e.g. Speed} | {e.g. Time 100mm travel} | {e.g. < 2s} | {e.g. < 3s} |
| {e.g. Repeatability} | {e.g. Home 10x, measure spread} | {e.g. ±0.05mm} | {e.g. ±0.1mm} |

## Burn-In Test

*If applicable — extended run to catch infant mortality or thermal issues.*

**Duration:** {e.g. 4 hours continuous operation}

**Monitor:** {e.g. Temperature, current draw, error count}

**Pass criteria:** {e.g. No errors, temperature stable below 60C}

---

[Next: The Gotchas →](./08-the-gotchas.md)
