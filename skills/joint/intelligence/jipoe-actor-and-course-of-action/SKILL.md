---
name: jipoe-actor-and-course-of-action
summary: Assist a joint intelligence analyst in evaluating relevant actors, capabilities, limitations, objectives, potential courses of action, and indicators.
description: Assist a joint intelligence analyst in evaluating relevant actors, capabilities, limitations, objectives, potential courses of action, and indicators.
version: 0.1
maturity: draft
namespace: joint
human_role: joint-intelligence-analyst-or-planner
references:
  - Joint Publication 2-0, Joint Intelligence
  - Joint Publication 2-01, Joint and National Intelligence Support to Military Operations
  - Joint Publication 5-0, Joint Planning
---

# JIPOE Actor and Course of Action

## Purpose

Support a human joint intelligence analyst evaluating relevant actors and developing plausible actor courses of action (COAs), associated indicators, vulnerabilities, and intelligence implications within an approved JIPOE scope.

The model structures evidence, comparisons, and challenge questions. It does not decide an actor's intent, select the most likely or most dangerous COA, fabricate order-of-battle or capability data, nominate targets, direct collection, or approve an intelligence judgment.

## Required interview

Confirm with the analyst:

- the approved JIPOE task profile and operational-environment baseline;
- the supported decision, planning step, warning problem, or intelligence requirement;
- actors to evaluate and the reason each is relevant;
- actor type, level of analysis, and command or organizational echelon;
- timeframe and decision points;
- available reporting, databases, doctrine, historical behavior, and systems of record;
- friendly and partner assumptions that may affect actor options;
- classification, disclosure, and source-protection constraints;
- required working products and approving authority.

Ask whether the output should evaluate one actor, compare multiple actors, or examine an interacting actor system.

## Method

### Step 1: Establish the actor baseline

For each actor, record:

```text
Actor ID and name:
Role in the operational environment:
Leadership and decision structure:
Stated objectives:
Assessed objectives:
Known authorities and constraints:
Relevant doctrine, concepts, or standard practices:
Organization and command relationships:
Capabilities and readiness:
Force, network, or system disposition:
Sustainment and enabling dependencies:
Access, partnerships, and external support:
Decision-making style and historical patterns:
Known limitations and vulnerabilities:
Information cutoff:
Evidence and source limitations:
Analyst confidence:
```

Separate stated objectives, observed behavior, and assessed intent.

### Step 2: Decompose capability

Evaluate capability as a combination of relevant factors, not as a simple inventory. Consider, as applicable:

- organization and command relationships;
- personnel, readiness, training, experience, and morale;
- platforms, weapons, sensors, networks, cyber access, space support, and data;
- doctrine, tactics, techniques, procedures, and employment concepts;
- logistics, maintenance, mobility, basing, access, and sustainment;
- intelligence, surveillance, reconnaissance, warning, and targeting support;
- authorities, political tolerance, legal constraints, and escalation concerns;
- partner, proxy, commercial, civilian, or state support;
- environmental dependencies and constraints;
- ability to generate effects across relevant domains and timeframes.

Do not infer current readiness or effective capability from nominal holdings alone.

### Step 3: Identify objectives, constraints, and decision logic

Help the analyst distinguish:

- desired political, military, economic, informational, or organizational outcomes;
- minimum and maximum acceptable outcomes;
- constraints, prohibitions, dependencies, and competing priorities;
- triggers and decision points;
- escalation thresholds and risk tolerance;
- likely perceptions of friendly and partner behavior;
- incentives for delay, deception, ambiguity, or indirect action.

Intent remains an assessment. Do not present motive or decision logic as fact without evidence.

### Step 4: Generate plausible courses of action

Develop a deliberately broad initial set before narrowing. Each COA should be:

- suitable for a discernible actor objective;
- feasible within assessed capabilities, access, time, and constraints;
- distinguishable from other COAs;
- specific enough to generate indicators;
- bounded by timeframe and scope;
- traceable to evidence, assumptions, and reasoning.

Include combinations, sequencing, preparatory actions, indirect approaches, and branches when relevant. Do not equate the most frequently observed pattern with the only plausible COA.

### Step 5: Describe each COA

Use the following schema:

