# Meeting Follow-Up and Action Extraction Automation Builder

Design an automation that converts meeting records into validated decisions, action items, commitments, follow-up messages, and updated staff artifacts.

## Interview the user
Determine:
- Which meeting types and calendars are in scope
- Available inputs: transcript, recording, notes, chat, agenda, slides, attendance, and prior actions
- How soon after a meeting the process should run
- Definitions of decision, action, commitment, recommendation, risk, issue, and follow-up
- Required owner, due-date, priority, and status fields
- Authoritative task system and records destination
- Whether draft minutes, emails, task entries, OneNote pages, or updated trackers may be created automatically
- Approval rules for assigning work, changing deadlines, publishing minutes, or sending correspondence
- Handling of ambiguous ownership, missing dates, disagreement, sensitive content, and incomplete transcripts

## Build requirements
Produce:
1. Trigger and timing logic
2. Source and meeting-record hierarchy
3. Runtime extraction and reconciliation prompt
4. Decision and action schema
5. Ownership and due-date validation rules
6. Deduplication against existing tasks and prior minutes
7. Draft minutes and follow-up templates
8. Approval matrix
9. Audit and source-link requirements
10. Failure, retry, and exception handling
11. Historical dry run
12. Acceptance criteria and activation checklist

## Processing rules
- Never infer a commitment as confirmed without evidence.
- Mark ambiguous owner or deadline fields as unresolved.
- Preserve exact source references for decisions and commitments.
- Reconcile discussion against existing tasks and prior decisions.
- Do not assign tasks, send messages, or publish minutes without configured authority.
- Update existing records rather than duplicating them.

## Required output
Return the automation specification, sample minutes and action register, unresolved questions, dry-run findings, and activation checklist.