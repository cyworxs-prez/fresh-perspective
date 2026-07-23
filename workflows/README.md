# Workflows

Reusable, human-readable operating procedures for recurring staff work.

A workflow describes how work moves from trigger to completed product. It should define the objective, inputs, sequence, decision points, review gates, outputs, records, and measures of success. Workflows are tool-agnostic unless a specific implementation is required.

## Required workflow sections

1. Purpose
2. Trigger
3. Inputs and authoritative sources
4. Roles and responsibilities
5. Procedure
6. Decision points and exceptions
7. Human review and approval gates
8. Outputs and destinations
9. Audit trail and retention
10. Failure handling
11. Measures and quality checks
12. Related skills, prompts, and automations

## Design principles

- Automate collection, sorting, extraction, drafting, and routine formatting where safe.
- Preserve human ownership of judgments, commitments, external communications, and irreversible actions.
- Separate facts, model inference, assumptions, and unresolved questions.
- Make every recurring product traceable to its source material.
- Design for idempotency so a repeated run does not create duplicate records or duplicate notifications.
- Define the system of record for each task, action, report, and decision.
- Use explicit escalation thresholds instead of vague concepts such as “important.”
- Record failures, partial completion, and unavailable sources rather than silently omitting them.

## Initial staff-work workflows

- `staff-work/inbox-triage.md`
- `staff-work/daily-start-of-day-brief.md`
- `staff-work/end-of-day-report.md`
- `staff-work/quarterly-activity-report.md`
