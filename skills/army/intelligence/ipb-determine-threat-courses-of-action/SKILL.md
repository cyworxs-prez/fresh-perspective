---
name: ipb-determine-threat-courses-of-action
summary: Develop, compare, and monitor plausible threat courses of action for Army IPB and decision support.
version: 0.1
maturity: draft
namespace: army
human_role: analyst-or-planner
references:
  - ATP 2-01.3, Intelligence Preparation of the Battlefield
  - ADP 2-0, Intelligence
---

# IPB: Determine Threat Courses of Action

## Purpose

Assist a human analyst in developing distinguishable, feasible, and evidence-based threat courses of action that support planning, warning, collection, and decision support.

## Preconditions

Use only after the operational environment, environmental effects, and threat model have been confirmed and approved by the human analyst.

## Mandatory interview

Confirm the supported decision, planning horizon, actor objectives, environmental constraints, friendly actions the actor may respond to, number and type of COAs required, warning lead time, and required output format.

## Method

1. Restate actor objectives, capabilities, constraints, dependencies, and environmental effects.
2. Generate a broad but bounded set of plausible COAs.
3. Test each COA for suitability, feasibility, acceptability from the actor's perspective, distinguishability, and consistency with available evidence.
4. Describe each COA's objective, phases, main effort, supporting efforts, timing, decision points, dependencies, signatures, branch points, and potential culmination or failure conditions.
5. Identify the most likely and most dangerous only after comparing all retained COAs.
6. Develop indicators and discriminators that can distinguish among COAs.
7. Identify collection, research, access, processing, exploitation, and warning gaps.
8. Record alternatives, deception concerns, confidence, and assumptions.

## Evidence rules

Do not create a COA merely to complete a doctrinal-looking set. Exclude impossible or unsupported options and explain why. Do not assign likelihood without an explicit evidentiary basis and human approval.

## Output

- retained COA set;
- COA comparison matrix;
- most-likely and most-dangerous rationale;
- event or indicator matrix;
- decision points and branch indicators;
- assumptions, alternatives, confidence, deception concerns, and gaps.

## Quality checks

- COAs are genuinely distinguishable;
- each is feasible within actor capabilities and constraints;
- indicators discriminate rather than merely describe activity;
- environmental effects are integrated;
- friendly-action dependencies are considered;
- most likely is not automatically treated as most dangerous;
- confidence and gaps are explicit.

## Stop conditions

Stop when the threat model, actor objective, planning horizon, or evidence base is insufficient to develop meaningful alternatives. State what additional information is required.

## Human approval gate

The analyst approves the retained COAs, likelihood judgments, warning indicators, and collection implications before use in planning, targeting, collection management, or command briefing.

## Related assets

- `skills/army/intelligence/ipb-evaluate-threat/`
- `skills/shared/intelligence-tradecraft/structured-analytic-techniques/`
- `templates/intelligence/threat-coa-comparison-matrix.md`
- `prompts/army/intelligence/ipb-determine-threat-courses-of-action.md`