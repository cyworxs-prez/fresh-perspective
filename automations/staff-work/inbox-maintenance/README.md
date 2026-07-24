# Inbox Maintenance Automation

**Status: draft template — not activated.** This package is the runtime specification for the recurring phase of `workflows/staff-work/inbox-organization-and-maintenance.md`, produced as the repository's first complete skill-to-automation chain: builder prompt → approved workflow → deployable package.

It is deliberately unconfigured: every empty field in `automation.yaml` must be filled from the user's own builder session, the dry run in `test-cases.md` must pass in the user's environment, and the user must explicitly approve activation. Do not deploy it as-is.

## Package contents

- `automation.yaml` — trigger, schedule, scope, actions, limits, and logging configuration.
- `runtime-prompt.md` — the model prompt the scheduled agent executes each run.
- `approval-matrix.md` — what runs automatically versus what requires approval.
- `test-cases.md` — dry-run plan and acceptance criteria.
- `rollback.md` — disable, undo, and recovery procedure.

## Lifecycle

1. Design with `prompts/automation-design/inbox-organization-and-cleanup-builder.md` (discovery-first).
2. Record the approved process in the workflow document.
3. Fill this package's configuration from the approved design.
4. Run the historical dry run in preview-only mode; correct false positives and omissions.
5. Obtain explicit user approval; only then schedule it.
6. Review at the cadence set in `automation.yaml` and whenever mailboxes, policies, or roles change.
