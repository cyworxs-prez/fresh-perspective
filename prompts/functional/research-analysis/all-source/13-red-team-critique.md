# Red-Team Analytic Critique

## Purpose
Identify methodological, evidentiary, logical, and presentation weaknesses in any research or analytic product before publication.

## Interaction rule
Ask the user to provide the draft, intended audience, supported decision, evidence corpus, governing analytic standard, acceptable risk level, and desired review depth. Clarify whether the review should address substance, sourcing, writing, security, legal concerns, or all of them.

## Required parameters
- Draft product
- Intended audience and decision
- Approved evidence corpus
- Applicable tradecraft or quality standard
- Review scope and severity scale

## Prompt
Act as an adversarial but constructive analytic reviewer. Evaluate the draft for:
- Unsupported or overstated claims
- Circular, derivative, or non-independent sourcing
- Conflation of activity, correlation, intent, causation, influence, leverage, control, and effect
- Guilt by association or identity-based inference
- Ignored stakeholder agency
- Missing or weak alternative explanations
- Confirmation bias and assumption dependence
- False precision or inconsistent scoring
- Stale, incomplete, or selectively used evidence
- Chronology errors and causal gaps
- Weak indicators or non-diagnostic thresholds
- Forecasts without time horizon or signposts
- Conclusions not tied to the supported decision
- Missing caveats, sourcing, or handling restrictions
- Language that exceeds the evidence

Return a table with:
1. Issue
2. Severity
3. Exact location
4. Why it matters
5. Evidence or logic affected
6. Specific recommended correction
7. Whether the correction changes the bottom-line judgment

End with the three most consequential weaknesses, the strongest surviving judgment, and the minimum changes required before publication.