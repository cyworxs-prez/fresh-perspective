---
name: homeland-strategic-warning
summary: Build a whole-of-government U.S. Homeland indicators-and-warning assessment by correlating atypical civilian, regulatory, commercial, infrastructure, and security observations into decision-linked strategic warning.
version: 1.0
maturity: draft
namespace: functional
human_role: analyst-or-planner
references:
  - ICD 203, Analytic Standards
  - Joint Publication 2-0, Joint Intelligence
---

# Homeland Strategic Warning

## Purpose

Develop a lawful, auditable, whole-of-government warning assessment for changes inside the United States that may indicate a foreign actor is preparing for crisis, conflict, coercion, sabotage, prepositioning, economic warfare, or strategic disruption.

This skill is designed for environments where relevant observations are distributed across federal civilian agencies, regulators, Sector Risk Management Agencies, state and local governments, law-enforcement organizations, private-sector operators, and non-IC departments that do not possess traditional intelligence collection or analytic missions.

The skill must distinguish:

1. **Visibility**: data, transactions, traffic, filings, inspections, incidents, or operational activity an organization can lawfully observe.
2. **Authority**: whether the organization may collect, retain, analyze, correlate, or share the information for warning purposes.
3. **Capacity**: whether it has trained analysts, technical systems, baselines, data science, liaison officers, or reporting processes.
4. **Responsibility**: whether it owns the decision, mitigation, referral, investigation, regulation, or warning function.
5. **Intelligence value**: whether the observation becomes diagnostic only when combined with other domains.

## Mandatory scoping interview

Before analysis, query the user for any missing parameter that would materially change the assessment. Do not silently inherit country, adversary, scenario, agency, authority, or planning assumptions from prior work.

Ask concise questions covering:

- **Target actor or hazard**: state, proxy, criminal network, cyber actor, supply-chain threat, or actor-agnostic warning problem.
- **Conflict or crisis scenario**: invasion, blockade, coercive campaign, cyber disruption, sabotage, economic warfare, mobilization, gray-zone escalation, or unspecified.
- **Area of analysis**: entire U.S. Homeland, specific region, sector, corridor, installation area, state, territory, or metropolitan area.
- **Area of interest**: foreign jurisdictions, maritime approaches, border zones, global supply chains, or transnational networks affecting the Homeland.
- **Decision supported**: strategic warning, force protection, continuity, sector defense, mobilization, law enforcement, economic security, emergency management, or policymaker awareness.
- **Audience**: Cabinet, National Security Council, DOW, IC, DHS, CISA, FBI, SRMA, governor, fusion center, sector executive, or mixed audience.
- **Planning horizon**: immediate, 0-30 days, 1-6 months, 6-24 months, or specified dates.
- **Required warning lead time**: hours, days, weeks, months, or unknown.
- **Relevant entities**: named departments, agencies, regulators, states, sectors, private operators, or data holders.
- **Data restrictions**: unclassified only, law-enforcement sensitive, CUI, proprietary, privacy-limited, classified, or unknown.
- **Output**: framework, dashboard, PIR/EEI matrix, agency playbook, warning note, executive report, collection plan, or skill/workflow.

### Clarification rule

- Ask only for missing information that affects the analysis.
- If the user cannot supply an item, state the assumption and its effect on confidence.
- Do not proceed with a named actor-specific warning assessment until the actor and scenario are confirmed.
- If the request is for a reusable framework, keep it actor-neutral unless the user explicitly requests otherwise.

## Core analytic question

> What lawful observations available to U.S. Homeland organizations, when correlated across domains and compared against baseline behavior, would provide early and diagnostic warning of a shift from competition or routine activity toward preparation for crisis or conflict?

## Analytic architecture

Use the chain:

**Strategic objective → preparatory requirement → observable Homeland behavior → data holder → legal authority → analytic gap → corroborating domains → warning threshold → decision → response**

Every major judgment must identify:

- the preparatory requirement being inferred;
- the observable behavior;
- who can see it;
- why it is unusual relative to baseline;
- alternative explanations;
- what corroboration is required;
- the warning lead time;
- the decision it supports;
- confidence and severity separately.

## Indicator families

At minimum assess:

