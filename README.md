# Fresh Perspective

A curated library of reusable AI skills, prompts, analytical frameworks, and workflow templates.

## Purpose

Fresh Perspective is designed to make high-quality reasoning workflows reusable, auditable, and easy to adapt across domains. Each collection should be self-contained, clearly scoped, and sanitized of project-specific details unless the collection is intentionally case-specific.

## Repository structure

```text
skills/
  <collection-name>/
    README.md
    <skill-name>/SKILL.md
    templates/
prompts/
  <domain-or-workflow>/
frameworks/
  <framework-name>/
examples/
```

## Initial collection

- `skills/country-influence-analysis/` — country- and subnational-level influence, access, infrastructure, actor-network, indicators-and-warning, and decision-support analysis.

## Contribution standards

- Keep skills reusable and domain-appropriate.
- Remove references to prior clients, countries, reports, or outputs unless essential to the skill.
- Separate fact, inference, assumption, and confidence.
- Include safety, privacy, and source-quality controls where relevant.
- Prefer modular skills over monolithic prompts.
- Store reusable tables, schemas, and ledgers in `templates/`.

## Status

Early-stage library. Structure and naming conventions may evolve as additional skills and prompts are added.
