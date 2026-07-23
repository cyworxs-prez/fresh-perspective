# Automation Design Prompts

Interview-first, model-ready prompts for helping a user design, configure, test, document, and approve recurring work on a desktop agent that already has authenticated access to the user's email, calendar, files, Microsoft Office applications, task systems, and other identity-bound resources.

**Maturity:** Reference design prompts. Individual generated workflows and automations remain drafts until reviewed and tested in the user's environment.

These prompts do not assume a specific orchestration platform. The agent should translate the approved design into the scheduler, workflow engine, local agent framework, or cron-compatible environment available on the user's system.

## Core assumptions

- The desktop agent is already installed and operational.
- Required connectors, identity, PKI, and permissions are already configured.
- The agent can read permitted resources and create or update authorized artifacts.
- The agent may inspect only resources approved by the user for the automation being designed.
- The agent must not infer authority to send, delete, publish, approve, accept commitments, or represent user judgment without explicit configuration.
- The user remains the approval authority for consequential or irreversible actions unless a narrow preauthorization is documented.
- Builder prompts design and document automations; they do not activate them without explicit approval.

## How to use these prompts

1. Select the builder that best matches the recurring staff task.
2. Give the complete builder prompt to the user's authenticated desktop agent or LLM.
3. Allow the agent to interview the user in manageable sections.
4. Let the agent inspect only user-approved mailboxes, calendars, folders, templates, task systems, notebooks, or prior products.
5. Review the proposed scope, schedule, exclusions, priorities, approval boundaries, and output format.
6. Run a dry test against historical or synthetic inputs.
7. Correct false positives, omissions, duplicate behavior, and unsupported assumptions.
8. Save the approved plain-language process under `workflows/<domain>/`.
9. Save the tested runtime configuration under `automations/<domain>/`.
10. Require explicit approval before activation.

## Design sequence

Every automation-builder prompt should guide the agent through:

1. Clarifying the user's objective and desired outcome.
2. Discovering relevant systems, folders, mailboxes, calendars, templates, and systems of record.
3. Establishing scope, exclusions, lookback periods, schedules, time zones, business-day rules, and blackout periods.
4. Defining prioritization, escalation, classification, and exception logic.
5. Defining what may occur automatically and what requires approval.
6. Selecting output formats, destinations, naming conventions, and retention rules.
7. Creating a plain-language workflow.
8. Creating a machine-readable or platform-translatable automation specification.
9. Creating the runtime model or agent prompt.
10. Producing test cases, acceptance criteria, and a dry-run plan.
11. Defining disable, rollback, and recovery behavior.
12. Requiring user approval before activation.

## Required outputs from the agent

Each builder should produce:

- configuration summary;
- assumptions and unresolved choices;
- plain-language workflow;
- trigger, schedule, time zone, and business-calendar logic;
- runtime model execution prompt;
- connector, permission, and identity-context map;
- automatic-action and approval matrix;
- output formats and destinations;
- deduplication and idempotency rules;
- failure, retry, timeout, and escalation behavior;
- audit, traceability, and retention rules;
- test plan and acceptance criteria;
- rollback or disable instructions;
- final activation checklist.

## Artifact destinations

The builder output should be separated after review:

```text
workflows/<domain>/<workflow-name>.md
```

Stores the approved human-readable operating procedure.

```text
automations/<domain>/<automation-name>/
```

Stores the tested runtime prompt, schedule, configuration, approval matrix, test cases, and rollback instructions.

The builder prompt remains here as a reusable design tool.

## Available builders

### General

- `automation-builder-master-prompt.md` — designs a new automation when no specialized builder exists.

### Email and inbox management

- `morning-email-triage-and-brief-builder.md` — configures morning inbox triage, prioritization, action extraction, and briefing.
- `inbox-cleanup-records-management-builder.md` — configures records-aware inbox cleanup, retention, labeling, and approval controls.

### Reporting and activity capture

- `end-of-day-staff-report-builder.md` — configures an end-of-day summary of progress, decisions, blockers, and next actions.
- `weekly-activity-rollup-builder.md` — configures a weekly accomplishment, activity, issue, and suspense rollup.
- `quarterly-activity-report-builder.md` — configures a quarterly report generated from approved sources such as email, calendar, task systems, OneNote, and Office artifacts.

### Meeting support

- `meeting-preparation-read-ahead-builder.md` — configures meeting research, agenda preparation, read-ahead assembly, open-question identification, and decision support.
- `meeting-follow-up-action-builder.md` — configures meeting-note reconciliation, decision capture, action extraction, task preparation, and follow-up drafting.

### Task and suspense management

- `overdue-action-suspense-watch-builder.md` — configures recurring monitoring for approaching, overdue, blocked, or unowned actions and deadlines.

## Choosing a builder

Use the specialized builder when one matches the task. Use the master builder when:

- the process spans multiple staff functions;
- the desired automation is not represented here;
- the user wants to combine several builders into one coordinated workflow;
- the task requires a custom event, condition, or approval sequence.

When combining builders, establish one authoritative workflow and prevent overlapping automations from creating duplicate tasks, reports, or notifications.