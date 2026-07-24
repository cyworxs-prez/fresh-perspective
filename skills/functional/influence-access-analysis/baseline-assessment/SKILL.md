---
name: area-influence-access-baseline
summary: Build an actor-neutral area influence, access, and freedom-of-maneuver baseline using DIMEFIL, PMESII-PT, ASCOPE, JIPOE, structured analytic techniques, and commander decision support.
description: Build an actor-neutral area influence, access, and freedom-of-maneuver baseline using DIMEFIL, PMESII-PT, ASCOPE, JIPOE, structured analytic techniques, and commander decision support.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst-or-planner
references:
  - Joint Publication 2-01.3, Joint Intelligence Preparation of the Operational Environment
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - ICD 203, Analytic Standards
---

# Area Influence, Access, and Freedom-of-Maneuver Baseline

## Purpose

Use this skill to produce a defensible, area-specific baseline that explains how target-actor state power, affiliated entities, commercial relationships, and local networks may shape local or partner decisions, infrastructure availability, coalition behavior, and Joint Force freedom of maneuver.

This skill is an analytic orchestrator. It invokes or emulates the companion skills in this package:

1. `source-tradecraft`
2. `environment-mapping`
3. `actor-network`
4. `critical-node-analysis`
5. `indicators-warning`
6. `commander-reporting`

## Required scoping check

Before analysis, resolve or explicitly assume:

- Area of analysis and area of interest.
- Target actor or actors, or whether the analysis is comparative or actor-agnostic.
- Local, partner, allied, neutral, and affected actors.
- Mission, decision, or policy question.
- Planning horizon and relevant event windows.
- Required access, capabilities, authorities, or outcomes.
- Audience, classification, sensitivity, and output format.

Ask the user only for missing information that would materially change the analysis. When proceeding with incomplete information, list assumptions and identify how they constrain confidence. Do not inherit geography, adversary, partner, or mission details from prior outputs.

## Governing analytic chain

Always trace findings through this chain:

**target-actor objective → DIMEFIL instrument → actor or access vector → PMESII-PT system → ASCOPE node → observable activity → local or partner behavior → operational consequence → commander decision**

Do not stop at descriptive findings such as “a target actor invested in a railway” or “a target-aligned narrative appeared online.” Explain what the activity enables, what behavior it may change, and which operational requirement could be affected.

## Scope definition

Before research, define:

- Primary country, territory, region, or subnational areas of interest.
- Planning horizon.
- Operational scenarios being considered.
- Required forms of access: routine presence, exercise access, contingency access, overflight, maritime transit, ISR, logistics, repair, rearm, medical evacuation, prepositioning, HADR, distributed operations, and coalition C2.
- Decision-makers who will consume the assessment.

## Analytical standards

### Distinguish normal engagement from malign activity

Do not label all target-actor activity malign. Use “malign” only when evidence supports one or more of the following:

- Covert or concealed direction.
- Coercion or intimidation.
- Corruption or improper inducement.
- Deception or false attribution.
- Sovereignty-eroding dependency.
- Exploitable access to sensitive systems.
- Deliberate obstruction of lawful local or partner decisions.

Commercial, diplomatic, academic, military, and cultural engagement may be strategically significant without being malign.

### Separate severity from confidence

Never combine risk and confidence into one score. A severe risk can have low confidence; a low-severity finding can have high confidence.

### Test alternatives

At minimum, test these hypotheses:

- H1: target-actor pressure or influence is driving the observed behavior.
- H2: Domestic politics or bureaucratic friction is driving it.
- H3: Normal commercial incentives explain it.
- H4: Sovereignty, safety, legal, or military concerns explain it.
- H5: Multiple factors are interacting.

## Workflow

### Phase 1: Frame the problem

Produce a concise research design containing:

- Key intelligence questions.
- Operational requirements.
- Geographic scope.
- Time horizon.
- Initial assumptions.
- Known constraints.
- Priority source categories.

### Phase 2: Build the area baseline

Develop:

- Political decision architecture.
- Military and security relationships.
- Economic and financial exposure.
- Social and elite networks.
- Information environment.
- Infrastructure and digital systems.
- Physical geography.
- Temporal decision windows.

