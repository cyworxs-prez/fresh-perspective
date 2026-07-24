# Fresh Perspective

A reusable library of AI skills, model-ready prompts, operating workflows, automation specifications, templates, and reference material for analysis, planning, staff work, research, reporting, and knowledge work.

Fresh Perspective helps a human user move from an informal request to a repeatable, reviewable, and eventually automatable way of working. The repository separates **reusable capability**, **model interaction**, **approved operating procedure**, and **runtime implementation**.

## Human-led operating philosophy

The model supplements a trained analyst, planner, researcher, reviewer, or staff officer. It does not become the accountable analyst.

Every substantive analytic asset must:

- interview the user before beginning;
- confirm the mission, decision, intelligence question, audience, scope, timeframe, actors, source set, handling restrictions, deliverable, and approval authority;
- use only authorized and identified information;
- prohibit fabricated reporting, citations, doctrine, collection, confidence, and judgments;
- distinguish reported information, source characterization, inference, assumption, judgment, likelihood, confidence, and implication;
- expose contradictory evidence, alternatives, uncertainty, and gaps;
- require human adjudication before finalization or consequential action.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for mandatory contribution and quality requirements.

## Core operating model

| Asset | Purpose | Typical use |
|---|---|---|
| **Skill** | Defines reusable capability, tradecraft, decision points, constraints, quality standards, and expected outputs. | Give an LLM or agent a reliable method for assisting a human with a class of work. |
| **Prompt** | Provides model-ready instructions for a bounded interaction or task. | Interview a user, execute a skill, design an automation, or perform a diagnostic review. |
| **Workflow** | Documents the approved human-and-machine operating procedure from trigger to completed product. | Explain who does what, in what order, using which sources and review gates. |
| **Automation** | Defines deployable runtime behavior: trigger, schedule, execution prompt, permissions, outputs, logging, retries, and rollback. | Run an approved workflow through an agent, scheduler, workflow engine, or orchestration platform. |
| **Template** | Provides a reusable working artifact or output schema. | Preserve traceability and make repeated execution consistent. |

### Why prompts, workflows, and automations remain separate

These directories are intentionally not collapsed.

- A **builder or execution prompt** controls a model interaction.
- A **workflow** records the reviewed and approved process in plain language.
- An **automation** records the machine-executable or platform-translatable implementation.

Keeping them separate prevents a draft prompt from being mistaken for an approved operating procedure or active automation. It also supports version control, testing, review, rollback, and platform portability.

## Repository structure

The top level describes the asset type. Subfolders describe the governing community, service, doctrine, domain, or shared methodology.

```text
skills/
  README.md
  shared/
    intelligence-tradecraft/
      <skill-name>/SKILL.md
  joint/
    intelligence/
      <skill-name>/SKILL.md
  ic/
    icd/
      <directive-or-skill-name>/SKILL.md
  army/
    intelligence/
  navy/
    intelligence/
  marine-corps/
    intelligence/
  air-force/
    intelligence/
  space-force/
    intelligence/
  functional/
    <methodology-collection>/
      <skill-name>/SKILL.md

prompts/
  README.md
  shared/
    intelligence-tradecraft/
  joint/
    intelligence/
  ic/
    icd/
  <service>/
    intelligence/
  functional/
    <methodology-collection>/
  automation-design/

workflows/
  README.md
  <domain-or-function>/

automations/
  README.md
  <domain-or-function>/
    <automation>.yaml
    <runtime-prompt>.md
    <test-cases>.md

templates/
  intelligence/
  <other-domain>/
```

Templates live centrally under `templates/`; skills link to them rather than carrying their own copies.

Planned but not yet populated: `frameworks/`, `examples/`, and `docs/` top-level directories, and the navy, marine-corps, air-force, and space-force service namespaces.

A publication is normally a reference inside a functional skill rather than a top-level folder. Publication-specific implementation belongs under the governing namespace, such as `skills/ic/icd/icd-203-analytic-standards/`.

Namespace rule: a collection governed by a specific community's doctrine or policy lives under `shared/`, `joint/`, `ic/`, or a `<service>/` namespace. A methodology collection that applies across communities and is not owned by any one doctrine — such as influence and access analysis, homeland indicators and warning, or generalized all-source research — lives under `functional/`.

Use `shared/` for methods that are substantially common across communities, including analyst interviews, evidence ledgers, structured analytic techniques, assumptions, confidence support, and analytic writing. Create a Joint or Service-specific version when doctrine, terminology, workflow, or required artifacts materially differ.

Directories may remain empty until an approved artifact exists. A builder prompt may exist before the corresponding workflow or automation is designed, tested, and authorized.

## Day-to-day integration

### Human-led intelligence analysis

Recommended sequence:

1. Run `prompts/shared/intelligence-tradecraft/interview-and-scope.md`.
2. Confirm the analysis profile and record the information cutoff.
3. Build the claim-and-evidence ledger using only authorized sources.
4. Select the relevant Joint, Service, IC, or functional skill.
5. Apply structured analytic techniques when they address a defined uncertainty or failure mode.
6. Draft key judgments with the organization's approved estimative-language convention.
7. Apply applicable sourcing and analytic-standard reviews.
8. Present every material judgment, confidence level, assumption, indicator, and gap for human adjudication.
9. Complete classification, disclosure, supervisory, and product-line review outside the model where required.
10. Save approved working artifacts and lessons for the next update.

### Recurring staff work and automation design

