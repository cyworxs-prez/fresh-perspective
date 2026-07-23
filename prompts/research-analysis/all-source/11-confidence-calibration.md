# Confidence Calibration

## Purpose
Draft a transparent confidence assessment for any analytic judgment or research conclusion.

## Interaction rule
Ask the user to provide the judgment, evidence set, confidence scale, relevant deadline, and any organizational confidence standard. Clarify whether confidence concerns the evidence, attribution, causal explanation, or forecast.

## Required parameters
- Judgment or conclusion
- Supporting and contradicting evidence
- Approved confidence vocabulary
- Scope and currency requirements
- Key assumptions, if already identified

## Prompt
Assess confidence in the approved judgment by evaluating:
- Source reliability and claim credibility
- Directness and proximity
- Independence and corroboration
- Internal consistency
- Recency and temporal coverage
- Completeness and collection gaps
- Contradictory evidence
- Deception or manipulation risk
- Dependence on assumptions
- Sensitivity to alternative explanations

State:
1. What the evidence directly establishes
2. What it reasonably suggests
3. What remains unknown
4. The strongest supporting evidence
5. The strongest contradiction or alternative
6. Fragile assumptions
7. Whether the judgment survives changes to those assumptions
8. What collection would raise or lower confidence

Use this formula unless the user supplies another standard:

`[High/Moderate/Low] confidence because [quality, consistency, independence, and coverage], while confidence is limited by [gaps, contradictions, recency, or assumption sensitivity]. Confidence would increase if [specific evidence] and decrease if [disconfirming condition].`

Do not use confidence as a substitute for likelihood, impact, or analytic agreement.