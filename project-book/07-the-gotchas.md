# Chapter 7 — The Gotchas

[← Back to Table of Contents](./README.md) · [Previous: The Integrations](./06-the-integrations.md) · [Next: The Operations →](./08-the-operations.md)

---

> This is the tribal knowledge chapter — the stuff that lives in people's heads.
> Every entry here represents hours of debugging that someone already did.
> If you learn something the hard way, add it here so the next person doesn't have to.

## How to Read This Chapter

Each gotcha follows the same format:

- **The Symptom** — What you see that makes you think something is wrong
- **The Cause** — Why it's happening
- **The Fix** — How to resolve it
- **The Lesson** — What to remember going forward

---

### Gotcha: {Descriptive title}

**Symptom:** {What does this look like when you encounter it?}

**Cause:** {Why does this happen? What's the underlying issue?}

**Fix:**
```bash
*Commands or code changes that resolve it*
```

**Lesson:** {The takeaway. What should someone remember to avoid this in the future?}

---

### Gotcha: {Descriptive title}

**Symptom:** {What you see}

**Cause:** {Why it happens}

**Fix:**
```bash
{Resolution}
```

**Lesson:** {Takeaway}

---

### Gotcha: {Descriptive title}

**Symptom:** {What you see}

**Cause:** {Why it happens}

**Fix:**
```bash
{Resolution}
```

**Lesson:** {Takeaway}

---

## Things That Look Like Bugs But Aren't

*Behaviors that seem wrong but are actually intentional. Explain why they exist so people don't "fix" them.*

| Behavior | Why It Looks Wrong | Why It's Intentional |
|----------|-------------------|---------------------|
| {e.g. "Response takes 3s on first request"} | {Seems slow} | {Cold start — connection pool initializing} |
| {e.g. "Deleted items still appear for 60s"} | {Seems like a bug} | {Cache TTL — eventual consistency by design} |

---

## Known Limitations

*Things the system genuinely can't do or doesn't handle well. Be honest — this saves people from building on false assumptions.*

| Limitation | Impact | Workaround (if any) |
|-----------|--------|---------------------|
| {e.g. Max 10K records per query} | {Pagination required for large datasets} | {Use cursor-based pagination} |
| {e.g. No WebSocket support} | {No real-time updates} | {Poll every 5s or use SSE} |

---

> **Contributing to this chapter:** If you spent more than 30 minutes debugging something, add it here. Future teammates will thank you. There is no gotcha too small.

---

[Next: The Operations →](./08-the-operations.md)
