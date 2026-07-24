# Approval Matrix — Inbox Maintenance

| Action | Default authority | Configured in automation.yaml | Audit requirement |
|---|---|---|---|
| Read and inventory mailboxes | automatic | scope.mailboxes | log run timestamp and scope |
| Apply approved rules to missed mail | automatic | maintenance_actions.apply_rules_to_missed_mail | log item, rule, before/after folder |
| Refile misfiled mail | approval required | maintenance_actions.refile_misfiled_mail | log item and before/after state |
| Archive items past threshold | per configuration | maintenance_actions.archive_older_than | log item, age, destination |
| Move newsletters per disposition | per configuration | maintenance_actions.newsletter_disposition | log item and destination |
| Report duplicates | automatic (report only) | maintenance_actions.duplicate_handling | list in summary |
| Unsubscribe | approval required, per sender | maintenance_actions.unsubscribe | record sender and user approval |
| Delete or trash | disabled | maintenance_actions.delete | n/a — requires design change and re-approval |
| Touch protected folders or possible-records | never automatic | scope.protected_folders, scope.policy_constraints | queue untouched with reason |
| Change rules, categories, schedule, or scope | never automatic | — | workflow approval gate and package re-approval |
| Send mail on the user's behalf | never | — | n/a |

Escalation: anything not covered by a row above is treated as approval-required and queued with an explanation in the run summary.
