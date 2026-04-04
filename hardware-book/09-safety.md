# Chapter 9 — Safety

[← Back to Table of Contents](./README.md) · [Previous: The Gotchas](./08-the-gotchas.md) · [Next: Operations →](./10-operations.md)

---

> Read this chapter before building, not after something goes wrong.
> Hardware can hurt people. Take this seriously.

## Hazard Summary

| Hazard | Severity | Where | Mitigation |
|--------|----------|-------|-----------|
| {e.g. Electrical shock} | {High} | {e.g. Mains power supply} | {e.g. Enclosed, grounded, fused} |
| {e.g. Pinch points} | {Medium} | {e.g. Moving gantry} | {e.g. Keep hands clear during operation} |
| {e.g. Hot surfaces} | {Low} | {e.g. Stepper motors, heat bed} | {e.g. Warning labels, cool-down period} |
| {e.g. Eye hazard} | {High} | {e.g. Laser module} | {e.g. Proper safety glasses, interlocked enclosure} |

## Electrical Safety

*Voltage levels, isolation requirements, fusing, grounding.*

- Maximum voltage in system: {V}
- All mains wiring must be {enclosed / done by qualified person / etc.}
- Fuse rating: {value and location}
- {Other electrical safety notes}

## Mechanical Safety

*Moving parts, pinch points, sharp edges, weight.*

- {e.g. Never reach into the work area while motors are energized}
- {e.g. Emergency stop button location and function}
- {e.g. Maximum load: X kg. Exceeding this risks structural failure.}

## Emergency Procedures

### Power Emergency

*How to safely kill power immediately.*

1. {e.g. Hit the emergency stop button (big red button on front panel)}
2. {e.g. If E-stop doesn't work, disconnect mains at the wall}
3. {e.g. Do not touch any wiring until power is confirmed off with multimeter}

### {Other Emergency Type}

1. {Step}
2. {Step}

## Operating Limits

| Parameter | Safe Range | Absolute Maximum | What Happens Beyond |
|-----------|-----------|-----------------|-------------------|
| {e.g. Ambient temperature} | {0-40C} | {60C} | {e.g. Electronics derate} |
| {e.g. Input voltage} | {11-13V} | {14V} | {e.g. Regulator failure} |
| {e.g. Continuous run time} | {8h} | {24h} | {e.g. Bearing wear, thermal buildup} |

## Compliance

*If applicable — standards, certifications, or regulations.*

- {e.g. Not CE certified — intended for personal/research use only}
- {e.g. Laser class: {X} — requires {safety measures}}
- {e.g. FCC: unintentional radiator, not tested}

---

[Next: Operations →](./10-operations.md)
