---
name: pmesii-ascope-jipoe-mapping
summary: Map an operational or policy environment using PMESII-PT, ASCOPE, and a concise JIPOE overlay.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst-or-planner
references:
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - Joint Publication 2-01.3, Joint Intelligence Preparation of the Operational Environment
---

# PMESII-PT × ASCOPE × JIPOE Mapping

## Purpose

Build the environmental baseline for an area influence, access, resilience, or freedom-of-maneuver assessment.

## Required scoping check

Resolve or explicitly assume the area of analysis, area of interest, target actor or comparative posture, local and partner actors, mission or decision, planning horizon, required capabilities, audience, sensitivity, and output format. Ask only for missing information that would materially change the analysis. Never inherit geography, actor, adversary, partner, or mission details from prior outputs.

## PMESII-PT dimensions

Assess political, military, economic, social, information, infrastructure, physical-environment, and time dimensions.

## ASCOPE dimensions

For each relevant PMESII-PT dimension identify areas, structures, capabilities, organizations, people, and events.

## Required analytic deduction

Every material entry should support a statement of the form:

**Because actor X can influence organization Y, which controls capability Z at location or system A, the relevant actor may be able to create condition B during event or decision window C, affecting requirement or decision D.**

Do not populate the matrix with descriptive facts that have no decision or operational relevance.

## JIPOE overlay

Include:

- Area of operations and area of interest.
- Political and legal decision architecture.
- Key systems, subsystems, and dependencies.
- Critical terrain, infrastructure, and information nodes.
- Centers of gravity and critical capabilities, requirements, and vulnerabilities.
- Most likely and most dangerous relevant-actor courses of action.
- Event templates, named areas of interest, and decision windows.
- PIRs, EEIs, indicators, and collection opportunities.

## Actor-neutral source categories

Include local and partner institutions, target-actor state and affiliated bodies, commercial entities, civil society, academia, media, security organizations, transnational networks, and relevant external actors.

## Output

Produce:

- PMESII-PT narrative baseline.
- PMESII-PT × ASCOPE matrix.
- System and dependency map.
- Critical-factor assessment.
- Temporal decision-window timeline.
- JIPOE deductions tied to commander, executive, or policy decisions.

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires an environmental baseline for an influence, access, resilience, or freedom-of-maneuver assessment. Do not use it as a substitute for command-approved JIPOE or IPB products, formal geospatial or weather support, or the Joint and Army skills that implement those doctrinal processes under their own namespaces.

## Quality-control checklist

- [ ] Every matrix entry supports the required analytic deduction, not description alone.
- [ ] Dimensions irrelevant to the decision are omitted with rationale rather than padded.
- [ ] Sources, dates, and information cutoff are recorded for material entries.
- [ ] Deductions separate environmental conditions from actor-dependent effects.
- [ ] Gaps are stated where a dimension could not be assessed from authorized sources.

## Stop conditions

Stop and ask the analyst when the scoping check cannot be completed, when authorized sources cannot support a required dimension and the user asks the model to fill it, or when the mapping is being used to justify conclusions the evidence does not support.

## Human approval gate

The human analyst approves the baseline, matrix, and deductions before they feed pathway analysis, node analysis, indicators, or reporting.

## Related assets

- `skills/functional/influence-access-analysis/baseline-assessment/`
- `skills/functional/influence-access-analysis/critical-node-analysis/`
- `skills/joint/intelligence/jipoe-scope-and-operational-environment/`
- `skills/army/intelligence/ipb-define-operational-environment/`
