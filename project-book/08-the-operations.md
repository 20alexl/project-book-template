# Chapter 8 — The Operations

[← Back to Table of Contents](./README.md) · [Previous: The Gotchas](./07-the-gotchas.md) · [Next: The Roadmap →](./09-the-roadmap.md)

---

> How to deploy, monitor, and keep this thing alive in production.
> Written for the person who gets paged at 2am and needs to fix something fast.
>
> **Skip this chapter** if your project isn't deployed as a service (e.g. libraries, CLI tools, local-only projects).

## Environments

| Environment | URL | Branch | Deploys |
|------------|-----|--------|---------|
| Development | `{url}` | `main` | {Auto / Manual} |
| Staging | `{url}` | `staging` | {Auto / Manual} |
| Production | `{url}` | `production` | {Auto / Manual} |

## Deploying

### Standard Deploy

```bash
{deploy command or process}
```

*What happens during a deploy? How long does it take? Is there downtime?*

### Rollback

```bash
{rollback command}
```

*How to verify the rollback worked.*

### Emergency Deploy

*If the normal process is broken, how do you get a fix out fast?*

## Monitoring

### Health Checks

| Endpoint | What It Checks | Expected Response |
|----------|---------------|-------------------|
| `GET /health` | {What it verifies} | `200 OK` |
| `GET /ready` | {What it verifies} | `200 OK` |

### Key Metrics to Watch

*What numbers should someone monitor? What's normal? What's concerning?*

| Metric | Normal Range | Warning | Critical |
|--------|-------------|---------|----------|
| {e.g. Response time p95} | {< 200ms} | {> 500ms} | {> 2s} |
| {e.g. Error rate} | {< 0.1%} | {> 1%} | {> 5%} |
| {e.g. Queue depth} | {< 100} | {> 500} | {> 2000} |

### Where to Look

| What | Where |
|------|-------|
| Logs | {e.g. Datadog, CloudWatch, local path} |
| Metrics | {e.g. Grafana dashboard URL} |
| Errors | {e.g. Sentry project URL} |
| Alerts | {e.g. PagerDuty, Slack channel} |

## When Things Break

### {Scenario: e.g. "Database connection errors"}

**Symptoms:** {What you'll see in logs/alerts}

**Likely cause:** {Most common reason}

**Steps to resolve:**
1. {Step 1}
2. {Step 2}
3. {Step 3}

**Escalation:** {Who to contact if the above doesn't work}

### {Scenario: e.g. "High memory usage"}

**Symptoms:** {What you'll see}

**Likely cause:** {Most common reason}

**Steps to resolve:**
1. {Step 1}
2. {Step 2}

### {Scenario: e.g. "Integration X is down"}

**Symptoms:** {What you'll see}

**Likely cause:** {Their outage, not ours}

**Steps to resolve:**
1. {Check their status page}
2. {What degrades gracefully vs what breaks}
3. {Manual workaround if needed}

## Scheduled Tasks

*Cron jobs, background workers, periodic maintenance — anything that runs on a schedule.*

| Task | Schedule | What It Does | What Happens If It Fails |
|------|----------|-------------|-------------------------|
| {e.g. Cleanup old sessions} | {Daily 3am UTC} | {Purges expired data} | {Disk fills up over ~2 weeks} |
| {e.g. Sync external data} | {Every 15 min} | {Pulls latest from API} | {Data goes stale} |

## Backup & Recovery

*How is data backed up? How do you restore? Has this been tested?*

| What | Method | Frequency | Recovery Time | Last Tested |
|------|--------|-----------|---------------|-------------|
| {Database} | {e.g. pg_dump to S3} | {Daily} | {~30 min} | {Date} |
| {File storage} | {e.g. S3 versioning} | {Continuous} | {~5 min} | {Date} |

---

[Next: The Roadmap →](./09-the-roadmap.md)
