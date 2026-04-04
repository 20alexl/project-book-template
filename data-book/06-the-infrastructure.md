# Chapter 6 — The Infrastructure

[← Back to Table of Contents](./README.md) · [Previous: The Models](./05-the-models.md) · [Next: The Gotchas →](./07-the-gotchas.md)

---

> Where it runs, how it's orchestrated, and how to deploy.
>
> **Skip this chapter** if the pipeline runs locally or as a simple script with no deployment infrastructure.

## Architecture

```text
┌─────────────────┐     ┌──────────────┐     ┌──────────────┐
│   Orchestrator   │────▶│   Compute    │────▶│   Storage    │
│  {e.g. Airflow}  │     │ {e.g. Spark} │     │ {e.g. S3}    │
└─────────────────┘     └──────────────┘     └──────────────┘
         │                                          │
         ▼                                          ▼
┌─────────────────┐                         ┌──────────────┐
│   Monitoring     │                         │  Warehouse   │
│ {e.g. Datadog}   │                         │ {e.g. BQ}    │
└─────────────────┘                         └──────────────┘
```

## Environments

| Environment | Purpose | Infra | Data |
|-------------|---------|-------|------|
| {Local} | {Development} | {Docker compose} | {Sample / mock} |
| {Staging} | {Integration testing} | {Same as prod, smaller} | {Copy of prod, anonymized} |
| {Production} | {Live pipeline} | {Full infra} | {Real data} |

## Key Services

| Service | What | Where | Access |
|---------|------|-------|--------|
| {Orchestrator} | {e.g. Airflow} | {e.g. airflow.internal:8080} | {SSO} |
| {Compute} | {e.g. Spark on EMR} | {e.g. AWS us-east-1} | {IAM role} |
| {Storage} | {e.g. S3} | {e.g. s3://data-pipeline-prod/} | {IAM policy} |
| {Warehouse} | {e.g. BigQuery} | {e.g. project.dataset} | {Service account} |

## Deploying

### Standard Deploy

```bash
# {Deploy command}
```

### Rollback

```bash
# {Rollback command}
```

## Cost

*What does this system cost to run? Where does the money go?*

| Component | Monthly Cost | Notes |
|-----------|-------------|-------|
| {Compute} | {$X} | {e.g. Spot instances} |
| {Storage} | {$X} | {e.g. S3 + warehouse} |
| {Orchestrator} | {$X} | |
| **Total** | **${X}** | |

## Scaling

*How to scale up/down. What's the bottleneck?*

| Scenario | Current Capacity | To Scale | Cost Impact |
|----------|-----------------|----------|-------------|
| {e.g. 2x data volume} | {Handles it} | {No changes needed} | {~20% more compute} |
| {e.g. 10x data volume} | {Pipeline too slow} | {Add Spark workers, partition differently} | {~3x compute cost} |

---

[Next: The Gotchas →](./07-the-gotchas.md)
