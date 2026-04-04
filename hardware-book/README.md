# Hardware Book

> **{Project Name}** — {One-line description}

This is the Hardware Book — a layered guide to understanding this hardware/embedded project from concept to assembly to operation. It reads like a build manual with context: start from the beginning for the full picture, or jump to what you need.

| Status | Value |
|--------|-------|
| **Last Updated** | {YYYY-MM-DD} |
| **Revision** | {Hardware revision, e.g. Rev C} |
| **Maintainer** | {Name / Team} |
| **License** | {License} |

---

## Table of Contents

### [Chapter 0 — The Elevator Pitch](./00-elevator-pitch.md)
What is this? What does it do in the physical world?

### [Chapter 1 — The Why](./01-the-why.md)
The problem this solves and what came before it.

### [Chapter 2 — The Design](./02-the-design.md)
Design philosophy, constraints, and key tradeoffs.

### [Chapter 3 — The Architecture](./03-the-architecture.md)
System overview: mechanical, electrical, and software layers.

### [Chapter 4 — Bill of Materials](./04-bom.md)
Every part, where to get it, and what it costs.

### [Chapter 5 — The Build](./05-the-build.md)
Assembly instructions, wiring, and physical setup.

### [Chapter 6 — The Firmware](./06-the-firmware.md)
Software that runs on the hardware: flashing, configuration, architecture.

### [Chapter 7 — Calibration and Testing](./07-calibration.md)
How to verify it works, tune it, and validate performance.

### [Chapter 8 — The Gotchas](./08-the-gotchas.md)
Things that will burn your time (or your components) if you don't know.

### [Chapter 9 — Safety](./09-safety.md)
Hazards, limits, emergency procedures, and compliance.

### [Chapter 10 — Operations and Maintenance](./10-operations.md)
Daily use, troubleshooting, wear parts, and repair.

### [Appendix — Reference](./11-appendix.md)
Pinouts, datasheets, schematics, glossary.

---

## How to Use This Book

**Evaluating this project?** Read Chapters 0-3. That covers what, why, and how it all fits together.

**Building one?** Chapters 4 and 5 are the BOM and assembly guide.

**Programming it?** Chapter 6 covers the firmware.

**Something's not working?** Chapters 7 (calibration), 8 (gotchas), and 10 (troubleshooting) are your friends.

**Safety concern?** Chapter 9, always.

---

## Keeping This Book Alive

Update it when:

- You change the hardware design or BOM (Chapters 3, 4, 5)
- You update firmware (Chapter 6)
- You discover a failure mode or gotcha (Chapters 8, 10)
- You find a safety issue (Chapter 9 — immediately)
- You change calibration procedures (Chapter 7)

If a chapter doesn't apply to your project, delete it. A shorter book that's accurate beats a complete one that's stale.

| If your project... | Cut these chapters |
|--------------------|--------------------|
| Has no programmable components | Chapter 6 (Firmware) |
| Is a one-off build, not a product | Chapter 10 (Operations) |
| Has no safety hazards | Chapter 9 (Safety) — but think twice |
| Is purely mechanical | Chapters 6, 7 (calibration), Appendix pinout section |

---

<sub>This project uses the [Project Book](https://github.com/20alexl/project-book-template) format.</sub>
