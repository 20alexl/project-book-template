# Chapter 6 — The Integrations

[← Back to Table of Contents](./README.md) · [Previous: The Build](./05-the-build.md) · [Next: The Gotchas →](./07-the-gotchas.md)

---

> This is the chapter that most docs get wrong.
> Don't just list endpoints. Explain the *relationship* with each external system.
> Why do we talk to it? What do we send? What do we get back? What happens when it's down?
>
> **Skip this chapter** if your project doesn't talk to external services or APIs.

## Integration Map

*Show which external systems this project connects to and why.*

```
                    ┌─────────────────┐
                    │   Your System   │
                    └────────┬────────┘
                             │
            ┌────────────────┼────────────────┐
            ▼                ▼                ▼
    ┌───────────────┐ ┌───────────────┐ ┌───────────────┐
    │ {Service A}   │ │ {Service B}   │ │ {Service C}   │
    │ {e.g. Stripe} │ │ {e.g. Auth0}  │ │ {e.g. S3}     │
    └───────────────┘ └───────────────┘ └───────────────┘
```

---

## {Integration 1: e.g. Stripe}

### Why We Use It

*What business need does this integration serve?*

### How It's Wired

*Authentication method, SDK vs REST, which endpoints we call and why.*

### What We Send

*The data that flows from our system to theirs. Include example payloads if helpful.*

```json
{
  "example": "payload"
}
```

### What We Get Back

*The data that comes back. What do we do with it?*

### When It Breaks

*What happens when this service is down or slow? Do we retry? Queue? Fail gracefully? What does the user see?*

### Credentials & Config

| Variable | Where to Get It | Notes |
|----------|----------------|-------|
| `{API_KEY}` | {Dashboard URL or process} | {Any gotchas} |

### Where to Find the Code

```
src/integrations/{service}/
```

---

## {Integration 2}

### Why We Use It

*Business need.*

### How It's Wired

*Auth, SDK, endpoints.*

### What We Send / Get Back

*Data flow in both directions.*

### When It Breaks

*Failure mode and handling.*

### Credentials & Config

| Variable | Where to Get It | Notes |
|----------|----------------|-------|
| `{API_KEY}` | {Source} | {Notes} |

### Where to Find the Code

```
src/integrations/{service}/
```

---

## {Integration 3}

*Same structure. Repeat for each integration.*

---

## Webhooks We Receive

*If your system receives webhooks from external services, document each one.*

### {Webhook: e.g. Stripe payment.succeeded}

**Source:** {Who sends it}

**Endpoint:** `POST /webhooks/{path}`

**What triggers it:** {When does this fire?}

**What we do with it:** {How we process it}

**Verification:** {How we validate it's authentic — signatures, IP allowlists, etc.}

---

## Rate Limits & Quotas

*Document the limits you need to stay within for each integration.*

| Service | Limit | Our Typical Usage | Headroom |
|---------|-------|-------------------|----------|
| {Service A} | {e.g. 100 req/sec} | {e.g. ~30 req/sec peak} | {Comfortable / Tight / At risk} |
| {Service B} | {e.g. 10K/day} | {e.g. ~2K/day} | {Comfortable} |

---

[Next: The Gotchas →](./07-the-gotchas.md)
