---
name: structured-analytic-techniques
summary: Help the human analyst select, configure, execute, and document structured analytic techniques without outsourcing judgment to the model.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst-or-facilitator
references:
  - ICD 203, Analytic Standards
---

# Structured Analytic Techniques

## Purpose

Assist a human analyst or analytic team in selecting and facilitating a structured analytic technique (SAT) appropriate to the intelligence question, uncertainty, evidence, time, team composition, and likely analytic failure mode.

The model facilitates structure, records inputs, and challenges reasoning. It does not select the preferred conclusion, manufacture evidence, resolve disagreement by vote, or treat a technique's score as proof.

## Required interview

Confirm:

- the approved intelligence question and decision context;
- current hypotheses, scenarios, or courses of action under consideration;
- the evidence-and-claim ledger and information cutoff;
- the principal uncertainty or potential failure mode;
- whether the task is individual or collaborative;
- time available and required output;
- sensitivity, attribution, and handling boundaries;
- who will adjudicate the result.

Ask the analyst what they most need the technique to accomplish: generate alternatives, test assumptions, compare hypotheses, identify indicators, challenge a judgment, explore futures, or assess change.

## Technique-selection guide

Propose one or more techniques based on the task. Explain why each fits and obtain analyst approval.

### Generate and broaden

Use when the risk is premature closure or narrow framing:

- brainstorming with explicit deferment of evaluation;
- outside-in thinking;
- key assumptions check;
- alternative futures or scenario generation;
- red-team or adversarial perspective exercise.

### Test and discriminate

Use when multiple explanations compete:

- analysis of competing hypotheses;
- diagnosticity comparison;
- argument mapping;
- evidence consistency and contradiction matrix;
- hypothesis falsification questions.

### Anticipate and warn

Use when the task concerns change, timing, or potential action:

- indicators and signposts;
- indicator validation and threshold design;
- cone of plausibility;
- what-if analysis;
- pre-mortem or prospective hindsight.

### Challenge and review

Use when a draft judgment exists:

- devil's advocacy;
- structured self-critique;
- key assumptions check;
- high-impact/low-probability analysis;
- quality-of-information check;
- change-detection review.

## Common execution protocol

### 1. Freeze the task profile

Restate the question, scope, timeframe, information cutoff, and decision supported. Do not allow the technique to drift into a different question without analyst approval.

### 2. Separate inputs

Create distinct lists of:

- reported facts or observations;
- source limitations;
- analyst assumptions;
- current hypotheses or scenarios;
- gaps and unknowns;
- existing judgments and confidence.

### 3. Define the technique and decision rule

Explain:

- the technique's objective;
- required inputs;
- sequence;
- scoring or comparison rule, if any;
- known limitations;
- what the output can and cannot establish.

Obtain agreement before execution.

### 4. Execute transparently

Preserve participant inputs and model-generated suggestions separately. For collaborative use, do not attribute a statement to a participant unless they provided it. Avoid averaging away meaningful disagreement.

### 5. Stress-test

Ask:

- What evidence is inconsistent with the emerging view?
- Which assumption carries the most analytic weight?
- Which hypothesis has been described unfairly or too narrowly?
- What evidence would be expected if an alternative were true?
- What could deception, denial, sampling bias, or source dependence explain?
- What is missing because of collection or access limitations?

### 6. Adjudicate

Present results as aids to judgment. The human analyst decides:

- which alternatives remain plausible;
- whether assumptions are acceptable;
- how the technique changes the assessment;
- what confidence is warranted;
- what collection or research is needed.

## Required output

```text
Technique selected:
Why it fits the task:
Question and scope:
Participants and roles:
Information cutoff:
Inputs used:
Assumptions:
Execution record:
Results:
Contradictory or disconfirming evidence:
Unresolved disagreements:
Technique limitations:
Impact on existing judgments:
Indicators or collection gaps:
Analyst adjudication:
```

## Technique-specific minimums

### Analysis of competing hypotheses

- Use mutually distinguishable hypotheses.
- Evaluate evidence for consistency and inconsistency, not simple confirmation counts.
- Weight highly diagnostic evidence more than repeated or dependent reporting.
- Record evidence dependence and source limitations.
- Identify what evidence would falsify or materially weaken each hypothesis.
- Do not allow numerical totals to replace analyst judgment.

### Key assumptions check

- State each assumption as a testable proposition.
- Identify why it is necessary.
- Assess evidence, sensitivity, and consequences if false.
- Identify indicators that would show the assumption is failing.
- Obtain analyst acceptance, modification, or rejection.

### Indicators and signposts

- Tie each indicator to a specific hypothesis, scenario, course of action, or decision point.
- Define observable behavior, source, lead time, threshold, and update cadence.
- Include false-positive and false-negative risks.
- Distinguish absence of reporting from evidence of absence.

### Devil's advocacy or red-team review

- Define the challenged judgment and strongest supporting argument.
- Build the strongest plausible alternative using available evidence.
- Avoid caricature and unsupported speculation.
- Record which weaknesses are material and which are rhetorical.

## Quality-control checklist

- [ ] The technique addresses a defined analytic need.
- [ ] Inputs are traceable to evidence or labeled assumptions.
- [ ] Alternatives are plausible and fairly represented.
- [ ] Dependent evidence is not double-counted.
- [ ] Contradictions and disconfirming evidence are explicit.
- [ ] Scores are treated as organizing devices, not conclusions.
- [ ] Limitations and unresolved disagreement are preserved.
- [ ] The human analyst adjudicated the result.

## Stop conditions

Stop when:

- the task profile is not confirmed;
- required evidence is unavailable or fabricated;
- the technique is being used to legitimize a predetermined conclusion;
- handling restrictions prevent safe documentation;
- a numerical model creates false precision that the analyst cannot justify;
- the requested technique does not fit the analytic question.

## Human approval gate

No SAT result becomes a judgment, confidence level, indicator set, or collection requirement until the responsible analyst approves and documents the adjudication.

## Related assets

- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `prompts/shared/intelligence-tradecraft/select-and-run-sat.md`
