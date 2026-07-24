# Inbox Organization and Maintenance Workflow

**Maturity:** Draft — template operating procedure produced from `prompts/automation-design/inbox-organization-and-cleanup-builder.md`. It becomes an approved procedure only after the builder has been run in the user's environment, the discovered values below are filled in, and the user approves the result.

## Purpose

Establish and keep a durable inbox structure — folders, rules, color-coded categories, and flags — so that cleanup is a one-time migration plus low-touch recurring maintenance, not a repeated manual effort. Organization precedes cleanup; deletion is never the default disposition.

## Trigger

- One-time: user-invoked initial organization and cleanup, designed and approved through the builder prompt.
- Recurring: scheduled maintenance run (cadence set at design time; typically weekly) executed by the companion automation `automations/staff-work/inbox-maintenance/`.

## Inputs

- The approved design record from the builder: in-scope mailboxes, protected folders, target folder structure, rule set, category scheme, flag conventions, and cleanup dispositions.
- The current state of the in-scope mailboxes at run time.
- Retention, legal-hold, records-management, and privacy constraints confirmed by the user.

## Procedure

1. **Discover (read-only).** Inventory in-scope mailboxes: folder tree with counts, rules, categories, flags, sender and volume profile, and clutter profile. Take no action.
2. **Compare.** Diff the discovered state against the approved design: mail that missed rules, misfiled items, aged archive candidates, newsletter backlog, duplicates, and rule or category drift.
3. **Preview.** Produce a batch preview grouped by action category (apply rules, refile, archive, unsubscribe candidates) with counts and samples. No destructive action is in scope for automatic execution.
4. **Execute approved categories.** Apply only the action categories the user preauthorized at design time, within the batch limit. Route everything else — and every possible-record — to the user.
5. **Log.** Record every moved, recategorized, archived, or rule-applied item in the audit log.
6. **Report.** Deliver a one-screen maintenance summary: actions taken, items awaiting approval, drift observed, and any access failures.

## Human approval gates

Required before:

- Activating the recurring automation or changing its schedule or scope.
- Any deletion (disabled by default), unsubscribe, or change to rules and categories beyond the approved design.
- Processing any folder or item that matches a retention, legal-hold, or records indicator.
- Expanding scope to a mailbox or folder not in the approved design.

## Outputs

- Maintenance summary report to the approved destination.
- Updated audit log.
- Pending-approval queue for out-of-policy items.

## Audit trail

Record run timestamp, item identifiers, before and after state (folder, category, flags), action category, batch ID, approvals granted, and failures. Repeated runs must not reprocess an approved batch.

## Quality checks

- No action executed outside a preauthorized category.
- Archive, never delete, as the default disposition.
- Possible-records routed to the user, not processed.
- Thread context and attachments preserved on refile.
- The report distinguishes actions taken from actions recommended.
