# Chapter 7 — The Gotchas

[← Back to Table of Contents](./README.md) · [Previous: The Infrastructure](./06-the-infrastructure.md) · [Next: Monitoring →](./08-monitoring.md)

---

> Data gotchas are the worst kind — they're silent. The pipeline succeeds, the dashboard looks fine,
> and the numbers are wrong. Every entry here prevents a bad decision based on bad data.

## How to Read This Chapter

Each gotcha follows the same format:

- **The Symptom** — What you observe (or don't)
- **The Cause** — Why it's happening
- **The Fix** — How to resolve it
- **The Blast Radius** — What downstream was affected

---

### Gotcha: {Descriptive title}

**Symptom:** {e.g. "Revenue numbers drop 20% on Mondays"}

**Cause:** {e.g. "Source system batches weekend events into Monday's export"}

**Fix:** {e.g. "Use event timestamp, not export timestamp, for date partitioning"}

**Blast Radius:** {e.g. "Revenue dashboard, weekly reports, churn model training data"}

---

### Gotcha: {Descriptive title}

**Symptom:** {What you observe}

**Cause:** {Why}

**Fix:** {Resolution}

**Blast Radius:** {What's affected}

---

## Silent Failures

*Things that go wrong without raising alerts. The most dangerous category.*

| Failure | Why It's Silent | How to Detect | How to Prevent |
|---------|----------------|---------------|----------------|
| {e.g. Source schema change} | {Pipeline still runs, new column ignored} | {Schema diff check} | {Contract test on ingestion} |
| {e.g. Partial source data} | {Row count looks normal} | {Compare to expected count} | {Freshness + completeness check} |
| {e.g. Timezone shift} | {Numbers look plausible} | {Compare day boundaries to source} | {Force UTC everywhere} |

## Data Quality Traps

| Trap | How It Manifests | Prevention |
|------|-----------------|-----------|
| {e.g. String "NULL" vs actual null} | {Counts are wrong} | {Normalize on ingestion} |
| {e.g. Duplicate records from retry} | {Inflated metrics} | {Dedupe on natural key} |
| {e.g. Encoding issues (Latin-1 vs UTF-8)} | {Garbled text, failed joins} | {Force UTF-8, validate on read} |

## Things That Look Wrong But Aren't

| Observation | Why It Looks Wrong | Why It's Expected |
|-------------|-------------------|-------------------|
| {e.g. Row count drops on holidays} | {Seems like data loss} | {Fewer events on holidays is real} |
| {e.g. Model scores shift after retrain} | {Seems like regression} | {New features change score distribution, same AUC} |

---

> **Contributing:** If you found bad data downstream, trace it back and document the gotcha here.

---

[Next: Monitoring →](./08-monitoring.md)
