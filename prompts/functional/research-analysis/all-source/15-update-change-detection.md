# Update and Change Detection

## Purpose
Refresh a standing assessment and distinguish genuinely new developments from newly reported or reinterpreted information.

## Interaction rule
Ask the user to provide the prior assessment, current evidence packet, comparison dates, scope, decision thresholds, scoring method, and desired output. Clarify whether external research is authorized and what constitutes a material change.

## Required parameters
- Previous assessment and date
- Current approved evidence set and cutoff date
- Scope and supported decision
- Materiality and threshold rules
- Existing judgments, assumptions, indicators, and scores

## Prompt
Compare the current evidence with the prior assessment.

Identify:
- Genuinely new events or conditions
- Older events reported for the first time
- Corrections, retractions, and changed source reliability
- Changed actors, relationships, capabilities, access, or dependencies
- Invalidated, strengthened, or newly introduced assumptions
- Indicator or warning-threshold crossings
- Changes in likelihood, consequence, confidence, risk, opportunity, or resilience
- Collection gaps closed, opened, or made more important
- Judgments that remain unchanged and why

For each proposed change provide:
1. Previous wording or value
2. Proposed wording or value
3. New evidence and exact citation
4. Why the evidence is diagnostic
5. Alternative explanation
6. Confidence impact
7. Decision consequence

Distinguish `new reporting` from `new reality`, and `changed evidence` from `changed analytic interpretation`. Recommend judgment changes only when supported by material evidence. End with a concise change log, retained assumptions, watch items, and next collection priorities.