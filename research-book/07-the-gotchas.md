# Chapter 7 — The Gotchas

[← Back to Table of Contents](./README.md) · [Previous: The Results](./06-the-results.md) · [Next: Related Work →](./08-related-work.md)

---

> The stuff that wasted hours. The bugs that looked like features. The things the paper doesn't mention.
> If you spent a day debugging something, write it down so the next person doesn't.

## How to Read This Chapter

Each gotcha follows the same format:

- **The Symptom** — What you see
- **The Cause** — Why it's happening
- **The Fix** — How to resolve it
- **The Lesson** — What to remember

---

### Gotcha: {Descriptive title}

**Symptom:** {What does this look like?}

**Cause:** {Why does this happen?}

**Fix:**
```bash
*Commands or code changes*
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

## Environment Gotchas

*Things specific to the software/hardware setup that cause problems.*

| Issue | Symptom | Fix |
|-------|---------|-----|
| {e.g. CUDA version mismatch} | {e.g. "no kernel image" error} | {e.g. Install torch with matching CUDA} |
| {e.g. Memory overflow at scale} | {e.g. OOM at 10K samples} | {e.g. Reduce batch size or use gradient accumulation} |

## Things That Look Wrong But Aren't

| Behavior | Why It Looks Wrong | Why It's Expected |
|----------|-------------------|-------------------|
| {e.g. Loss spikes at epoch 50} | {Seems like divergence} | {Learning rate warmup schedule} |
| {e.g. Metric drops then recovers} | {Seems like regression} | {Exploration phase in RL loop} |

---

> **Contributing:** If you spent more than 30 minutes debugging something, add it here.

---

[Next: Related Work →](./08-related-work.md)
