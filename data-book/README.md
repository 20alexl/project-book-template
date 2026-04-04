# Data Book

> **{Project Name}** — {One-line description}

This is the Data Book — a layered guide to understanding this data pipeline, ML system, or data engineering project. Start from the beginning for full context, or jump to what you need.

| Status | Value |
|--------|-------|
| **Last Updated** | {YYYY-MM-DD} |
| **Version** | {X.Y.Z} |
| **Maintainer** | {Name / Team} |
| **License** | {License} |

---

## Table of Contents

### [Chapter 0 — The Elevator Pitch](./00-elevator-pitch.md)
What does this pipeline do? What data goes in, what comes out?

### [Chapter 1 — The Why](./01-the-why.md)
The data problem this solves and what came before it.

### [Chapter 2 — The Design](./02-the-design.md)
Philosophy, data contracts, and key tradeoffs.

### [Chapter 3 — The Data](./03-the-data.md)
Sources, schemas, quality rules, and lineage.

### [Chapter 4 — The Pipeline](./04-the-pipeline.md)
How data flows from source to destination, step by step.

### [Chapter 5 — The Models](./05-the-models.md)
ML models, training, evaluation, and serving.

### [Chapter 6 — The Infrastructure](./06-the-infrastructure.md)
Where it runs, how it's orchestrated, and how to deploy.

### [Chapter 7 — The Gotchas](./07-the-gotchas.md)
Data quality traps, silent failures, and things that will ruin your week.

### [Chapter 8 — Monitoring and Alerting](./08-monitoring.md)
How to know it's healthy, how to know it's broken.

### [Chapter 9 — The Roadmap](./09-the-roadmap.md)
Where this is going, what was deliberately left out.

### [Appendix — Reference](./10-appendix.md)
Schema catalog, configuration, glossary.

---

## How to Use This Book

**Evaluating this system?** Read Chapters 0-2 for the what, why, and how.

**Onboarding?** Chapters 3-4 explain the data and how it flows.

**Training or updating a model?** Chapter 5.

**Something broke?** Chapters 7 (gotchas) and 8 (monitoring).

**Deploying or scaling?** Chapter 6.

---

## Keeping This Book Alive

Update it when:

- You add or change a data source (Chapter 3)
- You modify the pipeline (Chapter 4)
- You retrain or swap a model (Chapter 5)
- You discover a data quality issue (Chapter 7)
- You change infrastructure or orchestration (Chapter 6)

If a chapter doesn't apply to your project, delete it. A shorter book that's accurate beats a complete one that's stale.

| If your project... | Cut these chapters |
|--------------------|--------------------|
| Has no ML models | Chapter 5 (Models) |
| Runs locally or as a script | Chapter 6 (Infrastructure) |
| Has no production SLAs | Chapter 8 (Monitoring) |
| Is a one-time analysis, not a pipeline | Chapters 4, 6, 8 — keep 3 (Data) and 7 (Gotchas) |

---

<sub>This project uses the [Project Book](https://github.com/20alexl/project-book-template) format.</sub>
