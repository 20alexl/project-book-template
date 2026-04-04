# Research Book

> **{Project Name}** — {One-line description of the research}

This is the Research Book — a layered guide to understanding this research project, from motivation to results to reproducibility. It reads like a paper companion: start from the beginning for full context, or jump to what you need.

| Status | Value |
|--------|-------|
| **Last Updated** | {YYYY-MM-DD} |
| **Paper** | {Link to paper, if published} |
| **Authors** | {Names} |
| **License** | {License} |

---

## Table of Contents

### [Chapter 0 — The Elevator Pitch](./00-elevator-pitch.md)
What is this research about? One page.

### [Chapter 1 — The Problem](./01-the-problem.md)
The gap in existing work and why it matters.

### [Chapter 2 — The Approach](./02-the-approach.md)
Methodology, hypotheses, and key design choices.

### [Chapter 3 — The Architecture](./03-the-architecture.md)
System design and how the code maps to the approach.

### [Chapter 4 — Reproducibility](./04-reproducibility.md)
Environment, dependencies, data, and how to run everything.

### [Chapter 5 — The Experiments](./05-the-experiments.md)
What was run, how, and with what parameters.

### [Chapter 6 — The Results](./06-the-results.md)
Findings, tables, figures, and interpretation.

### [Chapter 7 — The Gotchas](./07-the-gotchas.md)
What went wrong, what was surprising, what to watch out for.

### [Chapter 8 — Related Work](./08-related-work.md)
How this fits in the field and what it builds on.

### [Chapter 9 — Future Work](./09-future-work.md)
What's next, what was left out, open questions.

### [Appendix — Reference](./10-appendix.md)
Hyperparameters, data schemas, hardware specs, glossary.

---

## How to Use This Book

**Reviewing the research?** Read Chapters 0-2 for context, then 5-6 for results.

**Reproducing the experiments?** Chapter 4 gets you set up, Chapter 5 tells you what to run.

**Extending this work?** Read everything, especially Chapters 7 and 9.

---

## Keeping This Book Alive

Update it when:

- You run new experiments or get new results (Chapters 5, 6)
- You find something surprising or broken (Chapter 7)
- You discover relevant related work (Chapter 8)
- You change the approach or architecture (Chapters 2, 3)

If a chapter doesn't apply to your project, delete it. A shorter book that's accurate beats a complete one that's stale.

| If your project... | Cut these chapters |
|--------------------|--------------------|
| Has no codebase (purely analytical) | Chapter 3 (Architecture) |
| Is a paper companion, not standalone | Chapter 8 (Related Work) — it's in the paper |
| Has no published paper yet | Remove Paper field from metadata |
| Is a single experiment | Chapters 5, 6 can merge into one |

---

<sub>This project uses the [Project Book](https://github.com/20alexl/project-book-template) format.</sub>
