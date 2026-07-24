# Automations

Deployable specifications for scheduled, event-driven, condition-based, and human-invoked work executed by an LLM, desktop agent, scheduler, workflow engine, or orchestration platform.

An automation is the runtime implementation of an approved workflow. It should be specific enough to deploy or translate into the user's available platform, while remaining documented well enough to review, test, disable, and migrate.

## Why this directory remains separate

`automations/` should not be collapsed into `prompts/`.

- A prompt can help design an automation.
- A workflow explains the approved process.
- An automation defines what actually runs.

Keeping runtime artifacts separate reduces the risk that a draft builder prompt is mistaken for an active job. It also supports environment-specific configuration, version control, testing, change approval, and rollback.

## What belongs here

An automation package may include:

```text
automations/<domain>/<automation-name>/
  README.md
  automation.yaml
  runtime-prompt.md
  approval-matrix.md
  test-cases.md
  rollback.md
```

A single-file automation is acceptable for simple cases, but it must still include the required controls described below.

## Automation types

- **Scheduled:** runs at a defined time or cadence.
- **Event-driven:** runs when a message, file, calendar event, form, or status change occurs.
- **Condition watch:** checks periodically and acts only when a defined condition becomes true.
- **Human-invoked:** starts from an explicit user command but follows a standardized execution plan.

## Day-to-day operating model

Before activation:

1. Complete the relevant builder prompt in `prompts/automation-design/`.
2. Approve the plain-language workflow in `workflows/`.
3. Generate the runtime configuration and prompt.
4. Test against representative historical or synthetic inputs.
5. Verify exclusions, permissions, duplicate prevention, and approval gates.
6. Confirm output destinations, retention, logging, failure alerts, and disable instructions.
7. Obtain explicit user approval to activate.

After activation:

1. Review run logs and exceptions during the initial observation period.
2. Correct false positives, omissions, duplicate actions, or unsafe behavior.
3. Confirm that source systems and permissions remain valid.
4. Re-test after material changes to the workflow, prompt, model, connectors, role, or environment.
5. Review the automation on a defined cadence.
6. Disable it immediately when authority, data access, or expected behavior is uncertain.

## Required automation sections

1. **Name, owner, and maturity**
2. **Objective and linked workflow**
3. **Automation type**
4. **Trigger or schedule**
5. **Time zone, business calendar, and blackout periods**
6. **Required connectors, permissions, and identity context**
7. **Input scope, exclusions, and lookback window**
8. **Runtime model or agent prompt**
9. **Deterministic processing steps**
10. **Human approval gates and preauthorized actions**
11. **Output formats and destinations**
12. **Deduplication and idempotency rules**
13. **Logging, source traceability, and audit requirements**
14. **Failure, retry, timeout, and escalation behavior**
15. **Data sensitivity, retention, and deletion controls**
16. **Test cases and acceptance criteria**
17. **Disable, rollback, and recovery instructions**
18. **Review cadence and change history**

## Scheduling guidance

Use cron only when the execution environment and time zone are explicit. Store a plain-language description beside every machine-readable schedule.

```yaml
schedule:
  type: cron
  expression: "0 7 * * 1-5"
  timezone: "America/New_York"
  description: "At 7:00 AM Eastern, Monday through Friday"
  business_calendar: "user-defined"
  blackout_dates: []
```

For a condition watch, separate the polling cadence from the notification condition.

```yaml
trigger:
  type: condition_watch
  poll_expression: "0 * * * *"
  timezone: "America/New_York"
condition:
  description: "Notify only when an unresolved item exceeds the approved threshold"
```

## Safety model

Routine reading, classification, summarization, extraction, drafting, reconciliation, and record preparation may be automated when authorized.

The following actions require explicit approval unless narrowly preauthorized and documented:

- sending external messages;
- deleting or moving records to trash;
- publishing or distributing products;
- accepting commitments, deadlines, invitations, or task ownership;
- changing authoritative records;
- modifying access or permissions;
- executing financial, legal, personnel, or security-sensitive actions;
- representing a judgment as user-approved.

The automation must stop safely when required sources are unavailable, permissions change, the output cannot be validated, or the requested action exceeds documented authority.

## Current status

One draft package is committed: `staff-work/inbox-maintenance/`, the runtime half of `workflows/staff-work/inbox-organization-and-maintenance.md`. It is a template — unconfigured and not activated — demonstrating the full chain from builder prompt to workflow to deployable package. The discovery-first design prompts are maintained in `prompts/automation-design/`, and approved operating procedures belong in `workflows/` before a runtime package is added here.

This directory is intentionally retained as the controlled destination for tested and authorized automation artifacts.