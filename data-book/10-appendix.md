# Appendix — Reference

[← Back to Table of Contents](./README.md) · [Previous: The Roadmap](./09-the-roadmap.md)

---

## Schema Catalog

*Complete schema definitions for all tables/datasets.*

### {Table: e.g. dim_users}

| Column | Type | Nullable | PK | Description |
|--------|------|----------|-----|-------------|
| {user_id} | {string} | {No} | {Yes} | {Unique user identifier} |
| {created_at} | {timestamp} | {No} | | {Account creation date, UTC} |
| {segment} | {string} | {Yes} | | {Computed user segment} |

### {Table: e.g. fact_events}

| Column | Type | Nullable | PK | Description |
|--------|------|----------|-----|-------------|
| {field} | {type} | {nullable} | {pk} | {description} |

## Configuration Reference

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| {key} | {type} | {default} | {What it controls} |

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| {VAR_NAME} | {Yes/No} | {What it does} |

## SQL Snippets

*Useful queries for debugging, investigation, or ad-hoc analysis.*

### {Check data freshness}

```sql
{Query}
```

### {Find duplicates}

```sql
{Query}
```

### {Compare source to warehouse}

```sql
{Query}
```

## Glossary

| Term | Definition |
|------|-----------|
| {Term} | {What it means in this system} |

## Links

- {Orchestrator UI}
- {Monitoring dashboard}
- {Data catalog}
- {Related pipelines}

---

[← Back to Table of Contents](./README.md)
