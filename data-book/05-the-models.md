# Chapter 5 — The Models

[← Back to Table of Contents](./README.md) · [Previous: The Pipeline](./04-the-pipeline.md) · [Next: The Infrastructure →](./06-the-infrastructure.md)

---

> ML models in the system: what they predict, how they're trained, and how they're served.
>
> **Skip this chapter** if the system doesn't include ML models.

## Model Inventory

| Model | Purpose | Type | Input | Output | Frequency |
|-------|---------|------|-------|--------|-----------|
| {e.g. User churn} | {Predict 30-day churn} | {XGBoost} | {User features} | {Probability 0-1} | {Weekly retrain} |
| {e.g. Anomaly detector} | {Flag unusual events} | {Isolation Forest} | {Event metrics} | {Anomaly score} | {Daily retrain} |

## {Model 1: e.g. User Churn Model}

### What It Predicts

*Plain language explanation of what the model does and what decisions it drives.*

### Features

| Feature | Source | Description |
|---------|--------|-------------|
| {e.g. events_last_7d} | {user_events} | {Count of events in last 7 days} |
| {e.g. days_since_last_login} | {user_events} | {Days since most recent event} |
| {e.g. plan_tier} | {crm_export} | {Subscription tier} |

### Training

```bash
# {Training command}
```

**Training data:** {What data, how much, what date range}

**Validation:** {Train/test split, cross-validation strategy}

### Evaluation

| Metric | Current | Threshold | Notes |
|--------|---------|-----------|-------|
| {e.g. AUC-ROC} | {0.84} | {> 0.75} | |
| {e.g. Precision@10%} | {0.62} | {> 0.50} | {At 10% recall} |

### Serving

**How:** {e.g. Batch predictions written to warehouse, REST API, embedded in pipeline}

**Latency:** {e.g. Batch — predictions available by 06:00 UTC}

**Fallback:** {What happens if the model is unavailable or stale?}

### Model Registry

| Version | Date | Metrics | Status |
|---------|------|---------|--------|
| {v3} | {YYYY-MM-DD} | {AUC 0.84} | {Production} |
| {v2} | {YYYY-MM-DD} | {AUC 0.81} | {Archived} |

## Retraining

*When, how, and who decides to retrain.*

| Trigger | Action |
|---------|--------|
| {Scheduled (weekly)} | {Automatic retrain + eval, promote if metrics pass} |
| {Metric degradation} | {Alert, manual review, retrain if needed} |
| {New feature added} | {Manual retrain with new feature set} |

---

[Next: The Infrastructure →](./06-the-infrastructure.md)
