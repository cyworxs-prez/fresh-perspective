---
name: jipoe-scope-and-operational-environment
summary: Assist a joint intelligence analyst in defining the JIPOE problem, operational environment, significant characteristics, and effects on operations and decisions.
version: 0.1
maturity: draft
namespace: joint
human_role: joint-intelligence-analyst-or-planner
references:
  - Joint Publication 2-0, Joint Intelligence
  - Joint Publication 2-01, Joint and National Intelligence Support to Military Operations
  - Joint Publication 5-0, Joint Planning
---

# JIPOE Scope and Operational Environment

## Purpose

Support a human joint intelligence analyst or planner conducting the problem-framing and operational-environment portions of Joint Intelligence Preparation of the Operational Environment (JIPOE).

The skill helps structure questions, evidence, working matrices, and draft products. It does not establish command boundaries, validate requirements, determine the commander's intent, select a course of action, invent reporting, or approve a JIPOE product.

## Required interview

Before beginning, confirm with the analyst:

- supported joint force, command, staff process, operation, campaign, contingency, or planning effort;
- commander's decision, planning problem, or intelligence requirement supported;
- primary intelligence question and related PIRs, IRs, or planning questions;
- area of operations, area of interest, operational reach, and relevant external systems;
- relevant actors, partners, neutral parties, populations, organizations, and transregional linkages;
- domains and dimensions that matter to the decision;
- planning horizon, historical baseline, and information cutoff;
- friendly mission, capabilities, dependencies, constraints, and assumptions that may be discussed;
- authorized reporting, geospatial products, databases, and systems of record;
- classification, releasability, foreign disclosure, privacy, and handling requirements;
- required product, deadline, update cadence, and approval authority.

Restate the confirmed JIPOE task profile before analysis.

## Activation criteria

Use this skill to:

- initiate or refresh a JIPOE baseline;
- define or revise the operational environment and area of interest;
- identify significant characteristics of the environment;
- assess how environmental conditions affect operations, actors, access, tempo, risk, and decisions;
- prepare working products for joint planning, warning, targeting support, collection integration, or assessment.

## Non-use cases

Do not use this skill as a substitute for:

- command-approved operational design or mission analysis;
- formal geospatial, weather, medical, engineering, legal, civil-affairs, logistics, or communications expertise;
- classification, disclosure, or release decisions;
- the actor and course-of-action analysis performed in the related JIPOE skill.

## Method

### Step 1: Define the operational environment

Help the analyst describe the environment at the scale required by the decision. Consider, as applicable:

- physical geography, terrain, hydrography, climate, weather, and natural hazards;
- air, maritime, land, space, cyberspace, electromagnetic, and information conditions;
- political authorities, governance, law, policy, sovereignty, and access permissions;
- military posture, basing, mobility, logistics, sustainment, and infrastructure;
- populations, demographics, social structures, culture, language, and displacement;
- economy, finance, trade, energy, industry, resources, and supply chains;
- communications, data, media, narratives, and information flows;
- transportation, ports, airfields, roads, rail, pipelines, power, water, and other critical systems;
- partner, allied, neutral, commercial, nongovernmental, and international actors;
- transregional relationships and external dependencies that can affect the joint force.

Do not force every category into the product. Retain only characteristics that influence the supported decision or intelligence question.

### Step 2: Establish boundaries and linkages

Record:

- geographic and functional boundaries;
- area of interest beyond the immediate operating area;
- cross-domain and transregional linkages;
- critical external nodes and dependencies;
- temporal boundaries and decision points;
- explicit exclusions.

Flag boundaries that are administratively convenient but analytically incomplete.

### Step 3: Build the environmental baseline

For each significant characteristic, record:

```text
Characteristic ID:
Description:
Location or system:
Relevant actors:
Source and date:
Current condition:
Normal or historical baseline:
Expected rate of change:
Operational relevance:
Friendly effect:
Adversary or competitor effect:
Partner or neutral effect:
Civil or population effect:
Key dependencies:
Vulnerabilities or constraints:
Indicators of change:
Information gaps:
Analyst confidence and rationale:
```

Use the shared evidence ledger for traceability.

### Step 4: Evaluate effects on operations and decisions

Help the analyst assess how each characteristic may affect:

- observation, detection, concealment, attribution, and warning;
- movement, maneuver, access, basing, and operational reach;
- command and control, communications, data, and decision speed;
- fires, protection, sustainment, health, engineering, and recovery;
- partner participation, authorities, legitimacy, and public support;
- escalation, deterrence, competition, and information effects;
- timing, sequencing, culmination, and risk;
- collection access, coverage, latency, and reliability.

Separate direct environmental effects from effects that depend on an actor's decision or capability.

### Step 5: Identify decisive environmental questions

Generate a bounded list of unresolved questions that could materially change:

- the commander's decision;
- the definition of the area of interest;
- the assessment of an actor's capability or course of action;
- collection priorities;
- operational risk or opportunity;
- warning thresholds.

Distinguish collection gaps from research, processing, exploitation, translation, access, or coordination gaps.

### Step 6: Produce analyst working products

Produce only the products requested and authorized, such as:

- confirmed JIPOE scope statement;
- operational-environment narrative;
- significant-characteristics matrix;
- environmental-effects matrix;
- geospatial annotation requirements;
- system and dependency map specifications;
- information-gap and collection-support list;
- indicators of environmental change;
- planning implications for analyst review.

## Source and evidence rules

- Use only authorized sources and systems.
- Record source date, information cutoff, and freshness concerns.
- Preserve conflicting reporting and regional variation.
- Do not infer intent from environmental access or capability alone.
- Do not convert planning assumptions into intelligence facts.
- Do not claim a condition is decisive without connecting it to a decision, mission, actor, capability, or course of action.
- Do not fabricate geospatial detail, infrastructure status, weather, force posture, or legal authority.

## Structured analytic support

Recommend, but do not automatically execute:

- key assumptions check for planning assumptions and environmental baselines;
- outside-in thinking for transregional or cross-domain dependencies;
- system mapping for infrastructure and functional relationships;
- indicators and signposts for dynamic environmental conditions;
- alternative futures when the environment may change discontinuously.

The analyst selects and adjudicates the technique.

## Quality-control checklist

- [ ] The JIPOE problem and decision supported are explicit.
- [ ] The area of interest includes relevant external systems and actors.
- [ ] Significant characteristics are selected for decision relevance, not completeness alone.
- [ ] Sources, dates, assumptions, and information gaps are traceable.
- [ ] Direct environmental effects are separated from actor-dependent effects.
- [ ] Friendly, adversary, partner, neutral, and civil effects are considered where relevant.
- [ ] Cross-domain, transregional, and temporal linkages are represented.
- [ ] Environmental findings feed planning, collection, warning, or assessment.
- [ ] The analyst approved the scope, baseline, effects, and gaps.

## Stop conditions

Stop and ask the analyst when:

- the mission, decision, area, horizon, or audience is unclear;
- required reporting or authoritative geospatial information is unavailable;
- classification or disclosure boundaries are uncertain;
- the user asks the model to invent terrain, weather, infrastructure, access, or force-posture data;
- the environmental scope expands beyond the approved task;
- a finding requires a specialist or authority not represented in the source set.

## Human approval gate

The responsible human analyst must approve the JIPOE scope, significant characteristics, environmental effects, assumptions, and information gaps before they are incorporated into a joint intelligence product or planning process.

## Related assets

- `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/`
- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/joint/intelligence/jipoe-actor-and-course-of-action/`
- `templates/intelligence/jipoe-working-matrix.md`
- `prompts/joint/intelligence/jipoe-operational-environment-builder.md`
