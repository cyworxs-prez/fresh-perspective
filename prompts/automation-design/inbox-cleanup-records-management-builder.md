# Inbox Cleanup and Records Management Automation Builder

Design an automation that reduces inbox clutter while preserving records, context, and user control.

## Interview the user
Determine:
- Included mailboxes, folders, shared inboxes, and aliases
- Retention, legal hold, records-management, privacy, and organizational policy constraints
- Definitions of archive candidate, newsletter, notification, duplicate, stale thread, spam, and record copy
- Protected senders, topics, projects, dates, attachments, and folders
- Whether the agent may label, categorize, move, archive, unsubscribe, or delete
- Required approval thresholds for destructive actions
- Cleanup cadence, lookback window, and maximum batch size
- Whether related files, tasks, or correspondence must be preserved elsewhere
- Reporting and rollback expectations

## Build requirements
Produce:
1. Scope and policy constraints
2. Classification taxonomy
3. Schedule and batch limits
4. Runtime prompt
5. Exclusion and protected-record rules
6. Deduplication and thread handling
7. Approval matrix by action type
8. Preview report and rollback mechanism
9. Audit and retention log
10. Failure, retry, and partial-run behavior
11. Historical dry run in preview-only mode
12. Acceptance criteria and activation checklist

## Processing rules
- Default to preview-only until the user approves action categories.
- Never delete material subject to retention, litigation hold, records policy, or unresolved business need.
- Preserve thread context and attachments.
- Distinguish inbox removal from deletion.
- Use reversible actions before irreversible actions.
- Record every moved, archived, unsubscribed, or deleted item.
- Repeated runs must not reprocess the same approved batch.

## Required output
Return the automation specification, cleanup preview, protected-record rules, unresolved questions, dry-run findings, rollback plan, and activation checklist.