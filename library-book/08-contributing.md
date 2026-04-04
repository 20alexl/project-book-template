# Chapter 8 — Contributing

[← Back to Table of Contents](./README.md) · [Previous: The Gotchas](./07-the-gotchas.md) · [Next: The Roadmap →](./09-the-roadmap.md)

---

> Everything someone needs to go from "I want to contribute" to "I submitted a PR."
> Don't assume they know your toolchain.

## Development Setup

```bash
# Clone
git clone {repo-url}
cd {repo-name}

# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install in development mode
pip install -e ".[dev]"
```

## Running Tests

```bash
# Run all tests
pytest

# Run specific test file
pytest tests/test_{module}.py

# Run with coverage
pytest --cov={library-name}
```

## Code Style

*What tools and conventions does this project use?*

```bash
# Format
{e.g. ruff format .}

# Lint
{e.g. ruff check .}

# Type check
{e.g. pyright}
```

## Before Submitting a PR

- [ ] All tests pass
- [ ] New code has tests
- [ ] Code is formatted and linted
- [ ] {Any other requirements}

## Project Structure for Contributors

*Where to put things. What goes where.*

| I want to... | Look in / Add to |
|--------------|-----------------|
| Fix a bug | `src/{library}/` — find the relevant module |
| Add a feature | `src/{library}/` — and add tests in `tests/` |
| Update docs | `library-book/` |
| Add a test | `tests/` — follow existing patterns |

## How Decisions Are Made

*How does this project handle feature requests, design disagreements, and breaking changes? Who decides?*

---

[Next: The Roadmap →](./09-the-roadmap.md)
