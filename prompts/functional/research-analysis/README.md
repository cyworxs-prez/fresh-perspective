# Research and Analysis Prompts

Generalized, domain-neutral research and analysis prompts usable for intelligence, policy, security, business, and academic problems. These are standalone prompts by design — no single governing skill exists, so each carries its full method inline, per the CONTRIBUTING companion-prompt convention.

## All-source sequence

`all-source/` contains fifteen numbered prompts. The numbering is a workflow, not a mandate — enter at the step that matches the task and skip steps the task does not need.

| Step | Prompt | Use when you need to |
|---|---|---|
| 01 | problem-decomposition | Turn a broad requirement into answerable questions and a work plan |
| 02 | search-strategy-generator | Design a source-aware search and collection approach |
| 03 | source-extraction | Extract structured claims and evidence from authorized sources |
| 04 | ownership-finance-mapping | Reconstruct ownership, control, and financing chains |
| 05 | strategic-optionality-assessment | Assess an actor's options and freedom of action |
| 06 | campaign-synchronization | Correlate activity across instruments, actors, and time |
| 07 | system-node-mapping | Map systems, dependencies, and critical nodes |
| 08 | network-analysis | Analyze actor and relationship networks |
| 09 | competing-hypotheses | Test explanations with an ACH matrix |
| 10 | indicators-warning | Build decision-linked indicators and thresholds |
| 11 | confidence-calibration | Calibrate likelihood and confidence language |
| 12 | executive-judgment-drafting | Convert approved analysis into decision-ready judgments |
| 13 | red-team-critique | Adversarially review a draft before publication |
| 14 | citation-claim-audit | Audit claims against citations and sourcing |
| 15 | update-change-detection | Refresh a standing assessment and isolate real change |

## Typical entry points

- **New problem:** 01 → 02 → 03, then the analytic steps the problem requires.
- **Draft in hand:** 13 and 14, then 11 and 12.
- **Standing assessment:** 15, then only the steps the changes touch.

## Interaction contract

Every prompt interviews the user for missing critical parameters before working, uses only the approved evidence corpus, refuses to invent evidence or sources, exposes alternatives and gaps, and leaves judgments, confidence, and release decisions with the human analyst.

For intelligence tasks governed by organizational standards, pair this sequence with the shared tradecraft skills: run `skills/shared/intelligence-tradecraft/analyst-interview-and-scope/` first, keep the evidence ledger from `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`, and apply the ICD 203/206 review skills before release where they apply.
