---
name: ipb-evaluate-threat
summary: Build an evidence-based threat model covering organization, capabilities, doctrine, behavior, dependencies, vulnerabilities, and constraints.
description: Build an evidence-based threat model covering organization, capabilities, doctrine, behavior, dependencies, vulnerabilities, and constraints.
version: 0.1
maturity: draft
namespace: army
human_role: analyst-or-planner
references:
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - ADP 2-0, Intelligence
---

# IPB: Evaluate the Threat

## Purpose

Assist a human analyst in developing a mission-relevant threat model without collapsing reported capability, doctrinal capability, demonstrated behavior, intent, readiness, and analytic judgment into one category.

## Mandatory interview

Confirm:

- actor or threat set and level of analysis;
- supported mission, decision, echelon, and planning horizon;
- whether the task concerns capability, intent, disposition, readiness, behavior, vulnerability, or all of these;
- authorized source set and information cutoff;
- required threat model, graphic, matrix, or written product;
- classification, handling, disclosure, and approval boundaries.

## Required inputs

- current order of battle and disposition information when authorized;
- doctrine, training patterns, historical behavior, and observed tactics;
- capability, readiness, sustainment, command-and-control, and dependency reporting;
- relevant environmental effects;
- source and confidence limitations.

## Method

1. Establish actor identity, objectives, constraints, and operating context.
2. Build or update order of battle and disposition as supported by evidence.
3. Distinguish doctrinal, assessed, observed, and demonstrated capabilities.
4. Evaluate command and control, intelligence, fires, maneuver, protection, sustainment, information, cyber, electromagnetic, space, and other relevant functions.
5. Identify critical capabilities, requirements, dependencies, vulnerabilities, and failure points.
6. Compare current behavior against doctrine, historical precedent, and environmental constraints.
7. Identify likely adaptations, deception opportunities, indicators, and gaps.
8. Record source support, alternatives, and confidence for each material judgment.

## Evidence rules

Do not infer intent solely from capability. Do not infer capability solely from doctrine. Do not treat absence of reporting as evidence of absence unless the collection environment supports that inference.

## Output

- actor and objective summary;
- threat organization and capability model;
- disposition and readiness assessment;
- critical capabilities, dependencies, vulnerabilities, and constraints;
- observed departures from doctrine or baseline;
- indicators, assumptions, alternatives, confidence, and gaps;
- candidate implications for human adjudication.

## Quality checks

- intent and capability remain separate;
- doctrinal and demonstrated capability remain separate;
- readiness and sustainability are addressed;
- dependencies and vulnerabilities are evidence-based;
- contradictory reporting and plausible alternatives are visible;
- every key judgment traces to evidence.

## Stop conditions

Stop when actor identity, timeframe, evidence currency, source dependence, or essential capability data are too uncertain to support the requested judgment.

## Human approval gate

The analyst approves the threat model before it is used for COA development, targeting support, warning, collection planning, or commander briefing.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/army/intelligence/ipb-determine-threat-courses-of-action/`
- `templates/intelligence/threat-capability-model.md`
- `prompts/army/intelligence/ipb-evaluate-threat.md`