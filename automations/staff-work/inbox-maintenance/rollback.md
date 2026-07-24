# Rollback and Recovery — Inbox Maintenance

## Disable

1. Remove or pause the schedule in the runtime platform (cron entry, scheduler job, or agent task).
2. Set `status: disabled` in `automation.yaml` and record who disabled it and why.
3. The pending-approval queue remains valid; no action is lost by disabling.

## Undo a run

Every action is logged with before and after state, so a run is reversible:

1. Identify the batch ID in the audit log.
2. For each logged item, restore the recorded before-state (folder, categories, flags). Rule applications and refiles reverse cleanly; archives move back from the archive folder.
3. Deletion is disabled by design, so no run can require unrecoverable restoration.
4. Record the reversal as its own audit entry referencing the original batch ID.

## Recover from partial failure

A partially completed batch is safe to leave: idempotency tracking means the next run will not repeat completed items, and incomplete items simply reappear in the next preview. Do not hand-complete a failed batch; fix the cause, then let the next run pick it up.

## When to roll back versus re-design

Reverse a run when the configuration was right but execution was wrong. Re-enter the design process (builder prompt → workflow approval → package update) when the configuration itself was wrong — repeated false positives, wrong dispositions, or scope complaints. Do not patch the runtime prompt or YAML in place on an active automation without re-approval.