- International trade, customs, export licensing, and re-export behavior.
- Shipping, ports, freight, rail, aviation, warehousing, and logistics.
- Energy, fuel, grid, pipelines, generation, and industrial demand.
- Financial flows, insurance, securities, credit, capital movement, and beneficial ownership.
- Critical minerals, chemicals, machine tools, electronics, and defense-adjacent supply chains.
- Telecommunications, cloud, data centers, subsea cables, satellite services, and spectrum.
- Cyber activity, vulnerability exploitation, access persistence, and operational technology anomalies.
- Agriculture, food, fertilizer, veterinary, and commodity markets.
- Pharmaceuticals, medical supply chains, public health, and laboratory demand.
- Federal procurement, industrial-base orders, unusual subcontracting, and capacity reservation.
- Research, universities, laboratories, patents, technology transfer, and scientific personnel activity.
- Immigration, travel, visas, charter movements, and unusual personnel patterns.
- Diplomatic, consular, legal, lobbying, media, and influence activity.
- Law-enforcement, transnational crime, sanctions evasion, and illicit finance.
- State, local, tribal, territorial, and private-sector operational anomalies.

## Indicator design standard

Each indicator must include:

- title;
- preparatory requirement supported;
- observable event or condition;
- baseline and expected variance;
- data owner or lawful observer;
- collection or visibility authority;
- retention, privacy, classification, and disclosure constraints;
- frequency and latency;
- threshold;
- lead time;
- diagnosticity;
- false-positive risks;
- alternative explanations;
- corroborating indicators;
- warning level impact;
- decision supported;
- reporting recipient;
- confidence effect if confirmed or disproved.

## Warning levels

- **Level 0 — Baseline:** routine competition, normal commercial activity, or isolated anomalies.
- **Level 1 — Shaping:** increased access, influence, reconnaissance, dependency, or option creation.
- **Level 2 — Preparation:** multiple preparatory requirements show unusual, sustained activity.
- **Level 3 — Activation:** convergent indicators show systems, personnel, finance, logistics, or access being readied for use.
- **Level 4 — Imminent / Underway:** actions are difficult to explain except as immediate crisis or conflict preparation, or disruptive activity has begun.

Never raise a warning level from a single non-diagnostic indicator unless the indicator is independently decisive.

## Convergence test

Assess convergence across:

- number of independent domains;
- independence of sources;
- temporal synchronization;
- geographic alignment;
- linkage to a plausible preparatory requirement;
- departure from historical baseline;
- degree of reversibility;
- adversary cost or operational sacrifice;
- consistency with military and foreign indicators;
- absence of a more likely benign explanation.

## Agency visibility-authority-capacity matrix

For every relevant entity record:

- mission and statutory role;
- data or operational visibility;
- specific systems or record types;
- authority to collect;
- authority to analyze for secondary purpose;
- authority to share and with whom;
- privacy, proprietary, tax, health, grand-jury, law-enforcement, or classification restrictions;
- analytic workforce and occupational series;
- data-science and anomaly-detection capability;
- classification access;
- liaison mechanisms;
- reporting channel;
- current gaps;
- recommended bridge mechanism.

Do not characterize absence of intelligence authority as failure. Many organizations were not created or funded to perform strategic warning.

## Occupational and organizational capacity review

Identify whether relevant organizations possess or require:

- 0132 Intelligence Series personnel;
- 0301 or 0343 program and management analysts;
- 1801 investigative or compliance personnel;
- 1811 criminal investigators;
- 2210 IT and cybersecurity personnel;
- economists, statisticians, operations researchers, data scientists, scientists, engineers, contracting officers, trade specialists, inspectors, and emergency managers;
- intelligence liaison officers, embedded analysts, fusion-cell representatives, or cleared detailees.

Assess titles, grade structure, clearance eligibility, supervision, analytic standards, dissemination authority, training, and career paths.

## Whole-of-government collaboration design

Prefer a federated model over indiscriminate centralization.

The architecture should include:

1. Agency-owned data and mission authorities remain with the originating organization.
2. Common indicator taxonomy and metadata standard.
3. Privacy-preserving anomaly reporting where raw data cannot be shared.
4. Trusted liaison and referral channels to IC, DOW, DHS, FBI, CISA, Treasury, Commerce, and sector leads.
5. Cross-domain fusion at an authorized node.
6. Feedback to originating organizations on intelligence value.
7. Human review before escalation or operational action.
8. Audit logs, minimization, access controls, and periodic legal review.

