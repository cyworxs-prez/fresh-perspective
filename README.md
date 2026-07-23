# Fresh Perspective

A reusable library of AI skills, model-ready prompts, operating workflows, and automation specifications for analysis, staff work, research, reporting, and knowledge work.

Fresh Perspective is intended to help a user move from an informal request to a repeatable, reviewable, and eventually automated way of working. The repository separates **how a model should reason**, **how a user should configure a task**, **how the work should be performed**, and **how the task should run automatically**.

## Core operating model

Fresh Perspective uses four primary asset types:

| Asset | Purpose | Typical use |
|---|---|---|
| **Skill** | Defines reusable capability, tradecraft, quality standards, constraints, and expected outputs. | Give an LLM or agent a reliable way to perform a class of work. |
| **Prompt** | Provides model-ready instructions for a bounded task or for interviewing a user and designing a solution. | Start a task, configure an automation, or guide a model through a specific interaction. |
| **Workflow** | Documents the approved human-and-machine operating procedure from trigger to completed product. | Explain who does what, in what order, using which sources, with which review gates. |
| **Automation** | Defines the deployable runtime behavior: trigger, schedule, execution prompt, permissions, outputs, logging, retries, and rollback. | Run an approved workflow through a desktop agent, scheduler, workflow engine, or orchestration platform. |

### Why prompts, workflows, and automations remain separate

These directories are intentionally not collapsed.

- A **builder prompt** interviews the user and proposes a design.
- A **workflow** records the reviewed and approved process in plain language.
- An **automation** records the machine-executable or platform-translatable implementation.

Keeping them separate prevents a draft prompt from being mistaken for an approved operating procedure or an active automation. It also supports version control, human review, testing, rollback, and platform portability.

## Repository structure

```text
skills/
  README.md
  <collection-name>/
    README.md
    <skill-name>/SKILL.md
    templates/

prompts/
  README.md
  <domain-or-function>/
    README.md
    <prompt>.md

workflows/
  README.md
  <domain-or-function>/
    <workflow>.md

automations/
  README.md
  <domain-or-function>/
    <automation>.yaml
    <runtime-prompt>.md
    <test-cases>.md

frameworks/
  <framework-name>/

templates/
examples/
docs/
```

Directories may remain empty until an approved artifact exists. For example, an automation-builder prompt may exist before the corresponding automation is designed, tested, and authorized for use.

## Day-to-day integration

### Use a skill for complex work

Use a skill when the task requires repeatable tradecraft, quality control, or a defined analytical method.

Example operating sequence:

1. Select the relevant skill collection.
2. Complete its required scope or configuration profile.
3. Provide the model access to the relevant sources.
4. Run the skills in the recommended sequence.
5. Review assumptions, evidence, confidence, and unresolved gaps.
6. Produce the final artifact using the reporting or writing skill.
7. Save reusable ledgers, templates, and lessons learned for the next iteration.

### Use an automation-builder prompt for recurring staff work

Use a builder prompt when the work should eventually run on a schedule, event, or condition.

1. Open the relevant prompt in `prompts/automation-design/`.
2. Give it to the user's authenticated desktop agent or LLM.
3. Let the agent interview the user about purpose, scope, schedule, sources, exclusions, output format, permissions, and approval boundaries.
4. Review the proposed workflow, automation specification, runtime prompt, approval matrix, and test plan.
5. Save the approved plain-language process under `workflows/`.
6. Save the deployable configuration under `automations/`.
7. Run a historical or non-destructive dry test.
8. Correct false positives, omissions, duplicate behavior, and unsafe actions.
9. Require explicit user approval before activation.
10. Review the automation periodically and whenever the user's role, systems, permissions, or reporting requirements change.

### Example: morning email triage

A user would run `prompts/automation-design/morning-email-triage-and-brief-builder.md` with their desktop agent. The agent would interview the user, inspect only authorized resources, and produce:

- a proposed inbox-triage workflow;
- a schedule and lookback window;
- priority and escalation rules;
- automatic-action and approval boundaries;
- a runtime execution prompt;
- an output format for the morning brief;
- test cases and rollback instructions.

After review, the approved process belongs in `workflows/staff-work/`, while the platform-specific or portable runtime specification belongs in `automations/staff-work/`.

## Current collections

### Analysis skills

`skills/influence-access-analysis/`

Actor-neutral skills for area baselining, source tradecraft, environmental mapping, actor-network analysis, critical-node analysis, indicators and warning, analytic integration, and commander or executive reporting.

### Automation-design prompts

`prompts/automation-design/`

Interview-first prompts for configuring recurring staff work on an already authenticated desktop agent, including email triage, daily and periodic reporting, meeting support, suspense tracking, and records-safe inbox cleanup.

### Staff-work workflows

`workflows/staff-work/`

Approved, plain-language operating procedures. This section should contain only workflows that have been reviewed and accepted, not preliminary builder output.

### Staff-work automations

`automations/staff-work/`

Deployable automation packages. This section should contain only tested specifications with schedules, runtime prompts, permissions, approval gates, audit behavior, failure handling, and disable instructions.

## Governance and safety

Every reusable asset should follow these rules:

- Do not inherit a country, target actor, partner, mission, mailbox, folder, audience, or schedule from prior work without confirmation.
- Ask for missing information when it would materially change the result.
- Separate fact, inference, assumption, severity, confidence, and unresolved questions.
- Use authoritative sources and identify the system of record.
- Preserve traceability from output back to source material.
- Define what the agent may do automatically and what requires approval.
- Require explicit authority for sending, deleting, publishing, approving, accepting commitments, or changing authoritative records.
- Design recurring operations for idempotency so repeated runs do not create duplicate tasks, drafts, reports, or notifications.
- Record unavailable sources, partial completion, and failures rather than silently omitting them.
- Include test, disable, rollback, retention, and audit instructions for every automation.
- Sanitize reusable assets of prior clients, countries, adversaries, reports, personal identifiers, and environment-specific details unless they are intentionally part of a case-specific example.

## Contribution workflow

1. Determine whether the new asset is a skill, prompt, workflow, automation, framework, template, or example.
2. Start from the closest existing README or template.
3. Remove environment-specific or case-specific details.
4. Add scope questions, assumptions, source requirements, quality checks, and approval boundaries.
5. Add a plain-language usage example.
6. Link related skills, prompts, workflows, and automations.
7. Test with at least one normal case, one exception case, and one failure case.
8. Commit only artifacts that are complete enough for their declared maturity level.

## Maturity labels

Assets should describe their maturity in the file or collection README:

- **Draft:** concept or initial prompt; not yet validated.
- **Tested:** exercised against representative inputs.
- **Operational:** approved for recurring use in a defined environment.
- **Reference:** stable guidance or template intended for reuse.

## Status

Fresh Perspective is an evolving library. Current work is focused on generalized analysis skills and interview-driven staff-work automation design. Workflows and automations will grow as specific processes are configured, tested, approved, and committed.