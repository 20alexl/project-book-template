# Project Book Template

A layered, narrative documentation format for software projects. Reads like a book — not a pile of READMEs.

## The Problem

Documentation usually falls into two traps: either it's a bare README that tells you nothing, or it's a sprawling wiki that tells you everything in no particular order. Both fail the person who actually needs to understand the project.

## The Solution

A **Project Book** is a single folder of numbered markdown files that tell the story of your project from the ground up. Each chapter builds on the last. Someone can read front to back and understand the entire system, or jump to a specific chapter when they need it.

## Limitations

**Inserting chapters is manual.** Files are numbered and nav links are hardcoded. Adding a chapter in the middle means renaming files and updating links. In practice this rarely happens — you set up the structure once. If you anticipate changes, leave gaps in your numbering (00, 05, 10, 15...).

**This doesn't scale to hundreds of pages.** If your project needs full-text search across 200+ docs, cross-references between teams, or versioned API docs — you've outgrown this template and should look at a static site generator. That's fine. This covers the 80% of projects that never get there.

## Pick Your Variant

Different projects need different stories. Pick the one that fits:

| Building a... | Use |
|---------------|-----|
| Web app, API, microservice, deployed software | [`project-book/`](./project-book/) |
| Research project, paper companion, experiments | [`research-book/`](./research-book/) |
| Open source library, CLI tool, package | [`library-book/`](./library-book/) |
| Robot, PCB, embedded system, IoT device | [`hardware-book/`](./hardware-book/) |
| Data pipeline, ETL, ML system | [`data-book/`](./data-book/) |

### [`project-book/`](./project-book/) — Production Software

For deployed services, apps, and production systems. Covers architecture, setup, build details, integrations, operations, and runbooks.

```text
00 Elevator Pitch → 01 The Why → 02 The Vision → 03 The Map →
04 The Foundation → 05 The Build → 06 Integrations → 07 Gotchas →
08 Operations → 09 Roadmap → 10 Appendix
```

### [`research-book/`](./research-book/) — Research and Papers

For academic projects, experiments, and paper companions. Covers methodology, reproducibility, experiments, results, and related work.

```text
00 Elevator Pitch → 01 The Problem → 02 The Approach → 03 Architecture →
04 Reproducibility → 05 Experiments → 06 Results → 07 Gotchas →
08 Related Work → 09 Future Work → 10 Appendix
```

### [`library-book/`](./library-book/) — Libraries and Packages

For open source libraries, CLI tools, and packages. Covers quick start, usage guide, internals, advanced usage, and contributing.

```text
00 Elevator Pitch → 01 The Why → 02 The Design → 03 Quick Start →
04 The Internals → 05 Usage Guide → 06 Advanced Usage → 07 Gotchas →
08 Contributing → 09 Roadmap → 10 Appendix
```

### [`hardware-book/`](./hardware-book/) — Hardware, Robotics, and Embedded

For physical builds, electronics, firmware, and IoT. Covers BOM, assembly, firmware, calibration, safety, and maintenance.

```text
00 Elevator Pitch → 01 The Why → 02 The Design → 03 Architecture →
04 Bill of Materials → 05 The Build → 06 Firmware → 07 Calibration →
08 Gotchas → 09 Safety → 10 Operations → 11 Appendix
```

### [`data-book/`](./data-book/) — Data Pipelines and ML Systems

For ETL pipelines, data engineering, and ML systems. Covers data sources, schemas, pipeline stages, models, infrastructure, and monitoring.

```text
00 Elevator Pitch → 01 The Why → 02 The Design → 03 The Data →
04 The Pipeline → 05 The Models → 06 Infrastructure → 07 Gotchas →
08 Monitoring → 09 Roadmap → 10 Appendix
```

## Mixing Chapters Across Variants

Every chapter is a standalone file. If your project needs a Safety chapter from the hardware book or a Contributing guide from the library book, just copy the `.md` file into your book folder, renumber it to fit your sequence, and update the nav links.

## Why This Works

- **GitHub-native.** Markdown renders perfectly. No build tools, no static site generators. Just push and it works.
- **Sequential.** Chapters are numbered so they sort correctly in every file browser.
- **Navigable.** Every chapter has prev/next links and a link back to the table of contents.
- **Living.** It's just markdown files in your repo. Anyone can edit, PRs work normally, git blame tells you who wrote what.
- **Portable.** Works on GitHub, GitLab, Bitbucket, Gitea, or any markdown renderer.

## Getting Started

1. Pick a variant above and copy that folder into your repo
2. Delete any chapters that don't apply
3. Fill in the templates — start with Chapters 0-3
4. Link to it from your main README

Not every project needs all 11 chapters. A small CLI tool might only need Chapters 0-5 and 7. A large platform might use all of them. Use what fits — a shorter book that's accurate beats a complete one that's stale.

Add this to your repo's root README:

```markdown
## Documentation

**[Read the Project Book](./project-book/)** — the complete guide to this project.
```

## Philosophy

Every chapter answers **why** before **what**. Context before content. Story before specs.

The traditional reference material (API docs, config schemas, env vars) still exists — it's in the Appendix. But by the time someone reaches it, they understand the system well enough for the reference to actually be useful.

## License

MIT — use it however you want.
