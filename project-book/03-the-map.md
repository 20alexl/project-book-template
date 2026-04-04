# Chapter 3 — The Map

[← Back to Table of Contents](./README.md) · [Previous: The Vision](./02-the-vision.md) · [Next: The Foundation →](./04-the-foundation.md)

---

> This is the tour. Walk the reader through the system like you're showing a new teammate around the building.
> Use diagrams. Use plain language. Name things clearly.

## The Big Picture

*Start with the highest-level view. What are the major pieces and how do they relate? Include a diagram — even ASCII art works.*

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│              │     │              │     │              │
│  {Component} │────▶│  {Component} │────▶│  {Component} │
│              │     │              │     │              │
└──────────────┘     └──────────────┘     └──────────────┘
        │                                        │
        ▼                                        ▼
┌──────────────┐                         ┌──────────────┐
│              │                         │              │
│  {Component} │                         │  {Component} │
│              │                         │              │
└──────────────┘                         └──────────────┘
```

## The Tour

*Walk through each major component. For each one, explain:*

### {Component Name}

**What it does:** {One sentence}

**Why it exists:** {What problem does this specific piece solve?}

**What it talks to:** {Which other components does it interact with, and how?}

**Where it lives:** {File path, service name, repo — wherever someone would go to find it}

### {Component Name}

**What it does:** {One sentence}

**Why it exists:** {What problem does this specific piece solve?}

**What it talks to:** {Which other components does it interact with, and how?}

**Where it lives:** {File path, service name, repo}

### {Component Name}

**What it does:** {One sentence}

**Why it exists:** {What problem does this specific piece solve?}

**What it talks to:** {Which other components does it interact with, and how?}

**Where it lives:** {File path, service name, repo}

## How Data Flows

*Pick 1-2 core user actions and trace the data through the entire system. "When a user does X, here's what happens step by step." This is worth more than any amount of API documentation.*

### Flow: {e.g. "User submits a payment"}

```
1. User clicks "Pay" in the frontend
       │
       ▼
2. POST /api/payments hits the API gateway
       │
       ▼
3. PaymentService validates the request
       │
       ▼
4. Stripe API is called to create a charge
       │
       ▼
5. Webhook confirms payment, event is published
       │
       ▼
6. OrderService picks up the event, updates status
```

*Add as many flows as needed to cover the core paths through your system.*

## Directory Structure

*Show the repo layout with annotations. This is the physical map that corresponds to the logical map above.*

```
├── src/
│   ├── api/              # {What lives here}
│   ├── services/         # {What lives here}
│   ├── models/           # {What lives here}
│   ├── integrations/     # {What lives here}
│   └── utils/            # {What lives here}
├── config/               # {What lives here}
├── scripts/              # {What lives here}
├── tests/                # {What lives here}
└── project-book/         # You are here
```

---

[Next: The Foundation →](./04-the-foundation.md)
