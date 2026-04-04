# Project Book

> **{Project Name}** — {One-line description of what this project does}

This is the Project Book — a single, layered guide to understanding this project from the ground up. It reads like a book: start from the beginning and build context as you go, or jump to the chapter you need.

| Status | Value |
|--------|-------|
| **Last Updated** | {YYYY-MM-DD} |
| **Version** | {X.Y.Z} |
| **Maintainer** | {Name / Team} |
| **License** | {License} |

---

## Table of Contents

### [Chapter 0 — The Elevator Pitch](./00-elevator-pitch.md)
What is this? Who is it for? Start here.

### [Chapter 1 — The Why](./01-the-why.md)
The problem that existed before this project. Why it matters.

### [Chapter 2 — The Vision](./02-the-vision.md)
Design philosophy, principles, and what success looks like.

### [Chapter 3 — The Map](./03-the-map.md)
System architecture. How the pieces connect. The tour.

### [Chapter 4 — The Foundation](./04-the-foundation.md)
Tech stack, dependencies, and getting from zero to running.

### [Chapter 5 — The Build](./05-the-build.md)
How the core systems work, explained layer by layer.

### [Chapter 6 — The Integrations](./06-the-integrations.md)
How this system talks to the outside world.

### [Chapter 7 — The Gotchas](./07-the-gotchas.md)
Tribal knowledge. Edge cases. Things that will waste your time if you don't know.

### [Chapter 8 — The Operations](./08-the-operations.md)
Deploy, monitor, maintain, and fix.

### [Chapter 9 — The Roadmap](./09-the-roadmap.md)
Where this is going and what was deliberately left out.

### [Appendix — Reference](./10-appendix.md)
API specs, config schemas, environment variables, glossary.

---

## How to Use This Book

**First time here?** Read chapters 0 through 3. That gets you from "what is this" to "how it all fits together" in about 15 minutes.

**Setting up locally?** Chapter 4 has everything you need.

**Building a feature?** Chapters 5 and 6 explain how the internals work and how integrations are wired.

**Something broke?** Chapter 7 (gotchas) and Chapter 8 (operations) are your friends.

**Contributing?** Read the whole thing. It's worth it. Future you will thank present you.

---

## Keeping This Book Alive

This isn't a one-time artifact. Update it when:

- You ship a major feature or change architecture (Chapters 3, 5)
- You add or change an integration (Chapter 6)
- You spend 30+ minutes debugging something (Chapter 7)
- You change deploy process or infrastructure (Chapter 8)
- You make a deliberate scope decision (Chapter 9)

If a chapter doesn't apply to your project, delete it. A shorter book that's accurate beats a complete one that's stale.

| If your project... | Cut these chapters |
|--------------------|--------------------|
| Has no external APIs or services | Chapter 6 (Integrations) |
| Isn't deployed as a service | Chapter 8 (Operations) |
| Has no formal API surface | Appendix API section |
| Is a small internal tool | Chapters 6, 8, 9 |

---

<sub>This project uses the [Project Book](https://github.com/20alexl/project-book-template) format.</sub>
