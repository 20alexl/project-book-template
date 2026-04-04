# Chapter 2 — The Design

[← Back to Table of Contents](./README.md) · [Previous: The Why](./01-the-why.md) · [Next: The Data →](./03-the-data.md)

---

> Design philosophy before showing schemas or DAGs.

## Design Principles

### 1. {Principle}

{e.g. "Idempotent everything" — every pipeline step can be re-run safely.}

### 2. {Principle}

{e.g. "Schema-first" — data contracts before code.}

### 3. {Principle}

{e.g. "Late binding" — transform at read time, not write time.}

## Key Tradeoffs

| We Chose | Over | Because |
|----------|------|---------|
| {e.g. Batch processing} | {e.g. Real-time streaming} | {e.g. Simpler, data arrives daily anyway} |
| {e.g. Parquet on S3} | {e.g. Data warehouse} | {e.g. Cost, flexibility, no vendor lock-in} |
| {e.g. dbt} | {e.g. Custom Python transforms} | {e.g. SQL-native team, version-controlled} |

## Data Contracts

*What guarantees does this system make about its output?*

| Contract | Guarantee |
|----------|-----------|
| {e.g. Freshness} | {e.g. Data no older than 24h} |
| {e.g. Completeness} | {e.g. All sources present or job fails} |
| {e.g. Schema} | {e.g. Output matches published schema, validated on write} |
| {e.g. Uniqueness} | {e.g. No duplicate records on primary key} |

## What This System Is NOT

*Explicit non-goals.*

---

[Next: The Data →](./03-the-data.md)
