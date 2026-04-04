# Chapter 9 — The Roadmap

[← Back to Table of Contents](./README.md) · [Previous: Monitoring](./08-monitoring.md) · [Next: Appendix →](./10-appendix.md)

---

> Where this system is going and what was deliberately left out.

## Current State

| Component | Status | Confidence |
|-----------|--------|------------|
| {e.g. Core pipeline} | {Stable} | {High — running 6 months} |
| {e.g. ML model v3} | {Production} | {Medium — needs more features} |
| {e.g. Real-time layer} | {Planned} | {Low — not started} |

## What's Next

- [ ] {e.g. Add real-time event processing for time-sensitive alerts}
- [ ] {e.g. Migrate from Airflow to Dagster for better testing}
- [ ] {e.g. Add data catalog integration}

## What Was Deliberately Left Out

| Feature | Why Not |
|---------|---------|
| {e.g. Real-time streaming} | {e.g. Batch is sufficient for current SLAs, streaming adds complexity} |
| {e.g. Multi-region} | {e.g. All users in one region, not worth the cost} |
| {e.g. Self-serve feature store} | {e.g. Team is small enough to coordinate manually} |

## Technical Debt

*Be honest about what's duct-taped.*

| Debt | Impact | Priority |
|------|--------|----------|
| {e.g. Hardcoded source paths} | {Can't add sources without code changes} | {Medium} |
| {e.g. No integration tests} | {Schema changes caught in prod} | {High} |

---

[Next: Appendix →](./10-appendix.md)
