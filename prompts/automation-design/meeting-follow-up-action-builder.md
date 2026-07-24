# Meeting Follow-Up and Action Extraction Automation Builder

Design an automation that converts meeting records into validated decisions, action items, commitments, follow-up messages, and updated staff artifacts.

## Interaction rules
Discovery first: inspect the authorized systems (read-only) before asking the user anything, and open with a one-screen summary of findings — not a questionnaire. Ask remaining questions as numbered options with a recommended default marked `(recommended)`, at most five per message. Reserve open-ended questions for facts only the user knows. Never re-ask what discovery or the user already answered.

## Discover first (read-only)
- Enumerate accessible calendars and profile the recurring meetings and their typical records
- Determine which inputs actually exist per meeting type: transcripts, recordings, notes, chat, agendas, slides, attendance, prior actions — and where they are stored
- Identify candidate authoritative task systems and any existing minutes or action-register formats

Present the profile, then confirm scope by number.

## Then confirm with the user
Resolve as numbered choices with recommended defaults, in at most two messages:
- Which discovered meeting types are in scope
- How soon after a meeting the process should run
- Definitions of decision, action, commitment, recommendation, risk, issue, and follow-up (offer defaults)
- Required owner, due-date, priority, and status fields
- The authoritative task system and records destination (confirm the discovered candidates)
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