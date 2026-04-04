# Chapter 3 — The Data

[← Back to Table of Contents](./README.md) · [Previous: The Design](./02-the-design.md) · [Next: The Pipeline →](./04-the-pipeline.md)

---

> Everything about the data itself: where it comes from, what it looks like, and how good it is.

## Data Sources

| Source | Type | Frequency | Format | Volume | Owner |
|--------|------|-----------|--------|--------|-------|
| {e.g. User events} | {e.g. Kafka topic} | {e.g. Real-time} | {e.g. JSON} | {e.g. ~10M/day} | {e.g. Product team} |
| {e.g. CRM export} | {e.g. SFTP CSV} | {e.g. Daily} | {e.g. CSV} | {e.g. ~500K rows} | {e.g. Sales ops} |
| {e.g. Public API} | {e.g. REST} | {e.g. Hourly pull} | {e.g. JSON} | {e.g. ~50K records} | {e.g. External} |

## Schemas

### {Source/Table: e.g. user_events}

| Column | Type | Nullable | Description |
|--------|------|----------|-------------|
| {event_id} | {string} | {No} | {Unique event identifier} |
| {user_id} | {string} | {No} | {User identifier} |
| {event_type} | {string} | {No} | {e.g. click, purchase, view} |
| {timestamp} | {datetime} | {No} | {UTC} |
| {properties} | {json} | {Yes} | {Event-specific metadata} |

### {Source/Table: e.g. processed_output}

| Column | Type | Nullable | Description |
|--------|------|----------|-------------|
| {field} | {type} | {nullable} | {description} |

## Data Quality

### Known Issues

| Issue | Source | Impact | Mitigation |
|-------|--------|--------|-----------|
| {e.g. Duplicate events} | {e.g. Kafka at-least-once} | {e.g. Inflated counts} | {e.g. Dedupe on event_id in staging} |
| {e.g. Late arrivals} | {e.g. Mobile clients} | {e.g. Missing from daily batch} | {e.g. 3-day reprocessing window} |
| {e.g. Null user_id} | {e.g. Anonymous users} | {e.g. Can't join to user table} | {e.g. Session-based ID fallback} |

### Quality Checks

| Check | Where | Threshold | Action on Failure |
|-------|-------|-----------|------------------|
| {e.g. Row count > 0} | {After ingestion} | {> 0} | {Fail pipeline} |
| {e.g. Null rate on key columns} | {After transform} | {< 5%} | {Alert + continue} |
| {e.g. Schema match} | {Before write} | {Exact match} | {Fail pipeline} |

## Data Lineage

*Where does each output field come from? This is the section that saves debugging hours.*

```text
output.user_segment
  ← transform: classify_user()
    ← source: user_events.event_type (aggregated)
    ← source: crm_export.plan_tier
```

## Access and Permissions

*Who can access what, and how.*

| Data | Who Can Access | How |
|------|---------------|-----|
| {Raw events} | {Data engineering} | {Direct S3 access} |
| {Processed tables} | {All analysts} | {Warehouse query} |
| {PII data} | {Compliance team only} | {Restricted role} |

---

[Next: The Pipeline →](./04-the-pipeline.md)
