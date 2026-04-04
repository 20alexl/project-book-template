# Chapter 5 — The Build

[← Back to Table of Contents](./README.md) · [Previous: The Foundation](./04-the-foundation.md) · [Next: The Integrations →](./06-the-integrations.md)

---

> This is the biggest chapter. Explain how the core systems work, layer by layer.
> Write it like you're pair programming with someone on their first day.
> Prose does the heavy lifting. Code snippets illustrate — they don't replace explanation.

## Overview

*A brief recap of the major components from Chapter 3, but now you're going to go deep on each one. Tell the reader what order you'll cover things and why that order makes sense.*

---

## {Core System 1}

### What It Does

*Explain the responsibility of this system in plain language.*

### How It Works

*Walk through the logic. Not line-by-line code review — the *thinking* behind the code. Why is it structured this way? What pattern does it follow?*

```python
# Show the key code — the part that matters
# Not the whole file, just the conceptual core
```

*Explain what the code does and why the approach was chosen.*

### Key Decisions

*What non-obvious choices were made here? Why? What would break if you changed them?*

### Where to Find It

```
src/{path-to-relevant-files}
```

---

## {Core System 2}

### What It Does

*Same structure. Explain the responsibility.*

### How It Works

*Walk through the logic.*

```python
# Key code snippet
```

*Explanation.*

### Key Decisions

*Non-obvious choices and their rationale.*

### Where to Find It

```
src/{path-to-relevant-files}
```

---

## {Core System 3}

### What It Does

*Same structure.*

### How It Works

*Walk through the logic.*

### Key Decisions

*Non-obvious choices.*

### Where to Find It

```
src/{path-to-relevant-files}
```

---

## How the Pieces Talk to Each Other

*Now that the reader understands each system individually, explain how they interact. What calls what? What's synchronous vs async? Where are the boundaries?*

---

## Testing Strategy

*How is this project tested? Not "we use Jest" — what's the philosophy? What gets unit tested vs integration tested vs not tested at all? Why?*

### Running Tests

```bash
{test commands}
```

### Writing Tests

*Conventions, patterns, where test files live, any helpers or fixtures available.*

---

[Next: The Integrations →](./06-the-integrations.md)