Possible bridge mechanisms include:

- interagency working groups;
- National Security Memorandum or executive direction;
- formal information-sharing agreements;
- detailees and embedded analysts;
- fusion-center or task-force participation;
- SRMA coordination;
- National Labs and FFRDC support;
- common data standards and APIs;
- anonymized or aggregated reporting;
- classified tear-line feedback;
- statutory amendment or appropriations language when existing authorities are insufficient.

## PIR and EEI construction

PIRs must be decision-linked, time-bounded, answerable, and behavior-specific.

Example:

**PIR:** Is the target actor shifting from routine economic competition to coordinated preparation for conflict that could affect U.S. Homeland continuity within the next six months?

**EEIs:**

- unusual export-license applications or denials;
- changes in vessel routing, ownership, insurance, or cargo composition;
- strategic commodity accumulation or withdrawal;
- anomalous capital movement or beneficial-ownership changes;
- cyber access persistence in critical infrastructure;
- concentration of medical, food, fuel, or industrial orders;
- unusual personnel travel, chartering, or consular activity;
- synchronized legal, diplomatic, media, and influence preparation;
- unexplained outages, delays, contract invocation, or supplier nonperformance.

## Required outputs

Produce as requested:

- executive warning judgment;
- scope and assumptions;
- scenario and preparatory-requirement model;
- atypical indicator matrix;
- agency visibility-authority-capacity matrix;
- convergence and warning-level assessment;
- PIRs, EEIs, and collection requirements;
- gaps, shortfalls, and legal constraints;
- collaboration architecture;
- decision thresholds and reporting routes;
- alternative hypotheses;
- confidence statement;
- recommendations with responsible owner and timeframe.

## Analytic guardrails

- Do not request or recommend unlawful collection.
- Do not imply that civilian administrative data should be repurposed without legal review.
- Do not treat nationality, ethnicity, political belief, or protected activity as an indicator.
- Do not equate commercial activity with hostile intent absent diagnostic evidence.
- Do not expose sensitive infrastructure details unnecessarily.
- Use aggregate or anonymized data where possible.
- Separate regulatory, investigative, intelligence, and operational authorities.
- State when a proposed collaboration mechanism requires new statutory, regulatory, policy, budget, clearance, or technical authority.
- Preserve source provenance and prevent circular corroboration.
- Separate fact, inference, assumption, severity, probability, and confidence.

## Quality-control checklist

Before finalizing, confirm that:

- all material scope parameters were resolved or explicitly assumed;
- each indicator maps to a preparatory requirement and decision;
- every data source has a lawful observer and authority assessment;
- benign explanations were tested;
- warning depends on convergence, not volume alone;
- agency limitations are accurately described;
- privacy and civil-liberties constraints are addressed;
- the product identifies the fusion and reporting owner;
- confidence and severity are separate;
- the user can see which missing information would most change the judgment.

## Activation criteria and non-use cases

Use this skill when a confirmed task profile requires strategic warning built from lawful observations distributed across U.S. Homeland civilian, regulatory, commercial, and security organizations. Do not use it for foreign-theater warning problems better served by the joint or influence-access skills, for law-enforcement investigative decisions, for authorities determinations that require counsel, or to justify collection or data repurposing that has not had legal review.

## Stop conditions

Stop and ask the analyst when the scoping interview cannot resolve actor, scenario, or decision supported; when a warning-level change is requested from a single non-diagnostic indicator; when required data is legally restricted and the user asks the model to proceed as if it were available; or when a proposed collaboration mechanism requires authority the assessment cannot establish.

## Human approval gate

The responsible analyst and the organization's review chain adjudicate every warning level, indicator, agency characterization, and recommendation before the assessment is briefed, disseminated, or used to initiate referral, escalation, or operational action. The quality-control checklist above is completed as part of this gate.

## Related assets

- `skills/functional/influence-access-analysis/indicators-warning/`
- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `templates/intelligence/indicator-register.csv`
- `prompts/functional/research-analysis/all-source/10-indicators-warning.md`
