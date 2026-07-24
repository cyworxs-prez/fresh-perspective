---
name: assessment-language-and-confidence
summary: Help a human analyst express judgments, likelihood, uncertainty, and confidence clearly while preserving evidence traceability and organizational standards.
description: Help a human analyst express judgments, likelihood, uncertainty, and confidence clearly while preserving evidence traceability and organizational standards.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst-or-reviewer
references:
  - ICD 203, Analytic Standards
---

# Assessment Language and Confidence

## Purpose

Help the human analyst draft and review key judgments so readers can distinguish what is known, what is assessed, how likely an outcome is, why the analyst holds the judgment, and how much confidence the analyst places in it.

The model may propose wording and expose inconsistencies. The analyst assigns and approves likelihood terms, confidence, assumptions, implications, and changes from prior judgments.

## Required interview

Confirm:

- the approved task profile and intended consumer;
- the organization's authorized estimative-language lexicon and probability bands, if any;
- whether likelihood and confidence are required, optional, or product-line specific;
- the information cutoff and evidence ledger;
- the required product length and level of explanation;
- prior judgments that must be compared or updated;
- classification, sourcing, and release constraints;
- the responsible analyst and reviewer.

Do not invent a probability scale. If no scale is provided, ask the analyst whether to use plain-language likelihood terms without numeric bands or to adopt an explicitly labeled working convention.

## Core distinctions

### Judgment versus fact

A fact reports information established by evidence. A judgment interprets information, estimates an outcome, explains causation, or assesses meaning. Mark analytic judgments with appropriate estimative language rather than presenting them as observed fact.

### Likelihood versus confidence

- **Likelihood** communicates the assessed probability of an event, condition, explanation, or outcome.
- **Confidence** communicates the analyst's trust in the judgment given source quality, corroboration, knowledge gaps, assumptions, analytic complexity, and potential deception.

Do not use confidence as a synonym for likelihood.

### Uncertainty versus ambiguity

- **Uncertainty** reflects incomplete knowledge about what is or will be true.
- **Ambiguity** reflects multiple plausible interpretations of available information.

Represent both when material.

## Key-judgment construction

For each proposed judgment, help the analyst complete:

```text
Judgment ID:
Question answered:
Assessment statement:
Likelihood term:
Confidence level:
Principal supporting evidence:
Material contradictory evidence:
Critical assumptions:
Alternative explanation or outcome:
Why the alternative is less, equally, or more plausible:
Information gaps:
Indicators that would change the judgment:
Change from previous judgment:
Decision relevance or implication:
Analyst approval:
```

## Drafting method

### 1. State the judgment first

Lead with the answer, not the research chronology. Keep the subject, assessed behavior or outcome, timeframe, and scope explicit.

### 2. Use calibrated language consistently

Apply only the organization's approved terms. Do not mix equivalent-sounding terms casually. Avoid words such as possible, may, could, expected, likely, almost certainly, and unlikely when their meaning is undefined or inconsistent within the product.

When the product permits numeric ranges, ensure the word and range align. When it does not, do not add false precision.

### 3. Explain the basis

Identify the principal evidence and reasoning supporting the judgment. A long source list is not a rationale. Explain which evidence is most diagnostic and why.

### 4. Explain uncertainty

Identify source limitations, reporting gaps, assumptions, contradiction, deception risk, analytic complexity, and temporal uncertainty that materially affect the judgment.

### 5. Address alternatives

Present plausible alternatives fairly. State what evidence supports them and what would cause the analyst to revise the judgment.

### 6. Explain change or consistency

When updating prior analysis, state whether the judgment changed, the confidence changed, or the evidence base changed. Explain the reason. Do not imply change merely because wording changed.

### 7. Tie to the consumer's decision

Describe implications, opportunities, risks, indicators, or planning considerations without crossing into unauthorized policy advocacy or command decision-making.

## Confidence-support framework

The model may help the analyst examine:

- quality and credibility of underlying sources;
- source access and independence;
- corroboration and contradiction;
- directness and diagnostic value of evidence;
- data completeness and representativeness;
- stability of critical assumptions;
- analytic complexity and number of inferential steps;
- potential denial, deception, advocacy, or manipulation;
- consistency with established knowledge and reasons for departure;
- recency and expected rate of change.

Do not calculate confidence mechanically. A score or checklist may organize discussion, but the analyst must provide the final confidence judgment and rationale.

## Language checks

Flag:

- facts written as assessments or assessments written as facts;
- likelihood terms without a defined referent or timeframe;
- confidence labels without rationale;
- policy recommendations presented as intelligence judgments;
- causal claims supported only by correlation or sequence;
- intent inferred solely from capability, contact, investment, or rhetoric;
- absolute wording unsupported by the evidence;
- passive constructions that hide the actor or source of judgment;
- stacked caveats that make the judgment unintelligible;
- inconsistent probability terminology across the product;
- a key judgment that does not answer the intelligence question.

## Output

Produce:

1. revised key-judgment register;
2. likelihood and confidence consistency table;
3. fact/inference/assumption issues;
4. unsupported or overstated language findings;
5. alternatives and change-detection findings;
6. analyst adjudication log.

## Quality-control checklist

- [ ] Every key judgment answers a defined question.
- [ ] The subject, outcome, scope, and timeframe are explicit.
- [ ] Likelihood and confidence are distinct.
- [ ] The approved lexicon is used consistently.
- [ ] Evidence and reasoning are traceable.
- [ ] Material contradiction, assumptions, and gaps are visible.
- [ ] Alternatives are fairly represented.
- [ ] Changes from prior analysis are explained.
- [ ] Implications are relevant and do not become unauthorized advocacy.
- [ ] The analyst approved each judgment and confidence statement.

## Stop conditions

Stop and ask the analyst when:

- the probability lexicon or confidence convention is unknown;
- the evidence ledger is inadequate to support the requested wording;
- the user asks the model to assign confidence without analyst review;
- the task requires a predetermined conclusion;
- changes from prior analysis cannot be explained from available evidence;
- a requested statement would conceal uncertainty or contradict known sourcing limitations.

## Human approval gate

No judgment, likelihood term, confidence level, implication, or change statement is final until the human analyst approves it.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/ic/icd/icd-203-analytic-standards/`
- `templates/intelligence/key-judgment-register.md`
- `prompts/shared/intelligence-tradecraft/draft-key-judgments.md`
