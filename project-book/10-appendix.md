# Appendix — Reference

[← Back to Table of Contents](./README.md) · [Previous: The Roadmap](./09-the-roadmap.md)

---

> The traditional reference docs live here — API specs, config schemas, environment variables.
> By the time someone reaches this chapter, they have full context from the chapters before.
> This is the lookup table, not the textbook.

## API Reference

*List your endpoints. Keep it scannable. Link to OpenAPI/Swagger if you have it.*

### `{METHOD} {/path}`

**Description:** {What it does}

**Auth:** {Required? What kind?}

**Request:**
```json
{
  "field": "type — description"
}
```

**Response:** `{status code}`
```json
{
  "field": "type — description"
}
```

---

### `{METHOD} {/path}`

**Description:** {What it does}

**Auth:** {Required? What kind?}

**Request:**
```json
{}
```

**Response:** `{status code}`
```json
{}
```

---

*Add more endpoints as needed.*

## Configuration Reference

*Every config option with its type, default, and description.*

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `{config.key}` | `{string}` | `{default}` | {What it controls} |
| `{config.key}` | `{number}` | `{default}` | {What it controls} |
| `{config.key}` | `{boolean}` | `{false}` | {What it controls} |

## Environment Variables

*Complete list. Duplicates Chapter 4 intentionally — this is the reference version.*

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `{VAR_NAME}` | {Yes/No} | {default} | {What it does} |
| `{VAR_NAME}` | {Yes/No} | {default} | {What it does} |
| `{VAR_NAME}` | {Yes/No} | {default} | {What it does} |

## Error Codes

*If your system has specific error codes, document them here.*

| Code | Meaning | Common Cause | Resolution |
|------|---------|-------------|------------|
| `{ERR_001}` | {Description} | {Why it happens} | {How to fix} |
| `{ERR_002}` | {Description} | {Why it happens} | {How to fix} |

## Glossary

*Terms specific to this project that might confuse newcomers.*

| Term | Meaning |
|------|---------|
| {Term} | {Definition in context of this project} |
| {Term} | {Definition in context of this project} |
| {Term} | {Definition in context of this project} |

## Links & Resources

*External resources that are relevant to understanding or working on this project.*

| Resource | URL | Why It's Relevant |
|----------|-----|-------------------|
| {e.g. Stripe API Docs} | {url} | {We use their Payments API} |
| {e.g. RFC 7519 (JWT)} | {url} | {Our auth is built on this} |
| {e.g. Architecture Decision Records} | {url} | {Historical decision context} |

---

<sub>End of Project Book. If something is missing, add it. If something is wrong, fix it. This is a living document.</sub>

[← Back to Table of Contents](./README.md)
