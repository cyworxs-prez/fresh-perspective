---
name: evidence-and-claim-ledger
summary: Build and maintain a traceable ledger connecting reported information, source characterization, assumptions, inferences, and analytic judgments.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst
references:
  - ICD 203, Analytic Standards
  - ICD 206, Sourcing Requirements for Disseminated Analytic Products
---

# Evidence and Claim Ledger

## Purpose

Help the human analyst create a transparent evidence base before drafting conclusions. The skill decomposes reporting and judgments into auditable records so the analyst can evaluate source quality, independence, corroboration, contradiction, uncertainty, and information gaps.

The model may organize and compare evidence. It must not invent reporting, citations, source access, reliability, credibility, or corroboration.

## Required interview

Before creating or updating a ledger, confirm:

- the approved task profile and primary intelligence question;
- the authorized source set and systems of record;
- information cutoff and freshness requirements;
- applicable sourcing, citation, classification, and disclosure rules;
- whether the ledger may contain source-identifying details or must use protected descriptors;
- the analyst's preferred source-evaluation scheme;
- required output format and storage location.

If no source-evaluation scheme is mandated, propose an organization-neutral schema and obtain approval before applying it.

## Core distinctions

Maintain separate fields for:

1. **Reported information** — what a source states, depicts, measures, or records.
2. **Source characterization** — access, provenance, competence, incentives, methodology, recency, and limitations.
3. **Corroboration status** — independent support, partial support, contradiction, or no independent confirmation.
4. **Analytic inference** — reasoning that connects information to a possible explanation or consequence.
5. **Assumption** — a proposition accepted for the analysis but not established by evidence.
6. **Judgment** — the analyst's answer or assessment.
7. **Confidence contribution** — how the evidence affects, but does not automatically determine, confidence.

Do not collapse these categories into a single narrative sentence.

## Ledger schema

Use one row per material claim or evidentiary proposition.

```text
Claim ID:
Task or judgment supported:
Claim text:
Claim type: reported-information | inference | assumption | judgment
Source ID and retrievable citation:
Source type and originating organization:
Publication, collection, or observation date:
Date accessed:
Information cutoff status:
Source access or methodology:
Source strengths:
Source limitations:
Reliability or provenance assessment:
Information credibility assessment:
Independence group:
What the source directly supports:
What the source does not establish:
Corroborating evidence:
Contradictory evidence:
Alternative explanations:
Geographic, actor, domain, and temporal relevance:
Confidence contribution:
Handling or releasability note:
Analyst adjudication:
Reviewer comments:
```

Use the organization's required fields when they differ.

## Method

### Step 1: Decompose the question

Break the primary intelligence question into decision-relevant propositions. Examples include capability, intent, access, control, readiness, dependency, attribution, timing, scale, and likely effect. Do not treat evidence of one proposition as proof of another.

### Step 2: Normalize source records

For every source, record enough information for an authorized reviewer to retrieve or identify it under applicable rules. Preserve the original wording separately from any model-generated summary.

### Step 3: Identify provenance and dependence

Determine whether multiple items derive from the same:

- original report;
- press release or public statement;
- anonymous source;
- imagery or dataset;
- government briefing;
- commercial database;
- wire report;
- social-media post;
- analytic product.

Place dependent items in the same independence group. Repetition is not corroboration.

### Step 4: Characterize quality and relevance

Help the analyst consider:

- source access and competence;
- proximity to the event or issue;
- method transparency and reproducibility;
- known incentives, advocacy, deception, or audience effects;
- recency and temporal fit;
- whether the source directly supports the claim or only provides context;
- whether aggregation hides variation or uncertainty.

Do not assign a formal source rating unless the analyst authorizes the scale and adjudicates the result.

### Step 5: Map evidence to judgments

For each key judgment, show:

- supporting claims;
- contradicting claims;
- assumptions;
- evidence dependencies;
- material gaps;
- evidence that would increase or decrease confidence;
- plausible alternative interpretations.

### Step 6: Identify collection and research gaps

Convert missing evidence into bounded questions. Distinguish a collection gap from a processing, access, translation, exploitation, or research gap. Do not claim that a gap requires new collection when existing reporting may be undiscovered or unavailable to the model.

## Output artifacts

Produce:

1. source register;
2. claim-and-evidence ledger;
3. judgment-to-evidence map;
4. contradiction and alternative-explanation list;
5. assumptions register;
6. collection and research gaps;
7. source-access and information-cutoff note.

## Quality-control checks

- [ ] Every material factual claim has an authorized, retrievable source reference.
- [ ] Source quality is described rather than implied by citation count.
- [ ] Dependent reporting is not counted as independent corroboration.
- [ ] Direct reporting is separated from inference and assumption.
- [ ] Contradictory evidence is visible.
- [ ] What each source does not establish is recorded for critical claims.
- [ ] Stale or temporally mismatched evidence is flagged.
- [ ] Gaps are not filled with model-generated facts.
- [ ] The analyst adjudicated material source and evidence judgments.

## Stop conditions

Stop and ask the analyst when:

- a cited source cannot be retrieved or verified;
- the source descriptor would expose information outside the permitted environment;
- the source set is too incomplete to support the requested judgment;
- reporting conflicts cannot be represented without additional context;
- the model cannot distinguish an original source from derivative reporting;
- a user asks for a fabricated citation, report, or source rating.

## Human approval gate

The human analyst must approve the ledger, evidence dependencies, material contradictions, assumptions, and gaps before the model uses them to draft key judgments.

## Related assets

- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `skills/ic/icd/icd-206-sourcing-review/`
- `templates/intelligence/evidence-claim-ledger.md`
- `prompts/shared/intelligence-tradecraft/build-evidence-ledger.md`
