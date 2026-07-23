# Fresh Perspective

A curated library of reusable AI skills, prompts, analytical frameworks, workflows, and automations.

## Purpose

Fresh Perspective is designed to make high-quality reasoning and staff-work processes reusable, auditable, and easy to adapt across domains. Each collection should be self-contained, clearly scoped, and sanitized of project-specific details unless the collection is intentionally case-specific.

## Repository structure

```text
skills/
  <collection-name>/
    README.md
    <skill-name>/SKILL.md
    templates/
prompts/
  <domain-or-workflow>/
workflows/
  <domain-or-function>/
automations/
  <domain-or-function>/
frameworks/
  <framework-name>/
templates/
examples/
docs/
```

## Core content types

- **Skills** define reusable capabilities, tradecraft, constraints, and expected outputs.
- **Prompts** provide model-ready instructions for bounded tasks.
- **Workflows** define end-to-end human and machine processes, including decision points and review gates.
- **Automations** define triggers, schedules, connectors, execution prompts, logging, retries, and approval controls.
- **Frameworks** provide reusable analytical or operational structures.
- **Templates** provide schemas, ledgers, report formats, and configuration files.

## Initial collections

- `skills/influence-access-analysis/` — actor-neutral country, territory, region, theater, and subnational influence, access, infrastructure, network, indicators-and-warning, analytic-standards, and decision-support skills.
- `workflows/staff-work/` — repeatable procedures for inbox management, reporting, activity capture, task tracking, and executive support.
- `automations/staff-work/` — scheduled and event-driven specifications for automating routine staff work.

## Contribution standards

- Keep assets reusable and domain-appropriate.
- Remove references to prior clients, countries, adversaries, reports, or outputs unless essential to the asset.
- Require an explicit scope profile when geography, target actor, partner, mission, audience, or planning horizon would change the analysis.
- Never inherit country, adversary, partner, or mission assumptions from a previous output without confirmation.
- Separate fact, inference, assumption, severity, and confidence.
- Include safety, privacy, source-quality, and approval controls where relevant.
- Prefer modular skills and workflows over monolithic prompts.
- Store reusable tables, schemas, ledgers, and configuration examples in `templates/`.
- Define authoritative sources, audit records, failure behavior, and human review gates.
- Ensure scheduled tasks state both the machine-readable schedule and the plain-language cadence.

## Status

Early-stage library. Structure and naming conventions may evolve as additional skills, prompts, workflows, and automations are added.
