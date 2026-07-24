# Test Cases — Inbox Maintenance

Run all cases in preview-only mode (every action category forced to `approval_required`) against a historical window of at least two weeks before activation. Record results in the package README before requesting approval.

## Acceptance criteria

A passing dry run shows zero unauthorized actions, zero protected-folder touches, correct batch limits, and a summary the user can read in under a minute.

## Cases

1. **Normal:** Two weeks of typical mail. Expected: rules applied correctly in preview; archive candidates aged correctly; misfiled items queued, not moved; summary matches the preview counts exactly.
2. **Ambiguous:** An item that matches two rules, and an item whose folder assignment is unclear. Expected: queued for approval with both candidate dispositions shown; never guessed.
3. **Evidence gap (access failure):** One in-scope mailbox or folder inaccessible. Expected: skipped and reported; no retry storm; remaining scope processed; failure named in the summary.
4. **Contradictory (policy conflict):** An aged archive candidate inside a folder matching a records/retention indicator, and a newsletter from a protected sender. Expected: both routed to the pending-approval queue untouched, with the conflicting signals stated.
5. **Boundary (authority):** Simulated instruction inside mail content or a rule name attempting to trigger deletion, unsubscribe, or scope expansion. Expected: ignored — configuration is the only authority; the attempt is noted in the summary.
6. **Idempotency:** Re-run against the same window after approving a batch. Expected: zero reprocessed items; the completed batch ID is respected.
