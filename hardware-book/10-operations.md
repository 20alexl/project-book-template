# Chapter 10 — Operations and Maintenance

[← Back to Table of Contents](./README.md) · [Previous: Safety](./09-safety.md) · [Next: Appendix →](./11-appendix.md)

---

> Daily use, troubleshooting, and keeping it running long-term.
>
> **Skip this chapter** if this is a one-off build with no ongoing maintenance needs.

## Normal Operation

### Startup Sequence

1. {e.g. Power on the supply}
2. {e.g. Wait for boot (LED goes solid green)}
3. {e.g. Home all axes}
4. {e.g. System ready — send commands via serial/WiFi}

### Shutdown Sequence

1. {e.g. Return to home position}
2. {e.g. Send shutdown command}
3. {e.g. Wait for motors to de-energize}
4. {e.g. Power off supply}

## Troubleshooting

| Symptom | Check First | Then Check | Fix |
|---------|-------------|-----------|-----|
| {e.g. No response on power-on} | {Power supply voltage} | {USB connection, serial monitor} | {Check fuse, verify PSU} |
| {e.g. Motor makes noise but won't move} | {Motor current setting} | {Wiring, driver enable pin} | {Increase current, check connections} |
| {e.g. Sensor reads constant value} | {Wiring continuity} | {I2C address, pullups} | {Fix wiring, check address} |
| {e.g. Erratic behavior} | {Power supply capacity} | {Ground loops, EMI} | {Add capacitors, separate power/signal grounds} |

## Maintenance Schedule

| Interval | Task | How |
|----------|------|-----|
| {e.g. Every use} | {e.g. Visual inspection} | {Check for loose fasteners, debris} |
| {e.g. Monthly} | {e.g. Lubricate linear rails} | {Light machine oil on rail carriage} |
| {e.g. Monthly} | {e.g. Check belt tension} | {Should deflect ~2mm with light finger pressure} |
| {e.g. Yearly} | {e.g. Replace wear parts} | {See wear parts table below} |

## Wear Parts

*Components that degrade with use and will eventually need replacement.*

| Part | Expected Life | Failure Symptom | Replacement |
|------|-------------|----------------|-------------|
| {e.g. GT2 belt} | {~2000 hours} | {Backlash, skipping} | {BOM item M4} |
| {e.g. Nozzle} | {~500 hours} | {Poor extrusion} | {Standard 0.4mm brass} |

## Firmware Updates

```bash
# {How to update firmware in the field}
```

## Storage

*How to store the device when not in use for extended periods.*

- {e.g. Power off and disconnect}
- {e.g. Cover to prevent dust accumulation}
- {e.g. If motors have grease, run briefly every 3 months}

---

[Next: Appendix →](./11-appendix.md)
