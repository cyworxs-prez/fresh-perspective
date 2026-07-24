# Influence, Access, and Freedom-of-Maneuver Analysis Skill Pack

This collection provides reusable analyst skills for country, territory, region, theater, corridor, city, and subnational assessments. It is actor-neutral and can be configured for a state, coalition, non-state network, commercial ecosystem, criminal organization, institutional bloc, or other relevant actor.

**Maturity:** Reference skill collection. Individual assessments remain draft analytic products until reviewed against the user's applicable standards and authorities.

## When to use this collection

Use this collection when the user needs to understand how actors, relationships, systems, investments, dependencies, authorities, and critical nodes may affect decisions, resilience, access, operational options, or freedom of maneuver in a bounded area.

The collection is suitable for:

- baseline country or area assessments;
- comparative actor assessments;
- partner-access and decision-resilience analysis;
- infrastructure and dependency analysis;
- actor-network and influence-pathway analysis;
- indicators-and-warning development;
- commander, executive, policymaker, or planner reporting.

It does not presume an adversary, malign intent, or a military mission.

## Required analysis configuration

Before using any skill, establish an analysis profile. Ask the user for missing elements that materially affect the assessment; otherwise record explicit assumptions and proceed.

- **Area of analysis:** country, territory, region, theater, corridor, city, or other bounded area.
- **Area of interest:** adjacent areas, external systems, and transnational networks that can affect the area of analysis.
- **Target actor or actors:** state, coalition, organization, network, industry grouping, or other actor whose influence, access, capabilities, or dependencies are being assessed.
- **Local or partner actors:** governments, institutions, communities, firms, and networks whose decisions or systems are relevant.
- **Mission or decision context:** the operational, diplomatic, security, economic, policy, humanitarian, commercial, or organizational decision the assessment must support.
- **Planning horizon:** current, near-term, mid-term, long-term, or specified dates.
- **Required access or capability:** permissions, infrastructure, logistics, communications, data, financing, public support, authorities, or other conditions.
- **Audience and format:** commander, executive, policymaker, analyst, planner, investigator, program manager, or other consumer.
- **Constraints:** classification, data sensitivity, legal boundaries, available sources, time, and geographic exclusions.

Do not assume an adversary, partner, mission, geography, audience, or desired conclusion from prior work. If the user does not identify a target actor, ask whether the assessment should be actor-specific, comparative, or actor-agnostic.

## Skills

- `baseline-assessment`: master workflow, scoping, integration, structured analysis, and quality controls.
- `source-tradecraft`: source validation, claim decomposition, corroboration, and evidence ledger.
- `environment-mapping`: PMESII-PT, ASCOPE, JIPOE, and environmental baseline analysis.
- `actor-network`: public actor, institution, firm, and relationship mapping.
- `critical-node-analysis`: physical, logical, institutional, financial, commercial, digital, and temporal nodes.
- `indicators-warning`: indicators, warning thresholds, PIRs, EEIs, and collection matrices.
- `commander-reporting`: concise, visual, decision-oriented reporting for commander or executive audiences.

## Recommended sequence

1. Establish and record the analysis profile.
2. Run `source-tradecraft` to create the evidence and claim ledger.
3. Run `environment-mapping` to establish the area baseline.
4. Run `actor-network` and `critical-node-analysis` in parallel when sources permit.
5. Run `indicators-warning` after major pathways, vulnerabilities, and decision points are identified.
6. Use `baseline-assessment` to integrate, score, challenge, and adjudicate findings.
7. Use `commander-reporting` to create the final decision-support product.
8. Conduct a final review for evidence, confidence, alternative explanations, unsupported labels, source freshness, and decision relevance.

## Day-to-day analyst use

A practical operating rhythm is:

1. Create a working folder or case workspace for the assessment.
2. Copy the analysis-profile template (`templates/intelligence/influence-analysis-profile.md` at the repository root) and complete it with the user.
3. Open the claim ledger before collecting evidence.
4. Add claims, sources, dates, reliability, credibility, and corroboration as research progresses.
5. Maintain the environmental, actor, node, and indicator artifacts as separate working products.
6. Record assumptions and collection gaps as they emerge rather than waiting for the final report.
7. Re-run the integration step when a major source, actor, node, or scenario changes.
8. Produce a concise decision-oriented report and retain the supporting ledgers for audit and updates.

For recurring monitoring, pair this skill collection with an approved workflow and automation. The automation should identify which skill version, source windows, indicators, thresholds, and review gates it uses.

## Templates

The collection's working templates live centrally under `templates/intelligence/` at the repository root: `influence-analysis-profile.md`, `influence-claim-ledger.csv`, `influence-scoring-model.md`, `actor-edge-list.csv`, `critical-node-register.csv`, and `indicator-register.csv`.

## Expected working artifacts

The collection should normally produce:

- analysis profile;
- source and claim ledger;
- environmental baseline matrix;
- actor and relationship map;
- critical-node register;
- influence, dependency, or effect pathways;
- alternative hypotheses;
- indicators and warning matrix;
- collection gaps and requirements;
- key judgments with confidence;
- decision, risk, or response matrix;
- final commander or executive report.

## Core principles

- Evaluate observable relationships, activities, systems, investments, dependencies, and authorities before assigning intent.
- Separate legitimate engagement, structural dependence, competitive influence, coercion, corruption, deception, and hostile activity.
- Use terms such as malign, coercive, deceptive, corrupt, captured, compromised, or hostile only when supported by evidence and clearly defined criteria.
- Distinguish documented fact from analytic inference and assumption.
- Include alternative explanations and evidence that would change the judgment.
- Tie findings to a decision, access requirement, capability, vulnerability, resilience measure, or collection need.
- Do not substitute scoring for analytic reasoning; scores organize judgments but do not prove them.