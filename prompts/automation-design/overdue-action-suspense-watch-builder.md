# Overdue Action and Suspense Watch Automation Builder

Design a condition-watch automation that identifies approaching, overdue, blocked, or unowned staff actions across authenticated task systems, email, calendar, meeting records, OneNote, Teams, SharePoint, and Office trackers.

## Interview the user
Determine:
- Authoritative task and suspense systems
- Included projects, teams, mailboxes, calendars, notebooks, trackers, and channels
- Definitions of due soon, overdue, blocked, at risk, unowned, and stale
- Warning thresholds by priority and task type
- Business hours, workdays, holidays, and escalation windows
- Required owner, approver, dependency, and status fields
- Notification audiences and preferred delivery channels
- Whether reminders, draft messages, task updates, or calendar holds may be created automatically
- Escalation hierarchy and approval rules
- Exceptions for sensitive, private, paused, cancelled, or externally controlled work

## Build requirements
Produce:
1. Condition definitions and thresholds
2. Polling cadence and machine-readable schedule
3. Source and system-of-record hierarchy
4. Runtime reconciliation prompt
5. Duplicate and stale-record handling
6. Notification and escalation matrix
7. Draft reminder templates
8. Approval gates
9. Audit, retention, retry, and failure behavior
10. Historical dry run
11. Acceptance criteria and activation checklist

## Processing rules
- Reconcile the same action across multiple sources before notifying.
- Do not treat a calendar date as a confirmed suspense unless context supports it.
- Distinguish overdue, blocked, awaiting external response, paused, and cancelled work.
- Avoid repeated notifications unless status, risk, or escalation level changes.
- Preserve owner, due date, source link, dependency, and last verified status.
- Never alter deadlines, owners, or official status without configured authority.

## Required output
Return the automation specification, sample watch report and notifications, unresolved questions, dry-run findings, and activation checklist.