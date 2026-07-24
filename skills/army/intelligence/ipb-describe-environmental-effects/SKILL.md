---
name: ipb-describe-environmental-effects
summary: Analyze how terrain, weather, civil considerations, infrastructure, information, and cross-domain conditions affect operations.
description: Analyze how terrain, weather, civil considerations, infrastructure, information, and cross-domain conditions affect operations.
version: 0.1
maturity: draft
namespace: army
human_role: analyst-or-planner
references:
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - ATP 2-01, Plan Requirements and Assess Collection
---

# IPB: Describe Environmental Effects

## Purpose

Assist a human analyst in converting observed environmental characteristics into mission-relevant effects on friendly, adversary, neutral, and civilian activities.

## Preconditions

Use only after the operational environment, decision, timeframe, and authorized source set have been confirmed.

## Mandatory interview

Confirm the supported mission, echelon, phase, decision points, force types, mobility requirements, critical capabilities, planning horizon, weather period, civil considerations, and required level of detail.

## Method

1. Identify environmental characteristics relevant to the decision.
2. Evaluate terrain and mobility, including observation, fields of fire, cover and concealment, obstacles, key terrain, and avenues of approach where applicable.
3. Evaluate weather and seasonal effects on personnel, sensors, aviation, fires, mobility, sustainment, communications, and signatures.
4. Evaluate populations, governance, infrastructure, services, economics, information, and other civil considerations.
5. Evaluate cyber, electromagnetic, space, information, and cross-domain dependencies when relevant.
6. Compare effects across friendly, adversary, neutral, and civilian actors rather than assuming symmetry.
7. Identify opportunities, constraints, vulnerabilities, decision points, indicators, and gaps.
8. Record supporting evidence and confidence for each material effect.

## Evidence rules

Separate observed conditions from assessed effects. Do not present a generic doctrinal factor as an actual effect without evidence connecting it to the mission, actor, system, and timeframe.

## Output

- environmental-effects matrix;
- mobility and access findings;
- operational opportunities and constraints;
- actor-specific effects;
- assumptions, confidence, indicators, and gaps;
- candidate planning and collection considerations for human review.

## Quality checks

- effects are tied to a specific mission or decision;
- actor effects are not assumed to be identical;
- time and season are explicit;
- physical and human terrain are integrated;
- second-order and cross-domain dependencies are considered;
- unsupported precision is avoided.

## Stop conditions

Stop when current geospatial, weather, infrastructure, population, or source data are too incomplete to support a material judgment. State what is missing and the consequence.

## Human approval gate

The analyst approves environmental effects and any proposed planning or collection implications before they enter an estimate, brief, order, or requirement.

## Related assets

- `skills/army/intelligence/ipb-define-operational-environment/`
- `skills/army/intelligence/ipb-evaluate-threat/`
- `templates/intelligence/ipb-environmental-effects-matrix.md`
- `prompts/army/intelligence/ipb-describe-environmental-effects.md`