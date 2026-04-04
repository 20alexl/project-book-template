# Chapter 5 — The Experiments

[← Back to Table of Contents](./README.md) · [Previous: Reproducibility](./04-reproducibility.md) · [Next: The Results →](./06-the-results.md)

---

> Document what was run, not just what worked. Failed experiments are valuable context.
> For each experiment, explain the question it answers, not just the setup.

## Experiment Overview

*List all experiments and what question each one answers.*

| # | Name | Question | Status |
|---|------|----------|--------|
| 1 | {Name} | {What does this test?} | {Complete / In Progress / Planned} |
| 2 | {Name} | {What does this test?} | {Status} |
| 3 | {Name} | {What does this test?} | {Status} |

---

## Experiment 1: {Name}

### Question

*What specific hypothesis or claim does this experiment test?*

### Setup

*Describe the experimental setup: datasets, model configurations, baselines.*

| Parameter | Value |
|-----------|-------|
| {e.g. Learning rate} | {e.g. 1e-3} |
| {e.g. Batch size} | {e.g. 64} |
| {e.g. Epochs} | {e.g. 100} |
| {e.g. Model size} | {e.g. 1.5M params} |

### Baselines

*What are you comparing against? Why these baselines?*

### How to Run

```bash
# {Exact command to reproduce this experiment}
```

### Key Observations

*What happened? Brief — detailed results go in Chapter 6.*

---

## Experiment 2: {Name}

### Question

*What does this test?*

### Setup

*Configuration details.*

### Baselines

*Comparisons.*

### How to Run

```bash
# {Command}
```

### Key Observations

*What happened?*

---

## Ablations

*If you ran ablation studies, document them here. What was removed/changed, and what effect did it have?*

| Ablation | What Changed | Effect |
|----------|-------------|--------|
| {e.g. No fusion bridges} | {Disabled neural-symbolic bridges} | {-3% accuracy, schemas compile slower} |
| {e.g. No replay buffer} | {Removed experience replay} | {Catastrophic forgetting after 300 episodes} |

---

## Experiments That Didn't Work

*These are just as important. What did you try that failed, and what did you learn from it?*

### {Failed experiment name}

**What was tried:** {Description}

**What happened:** {Result}

**What it taught us:** {Lesson}

---

[Next: The Results →](./06-the-results.md)
