# Chapter 6 — The Results

[← Back to Table of Contents](./README.md) · [Previous: The Experiments](./05-the-experiments.md) · [Next: The Gotchas →](./07-the-gotchas.md)

---

> Present results honestly. Include variance, not just best runs.
> Separate observation from interpretation — what happened vs what it means.

## Main Results

*The headline numbers. What did the experiments show?*

| Method | {Metric 1} | {Metric 2} | {Metric 3} |
|--------|-----------|-----------|-----------|
| {Baseline 1} | {Value ± std} | {Value ± std} | {Value ± std} |
| {Baseline 2} | {Value ± std} | {Value ± std} | {Value ± std} |
| **{Your method}** | **{Value ± std}** | **{Value ± std}** | **{Value ± std}** |

## Interpretation

*What do these results mean? Do they support your hypotheses from Chapter 2?*

- **H1:** {Supported / Partially supported / Not supported}. {Brief explanation.}
- **H2:** {Supported / Partially supported / Not supported}. {Brief explanation.}

## Detailed Results

### {Experiment 1 Name}

*Detailed results, figures, learning curves, breakdowns.*

```
*If text-based results, include them here*
```

*Or reference figures:*
> See `results/{figure-name}.png`

### {Experiment 2 Name}

*Detailed results.*

## Ablation Results

*How much does each component contribute?*

| Configuration | {Metric} | Delta from Full |
|--------------|----------|-----------------|
| Full system | {Value} | — |
| {Without component A} | {Value} | {-X%} |
| {Without component B} | {Value} | {-X%} |

## What Surprised Us

*Results that were unexpected, interesting, or counterintuitive. These are often the most valuable findings.*

## What Didn't Work as Expected

*Results that fell short of expectations. Be honest — this builds trust and saves others time.*

---

[Next: The Gotchas →](./07-the-gotchas.md)
