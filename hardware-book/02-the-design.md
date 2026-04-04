# Chapter 2 — The Design

[← Back to Table of Contents](./README.md) · [Previous: The Why](./01-the-why.md) · [Next: The Architecture →](./03-the-architecture.md)

---

> Design philosophy and constraints before showing schematics or code.
> Hardware decisions are expensive to change — document why you made them.

## Design Principles

### 1. {Principle}

{e.g. "Repairability over compactness" — what it means and what it costs you.}

### 2. {Principle}

*What it means. What it prevents.*

### 3. {Principle}

*What it means. What it prevents.*

## Constraints

*The non-negotiable limits that shaped every decision.*

| Constraint | Value | Why |
|-----------|-------|-----|
| {e.g. Budget} | {e.g. < $200 per unit} | {Target audience} |
| {e.g. Size} | {e.g. Fits in a 19" rack} | {Deployment environment} |
| {e.g. Power} | {e.g. USB-powered, no wall adapter} | {Portability} |
| {e.g. Temperature} | {e.g. -20C to 60C operating} | {Outdoor use} |

## Key Tradeoffs

| We Chose | Over | Because |
|----------|------|---------|
| {e.g. Through-hole components} | {e.g. SMD} | {Hand-solderable, repairable} |
| {e.g. ESP32} | {e.g. STM32} | {WiFi built-in, Arduino ecosystem} |
| {e.g. 3D printed enclosure} | {e.g. Injection molded} | {Low volume, easy iteration} |

## What This Project Is NOT

*Explicit non-goals. What should someone NOT expect from this?*

---

[Next: The Architecture →](./03-the-architecture.md)
