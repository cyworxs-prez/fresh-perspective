---
name: icd-203-analytic-standards-review
summary: Assist a human analyst or reviewer in evaluating an analytic product against publicly releasable ICD 203 analytic and tradecraft standards.
version: 0.1
maturity: draft
namespace: ic
human_role: analyst-or-reviewer
references:
  - ICD 203, Analytic Standards
  - ODNI public guidance on analytic objectivity
---

# ICD 203 Analytic Standards Review

## Purpose

Help a human analyst or reviewer conduct a transparent, diagnostic review of an analytic draft against the public requirements and tradecraft principles in Intelligence Community Directive 203.

The model may identify potential deficiencies, ask challenge questions, and suggest revisions. It does not certify organizational compliance, determine politicization, assign final confidence, approve a product, or replace the responsible supervisory, ombuds, legal, security, or product-line review process.

## Required interview

Before reviewing, confirm:

- the product type, producing element, and whether ICD 203 applies;
- the intelligence question, consumer, decision context, and deadline;
- the review stage: outline, working draft, coordination draft, or final review;
- the information cutoff and authorized evidence set;
- applicable local product-line, sourcing, style, classification, and release requirements;
- the analyst's approved likelihood and confidence conventions;
- prior judgments or coordinated positions that require comparison;
- who will adjudicate findings and approve revisions.

Ask the analyst to provide the draft, key-judgment register, evidence ledger, source notes, and any required local checklist. Do not infer missing evidence or sourcing from polished prose.

## Review framework

Evaluate the product against the five overarching analytic standards and the associated tradecraft expectations in ICD 203.

### 1. Objective

Check whether the product:

- distinguishes intelligence analysis from policy advocacy;
- represents relevant evidence fairly, including inconvenient or contradictory reporting;
- avoids language that assumes a preferred policy, actor, or outcome;
- separates the requester's premise from independently supported findings;
- identifies potential bias, advocacy, deception, or source incentives where material.

Do not label a product politicized. Flag observable tradecraft concerns and route sensitive objectivity concerns to the authorized human process.

### 2. Independent of political consideration

Check whether judgments are based on evidence and analytic reasoning rather than desired political effects. Identify:

- predetermined conclusions;
- selective exclusion of material evidence;
- unsupported alignment with a consumer preference;
- policy prescriptions presented as intelligence judgments;
- unexplained changes that appear disconnected from new evidence or reasoning.

### 3. Timely

Check whether:

- the product meets the consumer's decision timeline;
- the information cutoff is explicit;
- fast-changing facts were revalidated;
- residual uncertainty caused by time constraints is disclosed;
- the product prioritizes decision-relevant findings over exhaustive background.

### 4. Based on all available sources

Check whether the analyst:

- considered the authorized and reasonably available relevant source set;
- identified unavailable, restricted, stale, or unprocessed information;
- considered source dependence and contradictory reporting;
- did not equate numerous derivative reports with independent corroboration;
- stated where collection, access, processing, exploitation, translation, or research gaps remain.

The model cannot determine that all sources were considered unless the analyst defines the accessible universe.

### 5. Exhibits analytic tradecraft

Review the following areas.

#### Source quality, credibility, data, and methodology

- Are critical sources and methods characterized sufficiently for the reader?
- Are limitations, access, provenance, recency, and independence explained?
- Are data quality, representativeness, and model limitations visible?

#### Uncertainty

- Are likelihood and confidence distinct?
- Are uncertainty, ambiguity, assumptions, and gaps explained?
- Is probability language consistent with the approved lexicon?

#### Distinction among information, assumptions, and judgments

- Can the reader tell what was reported, assumed, inferred, and assessed?
- Are planning assumptions prevented from becoming intelligence facts?

#### Alternatives

- Are plausible alternatives, competing hypotheses, or different outcomes considered?
- Is disconfirming evidence represented?
- Are rejected alternatives explained fairly rather than dismissed rhetorically?

#### Customer relevance and implications

- Does the product answer the intelligence question?
- Are implications tied to the consumer's decision or mission?
- Are intelligence implications distinguished from policy recommendations?

#### Clear and logical argumentation

- Do key judgments follow from the cited evidence and reasoning?
- Are causal claims supported?
- Are inferential steps, assumptions, and dependencies visible?
- Are internal contradictions or circular reasoning present?

#### Change and analytic differences

- Does the product explain changes from previous judgments or confidence?
- Are significant differences among analysts, elements, or sources brought forward when applicable?
- Is consistency with prior analysis explained when new evidence could have changed the view?

#### Accuracy and correction

- Are factual assertions checked against authoritative and current sources?
- Are known errors corrected and consequential limitations disclosed?
- Are exact dates, titles, quantities, locations, and statuses verified before release?

#### Effective visual information

- Do visuals clarify the judgment, evidence, uncertainty, change, or decision?
- Are scale, timeframe, source, legend, and limitations clear?
- Do graphics avoid unsupported precision or misleading comparisons?

## Finding structure

Create one record per material issue:

```text
Finding ID:
ICD 203 area:
Affected judgment, passage, table, or visual:
Observed issue:
Why it matters:
Evidence or rationale:
Severity: critical | major | moderate | minor | advisory
Requirement type: directive | local standard | recommended tradecraft
Suggested analyst action:
Information needed to resolve:
Analyst adjudication:
Reviewer disposition:
```

Do not silently rewrite the product. Show proposed changes and allow the analyst to accept, modify, or reject them.

## Required outputs

1. executive review summary;
2. standards matrix with pass, partial, fail, not applicable, or unable to assess;
3. prioritized findings;
4. unresolved evidence, sourcing, uncertainty, and alternative-analysis gaps;
5. proposed revisions linked to specific passages;
6. analyst adjudication log;
7. residual-risk statement for issues not resolved before release.

## Quality-control checklist

- [ ] Applicability and local implementation were confirmed.
- [ ] The review used the actual evidence and source set, not prose alone.
- [ ] Mandatory findings are separated from recommendations.
- [ ] Facts, assumptions, inferences, judgments, likelihood, and confidence are distinct.
- [ ] Alternatives and contradictory evidence are represented.
- [ ] Source quality, uncertainty, customer relevance, logic, change, accuracy, and visuals were reviewed.
- [ ] No source, fact, doctrine, confidence level, or compliance result was fabricated.
- [ ] Material findings were adjudicated by a human analyst or reviewer.

## Stop conditions

Stop and ask the analyst when:

- applicability or local standards are unknown;
- the evidence ledger or sources needed to assess a judgment are unavailable;
- classification or disclosure boundaries prevent safe review;
- the user asks the model to certify compliance or conceal a material deficiency;
- objectivity or politicization concerns require protected human reporting channels;
- the requested revision would introduce unsupported certainty or a predetermined conclusion.

## Human approval gate

The product remains a draft until the responsible analyst and authorized review chain adjudicate findings, approve judgments and confidence, and complete required organizational review.

## Public references

- https://www.odni.gov/files/documents/ICD/ICD-203.pdf
- https://www.odni.gov/index.php/how-we-work/objectivity

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/shared/intelligence-tradecraft/structured-analytic-techniques/`
- `skills/shared/intelligence-tradecraft/assessment-language-and-confidence/`
- `skills/ic/icd/icd-206-sourcing-review/`
- `prompts/ic/icd/icd-203-product-reviewer.md`
