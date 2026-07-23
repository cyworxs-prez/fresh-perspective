# PRC All-Source Prompt Library

## Problem Decomposition

**Purpose:** Turn a broad requirement into researchable questions

```text
You are an analytic research assistant. Decompose the following decision-support requirement into a structured research plan.

DECISION: [decision and decision-maker]
SCOPE: [country/region/sector/organization], [time period]
REQUIRED OUTCOME OR ACCESS: [what must remain possible]
PRC ACTIVITY OF CONCERN: [initial description]

Use the analytic chain: objective → DIMEFIL instrument → implementing actor → intermediary/access vector → PMESII-PT system → ASCOPE node → observable activity → behavioral effect → operational/policy consequence → decision.

Output:
1. 5-10 priority intelligence questions
2. Atomic sub-questions
3. Variables and indicators
4. Priority source classes
5. Likely alternative explanations
6. Key assumptions
7. A collection sequence

Do not answer the questions or invent evidence.
```

## Search Strategy Generator

**Purpose:** Create multilingual and source-specific search strings

```text
Using the research question below, generate a source-discovery plan. Do not claim that sources exist.

QUESTION: [question]
ENTITIES: [names and known aliases]
GEOGRAPHY/LANGUAGES: [locations and languages]
TIME: [period]

Produce search strings for:
- Official PRC sources
- Host-nation government records
- Corporate registries and filings
- Procurement/contracts
- Court and regulatory records
- Local-language media
- Academic/technical sources
- Archived web content

Include Chinese-name variants, transliterations, abbreviations, and Boolean combinations. Explain what each search is intended to prove or disprove.
```

## Source Extraction

**Purpose:** Extract claims from supplied documents without adding facts

```text
Use only the supplied documents. Extract an evidence ledger with one row per atomic claim: claim, exact quotation or close paraphrase, source title, date, page/section, actor, action, target, DIMEFIL code, PMESII-PT code, ASCOPE node, and analyst relevance.

Mark ambiguous or missing fields as UNKNOWN. Identify duplicate or derivative reporting. Do not infer intent or effect in this step.
```

## Ownership and Finance Mapping

**Purpose:** Reconstruct corporate and financial relationships

```text
Using only the supplied filings and records, map the ownership and financing chain for [asset/company/project].

Distinguish:
- Legal owner
- Ultimate beneficial owner
- Creditor
- Guarantor
- Operator
- Maintainer
- Data controller
- Concession holder
- Government sponsor

For every relationship, cite the exact document and date. List unresolved entities and the records needed to resolve them. Do not infer state control from nationality alone.
```

## Investment Strategic-Optionality Assessment

**Purpose:** Assess leverage without presuming malign intent

```text
Assess [project/investment] using the following tests:
- Ownership/control rights
- Financing and collateral
- Contract and concession rights
- Technical/data access
- Maintenance and vendor lock-in
- Political and employment dependencies
- Dual-use utility
- Substitutability and resilience
- Activation triggers
- Observed use during disputes

Separate verified facts, reasonable inferences, assumptions, and unknowns. Provide benign, commercial, host-nation, and strategic-leverage hypotheses and identify diagnostic evidence for each.
```

## DIMEFIL Synchronization

**Purpose:** Identify whether separate activities form a campaign

```text
Given the supplied event list, code each event by DIMEFIL instrument, actor, target, location, and outcome. Then test for common objective, sequencing, reinforcement, activation, adaptation, and shared intermediaries.

Output:
1. Event table
2. Candidate campaign lines
3. Evidence supporting coordination
4. Evidence against coordination
5. Alternative explanations
6. Confidence

Do not equate temporal proximity with coordination.
```

## PMESII-PT × ASCOPE Matrix

**Purpose:** Build a critical-node environment map

```text
For [geography/sector], populate a PMESII-PT × ASCOPE matrix using only supplied evidence.

For each relevant cell identify:
- Node
- Function
- Owner/operator/regulator
- PRC pathway
- Dependency or vulnerability
- Resilience/substitute
- Possible effect
- Collection gap

Prioritize nodes that affect [decision/access requirement]. Mark empty cells rather than inventing content.
```

