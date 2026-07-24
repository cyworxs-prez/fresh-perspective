---
name: analyst-interview-and-scope
summary: Interview the human analyst and establish a confirmed intelligence task profile before substantive analytic work.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst-or-planner
references:
  - ICD 203, Analytic Standards
  - Joint Publication 2-0, Joint Intelligence
---

# Analyst Interview and Scope

## Purpose

Help a human analyst, planner, or reviewer convert an informal request into a bounded, reviewable intelligence task. This skill is mandatory at the start of every substantive analytic workflow unless the current conversation already contains a complete and explicitly confirmed task profile.

The model supports problem framing. It does not choose the mission, intelligence question, audience, actors, geography, assumptions, desired conclusion, confidence, or dissemination authority.

## Activate when

Use this skill when the user asks to:

- begin an assessment, estimate, JIPOE, IPB, warning, network, capability, or threat analysis;
- review or update an existing intelligence product;
- create an analytic workflow, recurring monitoring effort, or decision-support product;
- apply a structured analytic technique;
- draft key judgments or assessment language.

## Do not use as a substitute for

- formal intelligence requirements validation;
- command or agency tasking authority;
- classification, disclosure, legal, privacy, or records review;
- supervisor or product-line approval.

## Interview method

Ask questions in manageable groups. Do not present a long questionnaire when several answers can be inferred from documents the user has authorized the model to inspect. Never infer a material element without confirming it.

### 1. Decision and mission context

Determine:

- What decision, plan, operation, campaign, warning problem, or policy question will this support?
- Who requested the work and who is the accountable analyst or office?
- What would the consumer do differently based on the answer?
- Is the task descriptive, explanatory, estimative, comparative, warning-oriented, or evaluative?

### 2. Intelligence question

Capture one primary intelligence question and, when needed, supporting questions.

Test whether the question:

- identifies the subject or actor;
- specifies the behavior, capability, condition, outcome, or uncertainty of interest;
- establishes a timeframe;
- supports a decision rather than merely requesting information;
- avoids embedding an unproven premise or desired conclusion.

Rewrite only as a proposal and obtain the analyst's confirmation.

### 3. Scope

Confirm:

- geographic area, operational environment, area of operations, and area of interest as applicable;
- relevant actors, partners, neutral parties, populations, systems, and domains;
- historical baseline and information cutoff;
- near-, mid-, or long-term horizon;
- exclusions and issues intentionally out of scope;
- level of analysis: strategic, operational, tactical, organizational, network, system, or event.

### 4. Sources and access

Ask:

- Which reporting, databases, documents, repositories, and systems of record are authorized?
- Which sources are mandatory?
- Are any relevant sources unavailable, stale, restricted, or pending?
- Is the task based on finished intelligence, raw reporting, publicly available information, commercially available information, liaison reporting, diplomatic reporting, or a mixture?
- What source-citation and retrieval requirements apply?

Record the information cutoff and source-access limitations.

### 5. Product and audience

Confirm:

- intended consumer and their level of subject familiarity;
- required product type, length, format, visuals, and delivery channel;
- required key judgments, implications, indicators, collection gaps, or recommendations;
- deadline, update cadence, and review stages;
- applicable doctrine, product-line guidance, style guide, and quality standard.

### 6. Handling and authority

Confirm:

- classification and compartmentation boundaries;
- releasability and foreign disclosure constraints;
- privacy, civil liberties, legal, contractual, and records requirements;
- whether the model may draft, retrieve, transform, summarize, or only review;
- who approves judgments, confidence, markings, release, and dissemination.

The model must not determine or alter official markings.

## Task-profile output

Before substantive work, present the following for confirmation:

```text
Primary intelligence question:
Decision or mission supported:
Intended consumer:
Analytic purpose:
Geographic and functional scope:
Relevant actors and systems:
Time horizon:
Historical baseline:
Information cutoff:
Authorized source set:
Known source limitations:
Required product and format:
Applicable doctrine and local standards:
Handling and release constraints:
Assumptions authorized by the analyst:
Explicit exclusions:
Review and approval authority:
Unresolved questions:
```

Ask the analyst to approve or correct the profile.

## Processing rules

- Do not begin substantive analysis until material ambiguities are resolved or explicitly accepted as assumptions.
- Label analyst-provided assumptions and do not convert them into facts.
- Do not treat a requester's wording as proof of an actor's intent, capability, attribution, or responsibility.
- Do not broaden the scope because additional information is available.
- Do not narrow the scope merely to make the task easier.
- Do not invent sources, reporting, access, collection, or organizational requirements.
- If the deadline prevents adequate treatment, identify the minimum viable product and residual risk for analyst approval.

## Stop and escalate when

Stop and ask the analyst when:

- the primary intelligence question cannot be identified;
- the requested conclusion is predetermined;
- critical evidence is unavailable and the user asks the model to fill gaps;
- authority, handling, or dissemination boundaries are unclear;
- the task requires access the user has not authorized;
- competing interpretations of the task would materially change the method or result.

## Quality-control checklist

- [ ] The task supports an identifiable decision or mission.
- [ ] The primary question is answerable and does not presume the conclusion.
- [ ] Scope, timeframe, actors, domains, and exclusions are explicit.
- [ ] The information cutoff and authorized source set are recorded.
- [ ] Product, audience, handling, and approval requirements are defined.
- [ ] Assumptions and unresolved questions are visible.
- [ ] The analyst explicitly confirmed the task profile.

## Human approval gate

The skill is complete only when the human analyst confirms the task profile. All downstream skills must treat that profile as configuration, not as evidence.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/shared/intelligence-tradecraft/structured-analytic-techniques/`
- `templates/intelligence/analysis-profile.md`
- `prompts/shared/intelligence-tradecraft/interview-and-scope.md`
