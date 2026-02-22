# Contributing to OSS Maintainer Toolkit

Thanks for your interest in contributing! This guide covers the basics.

## Setup

```bash
# Clone and install in editable mode with dev + gatekeeper extras
git clone https://github.com/pranayom/oss-maintainer-toolkit.git
cd oss-maintainer-toolkit
pip install -e ".[dev,gatekeeper]"
```

## Running Tests

```bash
pytest                  # run the full suite
pytest -x               # stop on first failure
pytest tests/test_foo.py # run a specific file
```

Tests use `respx` for HTTP mocking and don't require a GitHub token or network access.

## Submitting a PR

1. Fork the repo and create a feature branch from `master`.
2. Make your changes and add tests for new functionality.
3. Run `pytest` to confirm all tests pass.
4. Open a PR with a clear description of what changed and why.

## Project Scope

This project handles **PR/issue governance and triage only**:
PR assessment, issue triage, linking, labeling, staleness detection,
contributor profiles, review routing, and conflict detection.

The repository contains legacy security tools (`scanners/`, `analysis/`, `cve/`)
that are **frozen** and will move to a separate project. Please do not modify
or extend those directories.

## Architecture

The core engine is a three-tier gated pipeline:

- **Tier 1** — Embedding-based analysis (sentence-transformers, cosine similarity)
- **Tier 2** — Deterministic heuristic rules (pure Python)
- **Tier 3** — LLM semantic analysis (OpenRouter free models, optional)

Tiers run strictly in sequence. Each tier is a gate. See `CLAUDE.md` for full details.

## Questions?

Open an issue if something is unclear. We're happy to help.