## Network Analysis

**Purpose:** Identify brokers, clusters, and leverage pathways

```text
Create an analytic network from the supplied entity and relationship data.

Classify nodes as:
- PRC party-state
- Security
- SOE/policy finance
- Commercial/technical
- Host-nation government
- Business elite
- Media/academic/civic
- Transnational

Classify edges as ownership, finance, contract, political, information, security, legal, family, or other.

Identify central nodes, brokers, chokepoints, clusters, and single-source claims. Explain which paths could plausibly transmit influence or leverage and what evidence is still required.
```

## ACH Matrix

**Purpose:** Test competing explanations

```text
Evaluate these hypotheses about [activity]:
- H1 strategic leverage
- H2 commercial opportunity
- H3 host-nation initiative
- H4 mixed motives/emergent leverage
- H5 misattribution

Use only supplied evidence. Create an ACH matrix rating each item as highly consistent, consistent, neutral, inconsistent, or highly inconsistent with each hypothesis.

Weight evidence by diagnosticity, reliability, independence, and deception risk. Identify the least inconsistent hypothesis and the evidence most likely to change the result.
```

## Indicators and Warning

**Purpose:** Develop observable triggers tied to decisions

```text
For the forecasted outcome [outcome], develop indicators across political, diplomatic, information, military/security, economic, financial, intelligence/data, legal, infrastructure, coalition, and temporal dimensions.

Each indicator must include:
- Baseline
- Observable change
- Threshold
- Expected sequence
- Lead time
- Source
- Alternative explanation
- Diagnostic value
- Decision/action triggered

Separate leading, coincident, and lagging indicators.
```

## Confidence Calibration

**Purpose:** Draft a defensible confidence statement

```text
Review the supplied evidence and draft a confidence assessment for this judgment: [judgment].

Evaluate source quality, independence, consistency, recency, directness, gaps, deception risk, and sensitivity to assumptions.

State:
- What the evidence proves
- What it only suggests
- The strongest contradiction
- What new information would raise or lower confidence

Do not change the substantive judgment unless the evidence does not support it.
```

## Executive Judgment Drafting

**Purpose:** Convert analysis into concise decision support

```text
Draft three versions of a key judgment for [audience]: 35 words, 75 words, and 150 words.

Each version must identify actor, mechanism, target, effect, decision consequence, and confidence. Avoid unsupported intent, vague terms such as “influence,” and deterministic predictions.

Then provide:
- One bottom-line sentence
- Three priority findings with operational/policy implications
```

## Red-Team Critique

**Purpose:** Find analytic weaknesses before publication

```text
Act as an adversarial analytic reviewer. Examine the draft for:
- Unsupported claims
- Circular sourcing
- Conflation of activity with effect
- Guilt by association
- Overstatement of PRC control
- Ignored host-nation agency
- Missing alternative explanations
- False precision
- Stale evidence
- Inconsistent scoring
- Weak indicators
- Conclusions not tied to a decision

Return a table with issue, severity, location, why it matters, and a specific fix.
```

## Citation and Claim Audit

**Purpose:** Ensure every factual claim is traceable

```text
Audit the draft against the supplied source packet. Break each paragraph into atomic factual claims and judgments.

For each, identify:
- Supporting source and exact location
- Whether support is direct or inferential
- Missing, contradictory, derivative, or outdated support

Do not create citations. Produce a correction list and a count of unsupported claims.
```

## Update and Change Detection

**Purpose:** Refresh a standing assessment

```text
Compare the current evidence packet with the previous assessment dated [date].

Identify:
- Genuinely new events
- Changed relationships
- Invalidated assumptions
- Threshold crossings
- Score changes
- Collection gaps closed or opened

Distinguish new reporting from new reality. Recommend only those judgment changes supported by diagnostic evidence, and provide a change log with citations.
```
