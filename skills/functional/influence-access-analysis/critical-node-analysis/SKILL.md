---
name: critical-node-site-analysis
summary: Identify and assess physical, logical, institutional, financial, commercial, and temporal nodes relevant to access, leverage, resilience, and freedom of maneuver.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst-or-planner
references:
  - Joint Publication 2-01.3, Joint Intelligence Preparation of the Operational Environment
  - Joint Publication 5-0, Joint Planning
---

# Critical Node and Site Analysis

## Purpose

Identify specific sites, systems, institutions, services, dependencies, and decision windows that constitute critical capabilities, requirements, vulnerabilities, investments, veto points, or resilience nodes.

## Required scoping check

Resolve or explicitly assume the area of analysis, area of interest, target actor or comparative posture, local and partner actors, mission or decision, planning horizon, required capabilities, audience, sensitivity, and output format. Ask only for missing information that would materially change the analysis. Never inherit geography, actor, adversary, partner, or mission details from prior outputs.

## Node classes

- **Physical:** ports, airfields, rail hubs, roads, bridges, fuel terminals, power assets, logistics parks, industrial areas, border crossings, and cable landing stations.
- **Logical and digital:** telecom cores, cloud and data centers, identity systems, customs platforms, payment rails, control systems, satellite ground stations, cybersecurity, and surveillance platforms.
- **Institutional:** cabinets, ministries, regulators, procurement boards, courts, customs, immigration, authorities, and headquarters.
- **Financial and commercial:** lenders, concession holders, insurers, clearing banks, joint ventures, maintenance providers, and sole-source suppliers.
- **Temporal:** elections, budget cycles, leadership transitions, reviews, exercises, debt maturities, contract renewals, weather or disaster seasons, and commissioning milestones.

## Critical-factor model

For each node assess function, owner, operator, regulator, financing, maintenance dependency, data access, redundancy, throughput, failure modes, political sensitivity, target-actor relationship, operational or policy relevance, indicators, and mitigation options.

## Criticality categories

- Critical capability.
- Critical requirement.
- Critical vulnerability.
- Strategic investment.
- Veto point.
- Resilience node.

## Scoring

Score 0–4 for operational or decision relevance, target-actor access, leverage, local or partner vulnerability, immediacy, reversibility, and evidence strength. Keep confidence separate.

## Output

Produce a critical-node register and map containing node name, location or system domain, category, function, actor linkage, risk mechanism, consequence, indicators, confidence, collection gap, and mitigation.

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires identifying which specific sites, systems, institutions, or decision windows matter to access, leverage, resilience, or freedom of maneuver. Do not use it for targeting nomination, engineering vulnerability assessment, or physical-security certification — those require authorities and expertise outside this skill.

## Quality-control checklist

- [ ] Every node links to an operational or decision consequence, not just a description.
- [ ] Scores separate relevance, access, leverage, vulnerability, immediacy, reversibility, and evidence strength.
- [ ] Confidence is recorded separately from severity and scores.
- [ ] Collection gaps are stated for nodes with weak evidence.
- [ ] Sensitive infrastructure detail is limited to what the assessment requires.

## Stop conditions

Stop and ask the analyst when the scoping check cannot be completed, when node status or ownership cannot be established from authorized sources, when the user asks the model to invent throughput, redundancy, or failure-mode data, or when the requested output shades into targeting support.

## Human approval gate

The human analyst approves the node register, criticality categories, scores, and mitigation options before they inform an assessment, plan, or briefing.

## Related assets

- `skills/functional/influence-access-analysis/baseline-assessment/`
- `skills/functional/influence-access-analysis/environment-mapping/`
- `skills/functional/influence-access-analysis/indicators-warning/`
- `templates/intelligence/critical-node-register.csv`
- `templates/intelligence/influence-scoring-model.md`
