# Changelog

All notable changes to this project will be documented in this file.

Format follows [Keep a Changelog](https://keepachangelog.com/).

## [0.4.0] - 2026-02-21

### Added
- PR coaching bot for actionable contributor feedback
- Audit backlog: batch triage with dedup clustering and shareable reports
- Contributor badges: exemplary PRs and well-formed issues get recognition
- Vision document generation: LLM-powered synthesis from repo docs and PR history

### Removed
- Frozen security CLI commands (scanners, CVE, data-flow) excluded from package

## [0.3.0] - 2026-02-17

### Added
- Label automation via embeddings + vision document taxonomy
- Contributor profiles from PR history (merge rate, test rate, expertise areas)
- Review routing based on CODEOWNERS and past review patterns
- Cross-PR conflict detection via file overlap + embedding similarity
- Smart stale detection: semantic staleness instead of timer-based
- Issue-to-PR linking via embedding similarity
- Issue triage: 3-tier pipeline for GitHub issues

## [0.2.0] - 2026-02-16

### Added
- Multi-provider LLM support for Tier 3 (OpenRouter, OpenAI, Anthropic, Gemini, generic)
- GitHub Action for full 3-tier pipeline in CI
- Batch triage script for large PR backlogs

## [0.1.0] - 2026-02-15

### Added
- Initial PR triage with three-tier gated pipeline (embeddings, heuristics, LLM)
- Vision document support for project-level governance policy
- MCP server for tool integration
- CLI via Typer
