---
name: ipb-define-operational-environment
summary: Define the operational environment, area of operations, area of interest, and intelligence problem for Army IPB.
description: Define the operational environment, area of operations, area of interest, and intelligence problem for Army IPB.
version: 0.1
maturity: draft
namespace: army
human_role: analyst-or-planner
references:
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - ADP 2-0, Intelligence
---

# IPB: Define the Operational Environment

## Purpose

Assist a human analyst in bounding the operational environment and identifying the characteristics requiring further analysis before environmental effects, threat evaluation, or course-of-action development.

## Activate when

Use for Army IPB, intelligence support to MDMP, operational planning, warning, targeting support, protection, sustainment, or civil considerations when the environment is not yet explicitly bounded.

## Do not use for

- command-approved mission analysis or operational design decisions;
- formal geospatial, weather, engineer, or legal determinations;
- the environmental-effects, threat-evaluation, or threat-COA analysis performed by the later IPB skills;
- joint-level problems better served by the JIPOE skills under `skills/joint/intelligence/`.

## Mandatory interview

Confirm:

- supported command, echelon, mission, and decision;
- primary intelligence question and planning horizon;
- area of operations, area of interest, and relevant adjacent areas;
- land, air, maritime, space, cyber, information, and human dimensions in scope;
- actors, populations, infrastructure, systems, and functions relevant to the mission;
- authorized sources, information cutoff, classification, handling, and disclosure constraints;
- required product, deadline, update cadence, and approving authority.

Restate the task profile and obtain confirmation before analysis.

## Required inputs

- commander's intent, mission, planning guidance, and operational framework when authorized;
- maps, geospatial data, boundaries, and control measures;
- current intelligence requirements and assumptions;
- relevant orders, plans, estimates, and prior assessments;
- source-access and handling limitations.

## Method

1. Define the supported decision and intelligence problem.
2. Record AO, AI, adjacent areas, and temporal boundaries.
3. Identify significant characteristics using relevant operational variables and mission variables.
4. Determine which characteristics can affect friendly, adversary, neutral, and civilian behavior.
5. Separate known conditions, assumptions, inferred conditions, and unknowns.
6. Identify information gaps and candidate requirements.
7. Produce a confirmed environment definition for use by later IPB steps.

## Evidence rules

Every material statement must link to authorized evidence or be labeled as an assumption or analytic inference. Do not fabricate boundaries, reporting, collection, or environmental conditions.

## Uncertainty and alternatives

Where the decision-relevance of a characteristic, the placement of a boundary, or the relevant-actor set is contested, present the competing options with their planning consequences rather than silently selecting one. Record the analyst's confidence and rationale for boundary and significant-characteristic decisions that later IPB steps will inherit.

## Output

- confirmed intelligence task profile;
- AO and AI definition;
- significant-characteristics register;
- initial assumptions and gaps;
- source and information-cutoff statement;
- issues requiring commander, planner, collection, geospatial, legal, or disclosure adjudication.

## Quality checks

- boundaries support the decision rather than merely copying an existing graphic;
- time horizon is explicit;
- civilian, information, infrastructure, and cross-domain factors are not omitted without rationale;
- AO and AI are not conflated;
- assumptions and gaps are visible;
- later IPB steps can trace back to this scope.

## Stop conditions

Stop and request clarification when mission, geography, timeframe, authoritative source set, or approval authority is materially ambiguous.

## Human approval gate

The analyst approves the environment definition before it is used to evaluate effects, characterize threats, generate requirements, or brief a commander.

## Related assets

- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `skills/army/intelligence/ipb-describe-environmental-effects/`
- `templates/intelligence/analysis-profile.md`
- `prompts/army/intelligence/ipb-define-operational-environment.md`