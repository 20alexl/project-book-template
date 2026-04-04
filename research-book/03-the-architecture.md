# Chapter 3 — The Architecture

[← Back to Table of Contents](./README.md) · [Previous: The Approach](./02-the-approach.md) · [Next: Reproducibility →](./04-reproducibility.md)

---

> How the code maps to the methodology. Walk through the system like you're onboarding a collaborator.
>
> **Skip this chapter** if there's no significant codebase (e.g. purely analytical work).

## The Big Picture

*High-level system diagram. How do the components relate?*

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│              │     │              │     │              │
│  {Component} │────▶│  {Component} │────▶│  {Component} │
│              │     │              │     │              │
└──────────────┘     └──────────────┘     └──────────────┘
```

## Components

### {Component Name}

**What it does:** {One sentence}

**Maps to:** {Which part of the methodology from Chapter 2}

**Key implementation detail:** {The non-obvious thing about how it's built}

**Where it lives:** {File paths}

### {Component Name}

**What it does:** {One sentence}

**Maps to:** {Which part of the methodology}

**Key implementation detail:** {Non-obvious implementation choice}

**Where it lives:** {File paths}

## Data Flow

*Trace data through the system for a core operation.*

```
1. Input arrives as {format}
       │
       ▼
2. {Processing step}
       │
       ▼
3. {Processing step}
       │
       ▼
4. Output: {what comes out}
```

## Directory Structure

```
├── src/              # {What lives here}
├── experiments/      # {Experiment scripts}
├── data/             # {Data or data loaders}
├── results/          # {Output artifacts}
├── configs/          # {Hyperparameter configs}
└── research-book/    # You are here
```

---

[Next: Reproducibility →](./04-reproducibility.md)
