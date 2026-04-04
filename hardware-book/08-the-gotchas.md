# Chapter 8 — The Gotchas

[← Back to Table of Contents](./README.md) · [Previous: Calibration](./07-calibration.md) · [Next: Safety →](./09-safety.md)

---

> Hardware gotchas are expensive. A software bug costs time. A hardware mistake costs components.
> Every entry here saves someone money and frustration.

## How to Read This Chapter

Each gotcha follows the same format:

- **The Symptom** — What you observe
- **The Cause** — Why it's happening
- **The Fix** — How to resolve it
- **The Cost** — What it costs if you don't catch it

---

### Gotcha: {Descriptive title}

**Symptom:** {What you observe — e.g. "Motor vibrates but doesn't turn"}

**Cause:** {Why — e.g. "Coil wires swapped between A and B phases"}

**Fix:** {How to fix — e.g. "Swap the two middle wires on the motor connector"}

**Cost:** {What happens if missed — e.g. "No damage, just won't work"}

---

### Gotcha: {Descriptive title}

**Symptom:** {What you observe}

**Cause:** {Why}

**Fix:** {Resolution}

**Cost:** {Consequence}

---

## Common Build Mistakes

| Mistake | What Happens | How to Avoid |
|---------|-------------|--------------|
| {e.g. Reversed motor driver power} | {e.g. Magic smoke, driver dead} | {e.g. Check polarity before connecting power} |
| {e.g. I2C pullups missing} | {e.g. Sensor reads all zeros} | {e.g. Add 4.7K pullups or use breakout with built-in} |
| {e.g. Screws too tight on rail} | {e.g. Binding, rough motion} | {e.g. Tighten until snug, then back off 1/8 turn} |

## Things That Look Broken But Aren't

| Behavior | Why It Looks Wrong | Why It's Normal |
|----------|-------------------|----------------|
| {e.g. Stepper motor warm to touch} | {Seems like overheating} | {Normal — steppers hold current at standstill} |
| {e.g. Sensor reads -1 on startup} | {Seems like hardware failure} | {Startup delay — first valid read after 100ms} |

## Component-Specific Notes

*Lessons learned about specific components that aren't in the datasheet.*

### {Component: e.g. TMC2209}

- {e.g. UART address must be set via MS1/MS2 pins before power-on}
- {e.g. Default current is often too low — set via UART or Vref pot}

### {Component}

- {Note}
- {Note}

---

> **Contributing:** If you destroyed a component or lost hours debugging, add it here.

---

[Next: Safety →](./09-safety.md)