### Phase 3: Map actors and nodes

Identify public-role actors and organizations that can approve, constrain, facilitate, revoke, or narratively shape access. Map critical physical, logical, institutional, financial, and temporal nodes.

### Phase 4: Analyze influence and access pathways

For each major issue, identify:

- Objective of the relevant actor.
- Responsible, enabling, affected, or relevant actor.
- DIMEFIL instrument.
- Local intermediary or access vector.
- Relationship mechanism.
- Influence stage: access, placement, leverage, activation, behavioral effect, operational effect.
- Observable indicators.
- Operational consequence.

### Phase 5: Conduct JIPOE overlay

Include:

- Operational environment and area of interest.
- Key systems and subsystems.
- Critical terrain and infrastructure.
- Centers of gravity and critical factors.
- Most likely and most dangerous target-actor courses of action.
- Event templates and named areas of interest.
- Decision points, PIRs, EEIs, and collection opportunities.

### Phase 6: Score and prioritize

Use the scoring template in `templates/intelligence/influence-scoring-model.md` (repository root).

### Phase 7: Produce decision support

Deliver:

- Executive summary.
- Key judgments.
- Area risk overview.
- PMESII-PT × ASCOPE matrix.
- DIMEFIL campaign assessment.
- Actor-relationship-effect map.
- Critical-node register.
- Freedom-of-maneuver consequence matrix.
- Indicators and warning dashboard.
- Commander decision matrix.
- Collection requirements.
- Alternative hypotheses.
- Assumptions and confidence.
- Lawful engagement and resilience opportunities.
- Source evaluation and bibliography.

## Required output language

Use estimative language consistently:

- “We assess” for analytic judgments.
- “Likely” for approximately 55–80 percent probability.
- “Very likely” for approximately 80–95 percent.
- “Almost certainly” for greater than 95 percent.
- “May” or “could” when probability is not sufficiently bounded.

Do not use “will” unless describing a known scheduled event or legal requirement.

## Public-person analysis safeguards

Analysis of named individuals must be limited to:

- Public office or professional role.
- Public statements.
- Publicly documented institutional relationships.
- Publicly disclosed business, board, party, academic, or organizational affiliations.
- Decision authority and policy relevance.

Do not include private addresses, private contact information, family details unrelated to public roles, travel patterns, personal vulnerabilities, or recommendations for manipulation, coercion, or targeting.

## Quality-control checklist

Before release, confirm:

- Every key judgment links to an operational consequence.
- Every named individual has a documented public role.
- Every high-impact claim is sourced or explicitly marked as an intelligence gap.
- Commercial activity is not automatically characterized as malign.
- Alternative hypotheses are addressed.
- Severity and confidence are separate.
- Current leaders, contracts, projects, and dates are revalidated.
- Visuals match the underlying evidence.
- Recommendations are lawful, transparent, sovereignty-respecting, and resilience-oriented.

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires a full area influence-and-access baseline that sequences the companion skills in this collection. Do not use it for a single-question task a companion skill answers alone, as a substitute for command-approved JIPOE or IPB, or for operational planning, targeting, or engagement decisions — it informs them.

## Stop conditions

Stop and ask the analyst when the scoping check cannot be completed, when the authorized source set cannot support a phase and the user asks the model to proceed as if it could, when findings would rest on a single uncorroborated source, or when the requested product would exceed the public-person or lawful-recommendation safeguards.

## Human approval gate

The human analyst adjudicates the research design, phase outputs, key judgments, confidence, and collection priorities before the baseline is released, briefed, or reused. The quality-control checklist above is completed as part of this gate.

## Related assets

- `skills/functional/influence-access-analysis/source-tradecraft/`
- `skills/functional/influence-access-analysis/environment-mapping/`
- `skills/functional/influence-access-analysis/actor-network/`
- `skills/functional/influence-access-analysis/critical-node-analysis/`
- `skills/functional/influence-access-analysis/indicators-warning/`
- `skills/functional/influence-access-analysis/commander-reporting/`
- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `templates/intelligence/influence-analysis-profile.md`
- `templates/intelligence/influence-scoring-model.md`
