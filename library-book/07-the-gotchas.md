# Chapter 7 — The Gotchas

[← Back to Table of Contents](./README.md) · [Previous: Advanced Usage](./06-advanced-usage.md) · [Next: Contributing →](./08-contributing.md)

---

> Common mistakes, confusing behavior, and things that will waste your time if you don't know.
> Every entry here saves someone hours of debugging.

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
```python
{Fix}
```

**Lesson:** {Takeaway}

---

### Gotcha: {Descriptive title}

**Symptom:** {What you see}

**Cause:** {Why it happens}

**Fix:**
```python
{Fix}
```

**Lesson:** {Takeaway}

---

## Common Mistakes

*Patterns that new users frequently get wrong.*

| Mistake | What They Write | What They Should Write |
|---------|----------------|----------------------|
| {e.g. Forgetting to close} | `x = lib.open()` | `with lib.open() as x:` |

## Things That Look Like Bugs But Aren't

| Behavior | Why It Looks Wrong | Why It's Intentional |
|----------|-------------------|---------------------|
| {Behavior} | {Why confusing} | {Why it's correct} |

## Migration Guide

*If there are breaking changes between versions, document the migration path.*

### Migrating from {vX} to {vY}

| Old API | New API | Notes |
|---------|---------|-------|
| `old_function()` | `new_function()` | {Why it changed} |

---

> **Contributing:** If you hit something confusing, add it here. There is no gotcha too small.

---

[Next: Contributing →](./08-contributing.md)
