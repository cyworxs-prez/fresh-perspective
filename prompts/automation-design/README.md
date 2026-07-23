# Automation Design Prompts

Model-ready prompts for helping a user design, configure, test, and document automations on a desktop agent that already has authenticated access to the user's email, calendar, files, Microsoft Office applications, task systems, and other identity-bound resources.

These prompts do not assume a specific orchestration platform. The agent should translate the resulting specification into the scheduler, workflow engine, local agent framework, or cron-compatible environment available on the user's system.

## Core assumptions

- The desktop agent is already installed and operational.
- Required connectors, identity, PKI, and permissions are already configured.
- The agent can read permitted resources and create or update authorized artifacts.
- The agent must not infer authority to send, delete, publish, approve, or commit the user without explicit configuration.
- The user remains the approval authority for consequential or irreversible actions unless a narrow preauthorization is documented.

## Design sequence

Every automation-builder prompt should guide the agent through:

1. Clarifying the user's objective and desired outcome.
2. Discovering relevant systems, folders, mailboxes, calendars, templates, and systems of record.
3. Establishing scope, exclusions, lookback periods, schedules, time zones, and business-day rules.
4. Defining prioritization, escalation, classification, and exception logic.
5. Defining what may occur automatically and what requires approval.
6. Selecting output formats, destinations, naming conventions, and retention rules.
7. Creating a machine-readable automation specification.
8. Creating a plain-language workflow and user operating guide.
9. Producing test cases and a dry-run plan.
10. Requiring user approval before activation.

## Initial prompts

- `automation-builder-master-prompt.md`
- `morning-email-triage-and-brief-builder.md`

## Required outputs from the agent

Each builder should produce:

- Configuration summary
- Assumptions and unresolved choices
- Workflow description
- Trigger or schedule
- Model execution prompt
- Connector and permission map
- Approval matrix
- Failure and retry behavior
- Audit and retention rules
- Test plan
- Rollback or disable instructions
- Final activation checklist
