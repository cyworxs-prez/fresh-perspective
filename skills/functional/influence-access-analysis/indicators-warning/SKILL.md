---
name: influence-indicators-warning
summary: Develop decision-linked indicators, warning thresholds, PIRs, SIRs, and collection requirements for influence, access, dependency, and resilience risks.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst-or-planner
references:
  - Joint Publication 2-01.3, Joint Intelligence Preparation of the Operational Environment
  - ICD 203, Analytic Standards
---

# Influence Indicators and Warning

## Purpose

Detect activation of influence, access, leverage, dependency, or coercion before it causes access denial, decision delay, sustainment disruption, intelligence compromise, coalition friction, or loss of resilience.

## Required scoping check

Resolve or explicitly assume the area of analysis, area of interest, target actor or comparative posture, local and partner actors, mission or decision, planning horizon, required capabilities, audience, sensitivity, and output format. Ask only for missing information that would materially change the analysis. Never inherit geography, actor, adversary, partner, or mission details from prior outputs.

## Organizing principle

Build indicators around decisions, branches, thresholds, and operational or policy consequences—not generic activity by the target actor.

## Indicator families

- Access and permission.
- Operational security and intelligence exposure.
- Coalition or stakeholder cohesion.
- Sustainment, finance, contracting, and logistics.
- Information environment and public legitimacy.
- Infrastructure availability and technical dependency.
- Legal, regulatory, and bureaucratic friction.

## Indicator design

Each indicator must include the decision supported, observable event, baseline, threshold, lead time, source, collection frequency, false-positive risks, alternative explanations, and required response.

## Warning levels

- **Green:** baseline activity; no material effect evident.
- **Amber:** preparatory activity, rising leverage, or increasing friction; consequence plausible.
- **Red:** activation or behavioral effect evident; consequence likely or underway.

## PIR construction

A PIR must be tied to a decision, answerable, time-bounded, behavior- or condition-specific, and supported by EEIs and collection opportunities.

Example:

**PIR:** Will relevant authorities approve required contingency access within the decision timeline?

**EEIs:** agenda changes; ministry guidance; local permit status; operator readiness; public messaging; target-actor diplomatic or commercial activity; legal challenges; unusual contract or regulatory action.

## Collection matrix

For each PIR include EEI, indicator, source or sensor, collection owner, frequency, reporting threshold, confidence impact, and gap if unanswered.

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires decision-linked indicators and warning for influence, access, dependency, or resilience risks. Do not use it as a substitute for a command's formal collection-management or requirements-validation process, or for the Homeland-specific warning skill when the problem is U.S. domestic whole-of-government warning.

## Quality-control checklist

- [ ] Every indicator ties to a decision and a consequence, not generic activity.
- [ ] Baselines, thresholds, and lead times are stated, not implied.
- [ ] False-positive risks and alternative explanations are recorded per indicator.
- [ ] Warning-level changes require the stated threshold, not analyst impression.
- [ ] Collection gaps are visible for unanswerable PIRs.

## Stop conditions

Stop and ask the analyst when the scoping check cannot be completed, when the supported decision cannot be identified, when a warning level is requested without threshold evidence, or when the user asks the model to fabricate baseline or collection data.

## Human approval gate

The human analyst approves indicators, thresholds, warning levels, PIRs, EEIs, and the collection matrix before they are briefed, disseminated, or used to task collection through authorized channels.

## Related assets

- `skills/functional/influence-access-analysis/baseline-assessment/`
- `skills/functional/homeland-indicators-warning/homeland-strategic-warning/`
- `templates/intelligence/indicator-register.csv`
- `prompts/functional/research-analysis/all-source/10-indicators-warning.md`
