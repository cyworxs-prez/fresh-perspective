# Inbox Triage Workflow

## Purpose
Reduce inbox noise, surface messages requiring attention, prepare draft responses, and preserve an auditable record of actions without automatically committing the user to external communications.

## Trigger
- Scheduled review at the start of the workday
- Optional midday and end-of-day review
- Manual invocation when backlog exceeds a defined threshold

## Inputs
- Messages received during the configured lookback window
- Existing folders, labels, rules, and priority senders
- Calendar commitments and active task list
- User-defined escalation criteria

## Procedure
1. Retrieve new and unresolved messages.
2. Remove exact duplicates and group messages by conversation.
3. Classify each thread as:
   - Immediate action
   - Action today
   - Action this week
   - Awaiting response
   - Informational
   - Newsletter or bulk notification
   - Archive candidate
   - Possible spam or suspicious
4. Extract sender, subject, request, deadline, owner, dependencies, and attachments.
5. Compare requests against the calendar and task system.
6. Draft responses for messages requiring routine acknowledgment or coordination.
7. Create or update action items with source links.
8. Apply only preauthorized labels or folders.
9. Produce a concise triage digest.
10. Route destructive, sensitive, external, or ambiguous actions for human review.

## Human approval gates
Required before:
- Sending any external response
- Deleting or moving records to trash
- Accepting commitments or deadlines
- Sharing attachments or sensitive content
- Marking a request complete when evidence is incomplete

## Outputs
- Prioritized inbox digest
- Draft replies
- New or updated tasks
- Suggested labels or archive actions
- Escalation list

## Audit trail
Record message identifier, classification, extracted deadline, action taken, draft created, labels changed, reviewer decision, and completion timestamp.

## Quality checks
- No unresolved request is classified as informational without explanation.
- Every extracted deadline includes a source reference.
- Drafts distinguish confirmed facts from assumptions.
- Repeated runs do not create duplicate tasks or drafts.
