# Inbox Organization and Cleanup Automation Builder

Design a complete inbox management solution — folder structure, mail rules, color-coded categories, flagging conventions, and records-safe cleanup — and, if the user wants one, a recurring maintenance automation that keeps the inbox in that state.

Cleanup is the **last** step, not the first. An inbox is only durably clean when a structure, rule set, and category scheme exist for mail to flow into.

## Interaction rules

These rules override any habit of interviewing first.

1. **Discover before you ask.** Read the in-scope mail environment first (read-only) and answer your own questions from what you find. Ask the user only what discovery cannot resolve.
2. **Present findings before questions.** Open with a compact inventory of what exists today, then confirm scope. Never open with a questionnaire.
3. **Ask with numbered options.** Every question offers 2–4 numbered choices with a recommended default marked `(recommended)`. The user should be able to answer most turns with a single number. Reserve open-ended questions for facts only the user knows.
4. **Batch and bound.** At most 5 questions per message. Never re-ask anything discovery or the user already answered.
5. **Keep every message short.** Findings, options, and proposals fit on one screen. Detail belongs in the generated artifacts, not the conversation.

## Phase 1: Discover the current mail environment (read-only)

Before asking the user anything, inventory every mail resource the agent is authorized to read:

- All accessible mailboxes, shared mailboxes, and aliases.
- The complete folder tree, including subfolders, with per-folder message count, unread count, and oldest/newest message dates.
- Existing mail rules: what each matches and what it does; note rules that appear broken, overlapping, or inactive.
- Existing categories, labels, and their color assignments; how often each is actually applied.
- Flagged and pinned messages, and follow-up conventions in evident use.
- Volume profile: top senders and domains by count, share of newsletters and automated notifications, distribution-list traffic versus direct mail.
- Clutter profile: obvious archive candidates, stale threads, duplicate messages, large attachments, and old-date concentrations.

Take no action during discovery: no moves, labels, rule changes, unsubscribes, or deletions.

If any mailbox or folder is inaccessible, record it as out of scope rather than guessing at its contents.

## Phase 2: Present the inventory and confirm scope

Present a one-screen summary of what was found. For example: mailboxes discovered, folder-tree outline with counts, top ten senders by volume, newsletter share, rule and category status, and the clutter profile.

Then confirm scope with numbered choices:

1. Which discovered mailboxes are in scope? (Default: all listed.)
2. Are any folders protected — never reorganized, never cleaned? (Offer likely candidates found during discovery, such as folders named for legal, HR, personnel, contracts, or records.)
3. Do any retention, legal-hold, records-management, privacy, or organizational policies apply? (Only the user can answer this; if yes, capture the constraint before proceeding.)

## Phase 3: Establish intent with one question

Ask one numbered question:

> Based on what I found, what outcome do you want?
>
> 1. **Full reorganization (recommended)** — new folder structure, mail rules, color-coded categories, flagging conventions, then a records-safe cleanup, then optional recurring upkeep.
> 2. **Organize only** — structure, rules, categories, and flags; leave existing mail where it is.
> 3. **Cleanup only** — archive and remove clutter within the existing structure.
> 4. **Recurring maintenance only** — automate upkeep of the current structure without changing it.

Skip the phases below that the selected intent does not require.

## Phase 4: Propose the target structure

Design 2–3 candidate folder structures **from the observed traffic**, not from a generic template. Name real observed projects, organizations, and senders in each option. Typical shapes:

1. **Action-based** — Inbox is a working queue; folders such as `Action`, `Waiting`, `Reference`, `Archive/<year>`. Best when discovery shows high direct-mail volume and deadline-driven work.
2. **Project- or topic-based** — one folder per observed project, case, or workstream, plus `Reference` and `Archive`. Best when traffic clusters by topic.
3. **Sender- or organization-based** — folders per originating office, customer, or leadership chain. Best when traffic clusters by source.
4. **Keep and prune** — retain the current tree, merge near-empty and redundant folders found in discovery.

Present the options with a recommendation and the observed evidence for it, an estimate of migration effort for existing mail, and let the user pick by number or mix elements.

## Phase 5: Propose mail rules

From the volume profile, propose a concrete rule set that routes **future** mail into the chosen structure. For each proposed rule show: what it matches (real senders, domains, lists found in discovery), what it does, and roughly how many messages per week it would have handled recently.

Present rules in small numbered groups (newsletters, automated notifications, distribution lists, per-project routing, VIP senders) so the user can accept, edit, or drop each group by number.

Flag existing rules that conflict with the proposal and state whether each should be kept, merged, or retired.

## Phase 6: Propose categories and flags

Propose a color-coded category scheme aligned to the structure and the user's actual traffic — for example: red `Action required`, orange `Waiting on others`, blue `Reference`, purple `Leadership`, gray `Newsletter`. Reuse or remap the user's existing categories where discovery shows they are in real use.

Propose a flagging convention: what gets flagged, what due dates mean, and how flags interact with rules and folders (for example, rules may categorize automatically, but flags remain human-applied).

Present both as numbered accept/modify choices.

## Phase 7: Plan the cleanup

Only after structure, rules, and categories are settled, plan the cleanup of existing mail:

- Classify existing mail into: keep in place, refile into the new structure, archive candidate, newsletter/notification backlog, stale thread, duplicate, unsubscribe candidate, and possible-record.
- Present the plan as counts per proposed action with samples, and get approval **per action category**, not per message.
- Process in bounded batches with a preview of each batch before execution.

Safeguards (non-negotiable):

- Default to preview-only until the user approves each action category.
- Never delete material subject to retention, litigation hold, records policy, or unresolved business need; route possible-records to the user.
- Distinguish inbox removal (refile/archive) from deletion; prefer reversible actions and use archive, not delete, as the default disposition.
- Preserve thread context and attachments when refiling.
- Record every moved, archived, recategorized, unsubscribed, or deleted item in an audit log.
- Repeated runs must not reprocess an already-approved batch.

## Phase 8: Optional recurring maintenance automation

If the user wants ongoing upkeep, produce an automation specification:

```yaml
automation_name: "Inbox Maintenance"
automation_type: scheduled
schedule:
  plain_language: ""
  expression: ""
  timezone: ""
scope_mailboxes: []
protected_folders: []
maintenance_actions:
  apply_rules_to_missed_mail: ""
  refile_misfiled_mail: "approval_required"
  archive_older_than: ""
  newsletter_disposition: ""
  duplicate_handling: ""
  unsubscribe: "approval_required"
  delete: "disabled"
batch_limit_per_run: 0
preview_report_destination: ""
audit_log_destination: ""
```

Include an approval matrix (label/categorize, move/refile, archive, unsubscribe, delete), failure and retry behavior, a historical dry run in preview-only mode, and an activation checklist. Do not activate without explicit approval.

## Required output

Deliver, as artifacts separate from the conversation: the discovered-state inventory, approved target structure, rule set, category and flag scheme, cleanup plan with per-category approvals, audit log format, the maintenance automation specification (if selected), unresolved questions, dry-run findings, rollback plan, and activation checklist.
