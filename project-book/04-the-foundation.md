# Chapter 4 — The Foundation

[← Back to Table of Contents](./README.md) · [Previous: The Map](./03-the-map.md) · [Next: The Build →](./05-the-build.md)

---

> Everything someone needs to go from a fresh machine to a running project.
> If someone follows this chapter and it doesn't work, this chapter is broken.

## Tech Stack

*List every major technology choice with a one-line reason for why it was chosen. Not just "what" — "why."*

| Layer | Technology | Why |
|-------|-----------|-----|
| Language | {e.g. TypeScript} | {e.g. Type safety without the Java overhead} |
| Framework | {e.g. Fastify} | {e.g. Needed raw speed, Express was the bottleneck} |
| Database | {e.g. PostgreSQL} | {e.g. Relational data, JSONB for flexibility} |
| Cache | {e.g. Redis} | {e.g. Session storage + job queues} |
| Infra | {e.g. Docker + Fly.io} | {e.g. Simple deploys, no k8s overhead} |
| CI/CD | {e.g. GitHub Actions} | {e.g. Free for open source, team already knew it} |

## Prerequisites

*What must be installed before anything else. Be exact about versions.*

- **{Tool}** {version} — [Install link]({url})
- **{Tool}** {version} — [Install link]({url})
- **{Tool}** {version} — [Install link]({url})

## Getting Started

*Step by step. Copy-pasteable. Tested. Number every step.*

### 1. Clone the repo

```bash
git clone {repo-url}
cd {project-name}
```

### 2. Install dependencies

```bash
{install command}
```

### 3. Configure environment

```bash
cp .env.example .env
```

*Explain each required variable. Don't make people guess.*

| Variable | Required | Description | Example |
|----------|----------|-------------|---------|
| `DATABASE_URL` | Yes | {What it connects to} | `postgres://localhost:5432/mydb` |
| `API_KEY` | Yes | {Where to get one} | `sk-...` |
| `DEBUG` | No | {What it does} | `true` |

### 4. Set up the database

```bash
{database setup commands}
```

### 5. Run it

```bash
{run command}
```

### 6. Verify it works

*How do they know it's actually running? What should they see? What URL to visit?*

```
Expected output:
> Server running at http://localhost:{port}
> Connected to database
> Ready
```

## Common Setup Issues

*Things that go wrong during setup and how to fix them. If you've seen it happen twice, document it here.*

### {Error message or symptom}

**Cause:** {Why this happens}

**Fix:**
```bash
*The command or change that fixes it*
```

### {Error message or symptom}

**Cause:** {Why this happens}

**Fix:**
```bash
*The command or change that fixes it*
```

---

[Next: The Build →](./05-the-build.md)
