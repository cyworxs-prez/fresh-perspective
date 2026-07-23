# Workflows

Human-readable operating procedures for repeatable work performed by people, LLMs, desktop agents, and connected applications.

A workflow explains how work moves from a trigger to a completed product. It is the approved process description, not merely a prompt and not yet the deployable automation configuration.

## Why this directory exists

`workflows/` remains separate from `prompts/` and `automations/` because each serves a different purpose:

- `prompts/` contains instructions used to interview the user or guide a model.
- `workflows/` contains the reviewed operating procedure that people can understand and approve.
- `automations/` contains the runtime specification that a scheduler or agent executes.

The workflow is the control document between design and deployment. It should remain understandable even if the underlying automation platform changes.

## When to create a workflow

Create or update a workflow when:

- a task repeats on a schedule, event, or recurring condition;
- multiple systems or people contribute to one product;
- the user needs consistent quality, escalation, or approval behavior;
- an automation-builder prompt has produced a candidate process;
- an existing automation needs a plain-language source of truth;
- a process should be auditable, transferable, or resilient to personnel changes.

Do not create a workflow merely to store a one-time prompt. A workflow should describe a repeatable operating process.

## Day-to-day use

A user or agent should use a workflow as the operating checklist for recurring work:

1. Confirm the trigger, schedule, and current scope.
2. Retrieve only the authorized sources identified in the workflow.
3. Follow the procedure and decision rules in order.
4. Stop at required human review gates.
5. Deliver outputs to the stated destinations.
6. Record source links, actions taken, exceptions, and failures.
7. Update the workflow when requirements, systems, authorities, or ownership change.

For automated processes, the workflow should be reviewed before changing the runtime configuration. The automation should implement the workflow rather than become the only record of how the process works.

## Required workflow sections

1. **Name and maturity:** draft, tested, operational, or reference.
2. **Purpose and intended outcome**
3. **Trigger, cadence, or invocation condition**
4. **Scope, exclusions, and lookback period**
5. **Inputs and authoritative sources**
6. **Systems of record**
7. **Roles and responsibilities**
8. **Procedure and sequence**
9. **Decision points, thresholds, and exceptions**
10. **Human review and approval gates**
11. **Outputs, formats, and destinations**
12. **Audit trail and retention**
13. **Failure, retry, and escalation handling**
14. **Measures, quality checks, and acceptance criteria**
15. **Related skills, prompts, templates, and automations**
16. **Change history and review date**

## Design principles

- Automate collection, sorting, extraction, drafting, reconciliation, and routine formatting where safe.
- Preserve human ownership of judgments, commitments, external communications, approvals, and irreversible actions.
- Separate confirmed facts, model inference, assumptions, and unresolved questions.
- Make every recurring product traceable to its source material.
- Define the system of record for each task, action, report, and decision.
- Use explicit escalation thresholds instead of vague terms such as “important” or “urgent.”
- Design for idempotency so repeated runs do not create duplicate tasks, drafts, reports, or notifications.
- Record unavailable sources, partial completion, and failures rather than silently omitting them.
- Keep platform-specific commands out of the workflow unless they are essential to the process.

## From builder prompt to workflow

When an automation-builder prompt is completed:

1. Review the proposed process with the user.
2. Resolve assumptions and unanswered questions.
3. Convert the approved plain-language process into a workflow file here.
4. Assign a maturity level of `draft` or `tested`.
5. Link the original builder prompt.
6. Create the deployable implementation under `automations/` only after the workflow is approved.
7. Promote the workflow to `operational` after successful testing and activation.

## Current workflows

- `staff-work/inbox-triage.md` — a reusable inbox triage operating procedure with classification, extraction, draft preparation, task creation, escalation, and approval controls.

Additional staff-work workflows should be committed only after the corresponding builder prompt has been completed, reviewed, and accepted.