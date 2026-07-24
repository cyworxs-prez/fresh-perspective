---
name: actor-relationship-effect-analysis
summary: Identify public actors, organizations, relationships, influence stages, and operational effects without conflating contact with malign influence.
description: Identify public actors, organizations, relationships, influence stages, and operational effects without conflating contact with malign influence.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst
references:
  - ICD 203, Analytic Standards
---

# Actor–Relationship–Effect Analysis

## Purpose

Explain how influence, access, authority, dependence, or leverage may move through political, economic, social, security, commercial, and information systems.

## Required scoping check

Resolve or explicitly assume the area of analysis, area of interest, target actor or comparative posture, local and partner actors, mission or decision, planning horizon, required capabilities, audience, sensitivity, and output format. Ask only for missing information that would materially change the analysis. Never inherit geography, actor, adversary, partner, or mission details from prior outputs.

## Actor categories

Track only actors relevant to decisions, narratives, authorities, or critical systems, including government bodies, diplomatic missions, military and security services, state-owned and private firms, elected officials, political parties, regulators, infrastructure operators, industry associations, universities, think tanks, media, civil society, labor, religious, diaspora, and transnational organizations.

## Relationship coding

Use precise labels such as ownership, financing, contract dependence, regulatory authority, party affiliation, employment, board membership, public advisory role, training, information exchange, commercial partnership, shared policy interest, public advocacy, coercion, substantiated corrupt payment, or mere contact. Never use “influence” as a substitute for the actual mechanism.

## Influence stages

1. Access.
2. Placement.
3. Leverage.
4. Activation.
5. Behavioral effect.
6. Operational or decision effect.

## Named-person standard

For each named individual include only current public role, decision relevance, publicly documented affiliations, public statements or actions, relationship type, evidence grade, and analytic significance. Do not infer loyalty, corruption, intelligence status, or foreign direction without credible evidence.

## Outputs

Produce a node list, edge list, network diagram, brokerage assessment when supported, influence-stage table, gatekeepers, brokers, resilience nodes, and unknown or weakly documented relationships.

## Analytic questions

- Who can approve, constrain, delay, revoke, or facilitate access or action?
- Who controls relevant infrastructure, information, authorities, or financing?
- Which relationships create persistent privileged access or dependency?
- What trigger could activate leverage?
- What observable behavior would demonstrate effect?
- Which alternative explanations remain plausible?

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires mapping who can enable, constrain, or shape access, decisions, or critical systems in an area of analysis. Do not use it to profile private individuals outside a public role, to assert influence without an evidenced mechanism, or as a substitute for counterintelligence, law-enforcement, or security-clearance processes.

## Quality-control checklist

- [ ] Every tracked actor has a documented public role and decision relevance.
- [ ] Every relationship uses a specific mechanism label, not "influence."
- [ ] Influence stages are supported by evidence, not inferred from contact alone.
- [ ] Alternative explanations are recorded for material relationships.
- [ ] Weakly documented relationships are labeled as such, not upgraded.

## Stop conditions

Stop and ask the analyst when the scoping check cannot be completed, when the evidence base for a material relationship is absent and the user asks the model to fill it, when a request would require inferring loyalty, corruption, or foreign direction without credible evidence, or when named-person analysis would exceed the public-role standard.

## Human approval gate

The human analyst adjudicates every node, edge, influence-stage assignment, and brokerage judgment before the network products are used in an assessment or briefed.

## Related assets

- `skills/functional/influence-access-analysis/baseline-assessment/`
- `skills/functional/influence-access-analysis/source-tradecraft/`
- `skills/functional/influence-access-analysis/critical-node-analysis/`
- `templates/intelligence/actor-edge-list.csv`
- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