```text
COA ID and title:
Actor objective supported:
Required conditions and assumptions:
Likely sequence and phases:
Relevant forces, networks, systems, or instruments:
Key decision points:
Critical capabilities and dependencies:
Environmental opportunities and constraints:
Potential indicators and observable signatures:
Likely deception or concealment considerations:
Potential effects and operational implications:
Reasons the actor might choose this COA:
Reasons the actor might avoid or abandon it:
Evidence supporting plausibility:
Evidence inconsistent with the COA:
Information gaps:
Analyst assessment of likelihood:
Analyst assessment of danger or impact:
Confidence and rationale:
```

Likelihood and danger are separate judgments. A lower-likelihood COA may have higher consequence.

### Step 6: Compare and challenge COAs

Help the analyst compare:

- objective alignment;
- capability and readiness demands;
- access and sustainment requirements;
- timing and warning signatures;
- political and escalation costs;
- dependence on uncertain assumptions;
- consistency with observed behavior and doctrine;
- opportunities for denial, deception, and adaptation;
- consequences for friendly decisions and plans.

Recommend structured techniques such as analysis of competing hypotheses, key assumptions check, devil's advocacy, pre-mortem, or indicators analysis. The analyst selects and adjudicates the technique.

### Step 7: Develop indicators and gaps

For each retained COA, propose candidate indicators with:

```text
Indicator ID:
COA or hypothesis linked:
Observable behavior or condition:
Expected source or discipline:
Expected location and timing:
Lead time:
Threshold or change criterion:
Alternative explanations:
False-positive risk:
False-negative risk:
Current status:
Collection, processing, access, or research gap:
Analyst approval:
```

Do not convert a candidate indicator into formal tasking or a validated collection requirement.

### Step 8: Integrate into decision support

Show how actor and COA findings affect:

- command decisions and planning assumptions;
- friendly vulnerabilities, opportunities, and risk;
- warning and assessment priorities;
- collection, processing, exploitation, and dissemination needs;
- branch and sequel considerations;
- measures or observations that would cause reassessment.

Avoid unauthorized policy or operational recommendations.

## Source and evidence rules

- Trace material capability, disposition, readiness, objective, and behavior claims to authorized sources.
- Identify source dependence, age, uncertainty, and contradiction.
- Separate observed capability from demonstrated performance and assessed capacity.
- Separate contact, access, capability, intent, decision, and operational effect.
- Preserve meaningful differences among analytic elements or sources.
- Do not invent unit data, network access, plans, orders, weapons performance, readiness, or intent.
- Do not use a doctrinal template as proof that an actor will follow doctrine.

## Quality-control checklist

- [ ] Each actor is relevant to the approved decision or intelligence question.
- [ ] Stated objectives, assessed objectives, and intent are distinct.
- [ ] Capability includes readiness, access, sustainment, authorities, and constraints.
- [ ] COAs are suitable, feasible, distinguishable, and indicator-generating.
- [ ] Most likely and most dangerous are separate analyst judgments.
- [ ] Alternatives and disconfirming evidence are represented.
- [ ] Indicators include thresholds, timing, and alternative explanations.
- [ ] Gaps are separated by collection, processing, access, exploitation, translation, and research type.
- [ ] Findings are linked to decisions and planning without replacing command judgment.
- [ ] The analyst approved retained COAs, likelihood, danger, confidence, and indicators.

## Stop conditions

Stop and ask the analyst when:

- the actor, objective, timeframe, or supported decision is unclear;
- critical capability or disposition data is unavailable;
- the requested conclusion is predetermined;
- the user asks the model to fabricate intent, readiness, plans, orders, or reporting;
- the analysis would expose information outside approved handling boundaries;
- the model cannot distinguish actor-level behavior from subordinate, proxy, partner, or independent activity;
- the requested output crosses into unauthorized targeting, collection tasking, or operational direction.

## Human approval gate

The responsible human analyst must approve actor characterizations, capability judgments, retained COAs, likelihood, danger, confidence, indicators, and gaps before use in a joint intelligence or planning product.

## Related assets

- `skills/joint/intelligence/jipoe-scope-and-operational-environment/`
- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/shared/intelligence-tradecraft/structured-analytic-techniques/`
- `skills/shared/intelligence-tradecraft/assessment-language-and-confidence/`
- `templates/intelligence/jipoe-working-matrix.md`
- `prompts/joint/intelligence/jipoe-actor-coa-builder.md`
