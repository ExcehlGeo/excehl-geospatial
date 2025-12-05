# Workflow Overview

This document outlines common development and automation workflows used across ExcehlGeo repositories.

## Branching & Development

- Work in feature branches
- Use descriptive names: `feat/geoai-parser`, `fix/crs-mismatch`
- Merge into `main` via PRs with automated checks

## CI/CD with GitHub Actions

Typical workflows include:

- **Linting** (e.g., `ruff`, `black`)
- **Testing** (e.g., `pytest`)
- **Builds** (for web tools or data pipelines)
- **Data refreshes** (scheduled or triggered)

## Automation Patterns

- Use `Make` or GitHub Actions to orchestrate:
  - Data ingestion
  - Format conversion (e.g., GeoJSON → Parquet)
  - Metadata extraction
  - Notion sync triggers

## Logging & Auditability

- Prefer structured logs with timestamps
- Include commit hashes in automated outputs
- Use tags or commit prefixes to trigger downstream actions

## External Integrations

- Notion: sync key metadata (see `INTEGRATIONS.md`)
- Antigravity: trigger workflows via commit tags or PR events
