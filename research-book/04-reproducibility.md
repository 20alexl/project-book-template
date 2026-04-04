# Chapter 4 — Reproducibility

[← Back to Table of Contents](./README.md) · [Previous: The Architecture](./03-the-architecture.md) · [Next: The Experiments →](./05-the-experiments.md)

---

> This is the chapter that makes or breaks research credibility.
> Someone should be able to go from a fresh machine to running your experiments by following this page.

## Hardware

*What hardware was used? This matters for reproducing timing results, memory constraints, and GPU-specific behavior.*

| Component | Spec |
|-----------|------|
| GPU | {e.g. RTX 4070 SUPER, 12GB VRAM} |
| RAM | {e.g. 64GB} |
| CPU | {e.g. AMD Ryzen 7 5800X} |
| Storage | {e.g. 1TB NVMe SSD} |
| OS | {e.g. Ubuntu 22.04 / Windows 11 + WSL2} |

## Software Dependencies

*Exact versions matter. Pin them.*

```bash
# Python version
python --version  # {e.g. 3.12.1}

# Install dependencies
pip install -r requirements.txt
```

*Or if using conda/docker:*
```bash
# {Exact setup commands}
```

### Key Library Versions

| Library | Version | Why Pinned |
|---------|---------|------------|
| {e.g. PyTorch} | {e.g. 2.6.0+cu124} | {e.g. CUDA compatibility} |
| {e.g. numpy} | {e.g. 1.26.4} | {e.g. API changes in 2.0} |

## Data

*Where does the data come from? How to obtain it? Any preprocessing needed?*

### Obtaining the Data

```bash
# {Commands to download or generate data}
```

### Data Format

*Describe the format, schema, or structure. Include sizes.*

## Running the Experiments

*Quick-start for reproducing the main results.*

```bash
# {The command(s) that reproduce the paper's main results}
```

Expected runtime: {e.g. ~2 hours on the hardware above}

Expected output: {What files/results get generated, where}

## Random Seeds

*Document seeds used for reproducibility.*

| Experiment | Seed(s) |
|------------|---------|
| {Main results} | {e.g. 42, 137, 256} |
| {Ablation} | {e.g. 42} |

---

[Next: The Experiments →](./05-the-experiments.md)