1. Open the relevant prompt in `prompts/automation-design/`.
2. Give it to the user's authenticated desktop agent or LLM.
3. Let the agent interview the user about purpose, scope, sources, schedule, exclusions, permissions, output, and approval boundaries.
4. Review the proposed workflow, automation specification, runtime prompt, approval matrix, and test plan.
5. Save the approved process under `workflows/`.
6. Save the deployable configuration under `automations/`.
7. Run a historical or non-destructive dry test.
8. Correct false positives, omissions, duplicate behavior, and unsafe actions.
9. Require explicit user approval before activation.
10. Review periodically and when roles, systems, permissions, or requirements change.

## Current collections

### Shared intelligence tradecraft

`skills/shared/intelligence-tradecraft/`

Initial skills:

- analyst interview and task scoping;
- evidence and claim ledger;
- structured analytic technique facilitation;
- assessment language and confidence support;
- intelligence requirements and collection support (candidate PIR/EEI/SIR/RFI lifecycle without tasking authority).

Companion prompts are under `prompts/shared/intelligence-tradecraft/`, with reusable working artifacts under `templates/intelligence/`.

### Joint intelligence

`skills/joint/intelligence/`

Initial JIPOE skills support:

- scope, operational-environment definition, significant characteristics, and environmental effects;
- actor, capability, course-of-action, indicator, and gap analysis.

Companion prompts are under `prompts/joint/intelligence/`.

### Intelligence Community directives

`skills/ic/icd/`

Initial directive-based skills support:

- ICD 203 analytic-standards review;
- ICD 206 sourcing and traceability review.

Companion prompts are under `prompts/ic/icd/`. These are diagnostic aids, not organizational compliance certifications.

### Army intelligence

`skills/army/intelligence/`

Army IPB skills covering all four steps: define the operational environment, describe environmental effects, evaluate the threat, and determine threat courses of action. Companion prompts are under `prompts/army/intelligence/`.

### Influence and access analysis

`skills/functional/influence-access-analysis/`

Actor-neutral skills for area baselining, source tradecraft, environmental mapping, actor-network analysis, critical-node analysis, indicators and warning, analytic integration, and commander or executive reporting.

### Homeland indicators and warning

`skills/functional/homeland-indicators-warning/`

Whole-of-government strategic-warning skill correlating lawful civilian, regulatory, commercial, infrastructure, and security observations into decision-linked Homeland warning.

### All-source research and analysis

`prompts/functional/research-analysis/all-source/`

A fifteen-prompt sequence for generalized all-source research: problem decomposition, search strategy, source extraction, ownership and finance mapping, network and system analysis, competing hypotheses, indicators, confidence calibration, judgment drafting, red-team critique, citation audit, and update detection.

### Automation design

`prompts/automation-design/`

Discovery-first prompts for configuring recurring staff work on an already authenticated desktop agent, including email triage, periodic reporting, meeting support, suspense tracking, and inbox organization with records-safe cleanup. Each builder inspects the authorized environment first, presents what it found, and resolves remaining choices as numbered options with recommended defaults.

## Governance and safety

Every reusable asset must:

- remain human-led and interview-first;
- avoid inheriting a country, actor, mission, audience, mailbox, source set, schedule, or desired conclusion without confirmation;
- preserve traceability from outputs to authorized evidence;
- record unavailable sources, partial completion, and failures;
- distinguish mandatory policy, authoritative doctrine, local requirements, and recommended tradecraft;
- treat current command, agency, product-line, security, disclosure, legal, privacy, and supervisory guidance as controlling;
- define what the model may do automatically and what requires approval;
- require explicit authority for sending, deleting, publishing, disseminating, tasking, approving, accepting commitments, or changing authoritative records;
- include test, disable, rollback, retention, and audit instructions for automations;
- remove prior-client, country, adversary, report, personal, and environment-specific details from reusable assets unless they are intentional examples.

## Contribution workflow

1. Read [`CONTRIBUTING.md`](CONTRIBUTING.md).
2. Determine the asset type and governing namespace.
3. Start from the closest skill, prompt, or template.
4. Add the mandatory interview, source boundaries, evidence rules, stop conditions, quality checks, and human approval gate.
5. Distinguish doctrine or policy requirements from repository recommendations.
6. Link related skills, prompts, workflows, automations, templates, and references.
7. Test normal, ambiguous, evidence-gap, contradictory, and boundary cases.
8. Commit only artifacts that meet their declared maturity level.

## Maturity labels

- **Draft:** concept or initial implementation; not yet validated.
- **Tested:** exercised against representative normal and failure cases.
- **Operational:** approved for recurring use in a defined environment.
- **Reference:** stable guidance or template intended for reuse.

## Roadmap

Deferred capabilities, in rough priority order:

- collection management as a dedicated skill (PIR/RFI/ISR request lifecycle beyond the existing indicators-and-warning fragments);
- finished-product templates (warning note, intelligence summary, read-ahead formats);
- promotion of OSINT-specific sourcing guidance from the influence collection into `shared/`;
- navy, marine-corps, air-force, and space-force intelligence namespaces;
- `frameworks/`, `examples/`, and `docs/` directories once approved content exists;
- promotion of skills from draft to tested as live-session results land in each collection's `test-expectations.md`.

## License

This repository is licensed under [Creative Commons Attribution 4.0 International](LICENSE) (CC BY 4.0). Nothing here is official doctrine or policy; local authority always governs.

## Status

Fresh Perspective is an evolving library. Current work is establishing a human-led, doctrine-grounded intelligence tradecraft foundation while retaining the repository's existing generalized analysis and interview-driven automation-design capabilities.