# Analysis of Competing Hypotheses

## Purpose
Test multiple plausible explanations for any event, activity, outcome, relationship, or forecast.

## Interaction rule
Ask the user to confirm the focal question, candidate hypotheses, evidence corpus, time period, confidence vocabulary, and whether the task is explanatory, attributional, or predictive. If hypotheses are missing, propose a diverse set and obtain approval before scoring them.

## Required parameters
- Focal question
- Approved hypotheses or permission to propose them
- Evidence corpus
- Scope and time period
- Weighting and confidence conventions

## Prompt
Evaluate the approved hypotheses using an Analysis of Competing Hypotheses method.

Build an evidence-by-hypothesis matrix. Rate each item as highly consistent, consistent, neutral, inconsistent, or highly inconsistent with each hypothesis. For every item assess:
- Reliability and credibility
- Source proximity
- Independence or derivation
- Diagnosticity
- Recency
- Deception or manipulation risk
- Whether absence of evidence is meaningful

Emphasize disconfirming evidence rather than counting supportive items. Identify assumptions embedded in each hypothesis and evidence that would invalidate them.

Produce:
1. Approved hypothesis set
2. ACH matrix
3. Most diagnostic evidence
4. Evidence vulnerable to denial, deception, or circular sourcing
5. Sensitivity analysis showing whether reasonable reweighting changes the result
6. Least inconsistent hypothesis or tied hypotheses
7. Residual uncertainty
8. Collection most likely to discriminate among hypotheses

Do not force a winner when the evidence does not discriminate. Do not convert the least inconsistent hypothesis into certainty.