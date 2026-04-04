# Chapter 4 — The Pipeline

[← Back to Table of Contents](./README.md) · [Previous: The Data](./03-the-data.md) · [Next: The Models →](./05-the-models.md)

---

> How data flows from source to destination. Every step, every transform, every handoff.

## Pipeline Overview

```text
{Source A} ──▶ [Ingest] ──▶ [Stage] ──▶ [Transform] ──▶ [Load] ──▶ {Destination}
                  │            │             │             │
                  ▼            ▼             ▼             ▼
              {Raw zone}   {Staging}    {Warehouse}    {Serving}
```

## Stages

### 1. Ingestion

**What happens:** {Raw data lands in the system}

**How:** {e.g. Kafka consumer, SFTP pull, API poller}

**Schedule:** {e.g. Continuous, hourly, daily at 02:00 UTC}

**Output:** {e.g. Raw Parquet files in s3://bucket/raw/}

**Failure mode:** {What happens if this stage fails}

### 2. Staging

**What happens:** {Raw data is cleaned and deduplicated}

**Transforms:**
- {e.g. Deduplicate on event_id}
- {e.g. Parse timestamps to UTC}
- {e.g. Validate schema, reject bad rows}

**Output:** {e.g. Cleaned Parquet in s3://bucket/staging/}

### 3. Transform

**What happens:** {Business logic applied, features computed}

**Key transforms:**
- {e.g. User segmentation based on event frequency}
- {e.g. Revenue attribution with 7-day window}
- {e.g. Feature engineering for ML model}

**Tool:** {e.g. dbt, Spark, Python scripts}

**Output:** {e.g. Warehouse tables / feature store}

### 4. Load / Serve

**What happens:** {Processed data delivered to consumers}

**Destinations:**
- {e.g. Warehouse: analytics queries}
- {e.g. API cache: real-time serving}
- {e.g. Dashboard: Looker/Metabase}
- {e.g. ML model: training data}

## DAG

*If using an orchestrator, document the task graph.*

```text
ingest_events ──▶ stage_events ──▶ transform_users ──┐
                                                      ├──▶ load_warehouse
ingest_crm ──▶ stage_crm ──▶ transform_segments ─────┘
                                                      │
                                                      ├──▶ train_model (weekly)
                                                      │
                                                      └──▶ export_dashboard
```

## Running Locally

```bash
# {How to run the pipeline locally for development/testing}
```

## Backfills

*How to reprocess historical data.*

```bash
# {Backfill command with date range}
```

**Watch out for:** {e.g. Rate limits on source APIs, costs of reprocessing large date ranges}

---

[Next: The Models →](./05-the-models.md)
