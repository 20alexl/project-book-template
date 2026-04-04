# Chapter 8 — Monitoring

[← Back to Table of Contents](./README.md) · [Previous: The Gotchas](./07-the-gotchas.md) · [Next: The Roadmap →](./09-the-roadmap.md)

---

> How to know the pipeline is healthy, and how to know it's broken.
> Data pipelines fail silently more often than they fail loudly.
>
> **Skip this chapter** if the pipeline runs manually or ad-hoc with no production SLAs.

## Health Dashboard

*Link to dashboard or describe what to check.*

**Where to look:** {e.g. Grafana at grafana.internal/d/pipeline-health}

## Key Metrics

| Metric | Healthy Range | Warning | Critical | Where to Check |
|--------|-------------|---------|----------|---------------|
| {e.g. Pipeline runtime} | {< 45 min} | {45-60 min} | {> 60 min} | {Airflow UI} |
| {e.g. Row count delta} | {< 10% change} | {10-30%} | {> 30% or zero} | {Data quality dashboard} |
| {e.g. Data freshness} | {< 4 hours} | {4-8 hours} | {> 8 hours} | {Freshness monitor} |
| {e.g. Model prediction latency} | {< 100ms p99} | {100-500ms} | {> 500ms} | {APM} |

## Alerts

| Alert | Condition | Severity | Who Gets Paged | Runbook |
|-------|-----------|----------|---------------|---------|
| {e.g. Pipeline failed} | {DAG task fails} | {High} | {Data eng on-call} | {See below} |
| {e.g. Data freshness SLA breach} | {> 8h stale} | {High} | {Data eng on-call} | {See below} |
| {e.g. Row count anomaly} | {> 30% change} | {Medium} | {Data eng Slack} | {See below} |
| {e.g. Model metric degradation} | {AUC < 0.75} | {Medium} | {ML eng Slack} | {See below} |

## Runbooks

### Pipeline Failed

1. Check Airflow task logs for error
2. {Common fix 1}
3. {Common fix 2}
4. If source issue, check {source system status page}
5. Rerun failed task: `{command}`

### Data Freshness Breach

1. Check if source delivered data: `{check command}`
2. Check if ingestion ran: `{check command}`
3. If source is late, wait and monitor
4. If ingestion failed, check logs and rerun

### Row Count Anomaly

1. Check if the change is real (holidays, marketing campaigns, etc.)
2. Compare source row count to staged count
3. If mismatch, check for schema changes or ingestion errors
4. If real, acknowledge alert and document

## SLAs

| Metric | SLA | Measured How |
|--------|-----|-------------|
| {e.g. Data freshness} | {Data available by 06:00 UTC} | {Timestamp of last write} |
| {e.g. Pipeline uptime} | {99% monthly} | {Successful runs / total scheduled} |
| {e.g. Prediction serving} | {p99 < 200ms} | {APM trace} |

---

[Next: The Roadmap →](./09-the-roadmap.md)
