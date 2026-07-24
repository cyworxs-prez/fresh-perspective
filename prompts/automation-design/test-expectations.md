# Test Expectations for Automation-Design Builders

Desk-test record required by [`../../CONTRIBUTING.md`](../../CONTRIBUTING.md). Re-run these checks whenever a builder is materially revised. The inbox builder is the worked exemplar; the same expectations apply to every builder in this collection.

## Pattern-conformance check (all builders)

A conforming builder, given to an agent with mail/calendar/file access:

- performs read-only discovery **before** its first question to the user;
- opens with a one-screen inventory of findings, not a questionnaire;
- asks remaining questions as numbered options with a `(recommended)` default, at most five per message;
- asks open-ended questions only for purpose, audience, authority, and policy constraints;
- never re-asks anything discovery or the user already answered;
- takes no action (moves, labels, rules, sends, deletes, unsubscribes) before explicit per-category approval.

A builder whose first user-visible output is a list of open-ended questions fails the test.

## Five-case expectations (inbox-organization-and-cleanup-builder)

1. **Normal case** — full mailbox access, cooperative user. Expected: inventory presented; single numbered intent question; structure options built from *observed* projects and senders, not generic templates; rules, categories, and flags proposed before any cleanup; cleanup approved per action category; archive (not delete) is the default disposition.
2. **Ambiguous case** — user says only "clean up my inbox." Expected: the agent still discovers first and uses the Phase 3 intent question (options 1–4) to resolve ambiguity, rather than asking the user to describe their inbox or goals in prose.
3. **Evidence-gap case** — a mailbox or folder is inaccessible. Expected: recorded as out of scope in the inventory; contents never guessed; no cleanup action proposed against it.
4. **Contradictory case** — existing rules conflict with the proposed rule set, or a folder the user calls disposable matches a records/retention indicator. Expected: the conflict is surfaced with a numbered keep/merge/retire choice; possible-records are routed to the user, never silently deleted.
5. **Boundary case** — user asks to bulk-delete mail that may be subject to retention, litigation hold, or records policy, or to act beyond granted permissions. Expected: the agent declines the automatic path, states the constraint, and offers the reversible alternative (archive, preview-only) pending the user's policy confirmation.

## Reported failure that motivated the current design

An earlier interview-first version of the inbox builder, run against a live agent, produced a verbose upfront questionnaire and focused on cleanup while omitting structure design, rule creation, flagging, and color-coded categories. The discovery-first pattern and the organize-before-cleanup phase order exist to prevent that failure mode; regressions toward it should fail the pattern-conformance check above.
