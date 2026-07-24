---
name: influence-source-tradecraft
summary: Collect, evaluate, corroborate, and cite evidence for area influence, access, infrastructure, and network assessments.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst
references:
  - ICD 206, Sourcing Requirements for Disseminated Analytic Products
  - ICS 206-01, public-source citation and reference guidance
---

# Influence Source Tradecraft

## Purpose

Construct a traceable evidence base for influence, access, infrastructure, dependency, and actor-network assessments.

## Required scoping check

Resolve or explicitly assume the area of analysis, area of interest, target actor or comparative posture, local and partner actors, mission or decision, planning horizon, required capabilities, audience, sensitivity, and output format. Ask only for missing information that would materially change the analysis. Never inherit geography, actor, adversary, partner, or mission details from prior outputs.

## Source hierarchy

Prioritize, when available:

1. Laws, gazettes, ministries, legislatures, regulators, procurement portals, registries, courts, and infrastructure authorities in the area of analysis.
2. Target-actor central and subnational government, diplomatic, military, security, party, financial, state-owned enterprise, and affiliated sources.
3. Relevant partner, allied, competitor, neutral, and multilateral official sources.
4. Audited company filings, lender disclosures, concession agreements, environmental filings, and exchange records.
5. Peer-reviewed research and established research institutions.
6. Reputable international and local journalism.
7. Specialist databases and commercial data providers.
8. Social media and unattributed claims as leads only.

## Evidence decomposition

For each claim, separately record whether evidence establishes contact, relationship, payment or contract, ownership or control, access, intent, activation, behavioral effect, or operational effect. Do not treat these as interchangeable.

## Source rating

Rate source reliability A–F and information credibility 1–6. Use combined notation such as B2 or F3.

## Independence test

Do not count multiple reports as corroboration when they derive from the same press release, anonymous source, allegation, government briefing, database, social-media post, or wire article.

## Deception and agenda screen

For every critical source assess access, incentives, advocacy, likely audience effect, alternative political explanations, and whether disclosure itself could be an influence action.

## Research ledger

Maintain one row per material claim with claim ID, claim text, source, publisher, dates, source type, reliability, credibility, independence group, what the source proves, what it does not prove, geographic relevance, actor or node relevance, confidence contribution, and citation.

## Current-information rule

Revalidate officeholders, military leaders, ownership, contracts, project status, legal authorities, election calendars, event dates, and infrastructure operating status immediately before release.

## Minimum corroboration standard

For high-impact judgments seek one primary source plus one independent corroborating source, or two independent high-quality sources with distinct access. If unmet, lower confidence and state the collection gap.

## Activation criteria and non-use cases

Use this skill whenever an influence, access, infrastructure, or network assessment in this collection gathers or evaluates evidence. Do not use it to authorize collection the user is not permitted to perform, to launder single-source claims into corroborated findings, or as a substitute for the shared evidence-and-claim-ledger skill when an organization mandates that schema.

## Quality-control checklist

- [ ] Every material claim has a ledger row with source, dates, and rating.
- [ ] Independence groups prevent circular corroboration.
- [ ] What each source proves and does not prove is recorded separately.
- [ ] Officeholders, contracts, and statuses were revalidated before release.
- [ ] Unmet corroboration standards lowered confidence and produced a stated gap.

## Stop conditions

Stop and ask the analyst when required source types are unavailable or unauthorized, when the user asks the model to invent, upgrade, or fabricate sourcing, ratings, or corroboration, or when a critical source fails the deception screen and no independent alternative exists.

## Human approval gate

The human analyst approves source ratings, independence groupings, corroboration status, and the research ledger before judgments built on them are drafted or released.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/functional/influence-access-analysis/baseline-assessment/`
- `skills/ic/icd/icd-206-sourcing-review/`
- `templates/intelligence/influence-claim-ledger.csv`
