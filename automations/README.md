# Automations

Reusable specifications for scheduled, event-driven, and condition-based staff-work automation.

An automation describes how a workflow is invoked and executed by a model, agent, script, scheduler, or orchestration platform. It should be portable across cron, task schedulers, workflow engines, and agent runtimes.

## Automation types

- **Scheduled:** runs at a defined time or cadence.
- **Event-driven:** runs when a message, file, calendar event, form, or status change occurs.
- **Condition watch:** checks periodically and acts only when a defined condition becomes true.
- **Human-invoked:** starts from an explicit command but follows a standardized execution plan.

## Required automation sections

1. Name and objective
2. Automation type
3. Trigger or schedule
4. Time zone and business-calendar assumptions
5. Required connectors and permissions
6. Input scope and lookback window
7. Model or agent prompt
8. Deterministic processing steps
9. Human approval gates
10. Output destinations
11. Deduplication and idempotency rules
12. Logging and audit requirements
13. Failure, retry, and escalation behavior
14. Data sensitivity and retention controls
15. Test cases and acceptance criteria

## Scheduling guidance

Use standard cron only when the execution environment and time zone are explicit. Store a plain-language schedule beside every cron expression.

Example:

```yaml
schedule:
  type: cron
  expression: "0 7 * * 1-5"
  timezone: "America/New_York"
  description: "At 7:00 AM Eastern, Monday through Friday"
```

For recurring work that depends on a future condition, define the polling cadence separately from the notification condition.

## Safety model

Routine reading, classification, summarization, drafting, and record preparation may run automatically. Sending external messages, deleting records, changing authoritative data, accepting commitments, and other destructive or irreversible actions require an explicit approval gate unless the automation is narrowly authorized in advance.

## Initial staff-work automations

- `staff-work/inbox-triage.yaml`
- `staff-work/start-of-day-brief.yaml`
- `staff-work/end-of-day-report.yaml`
- `staff-work/quarterly-activity-report.yaml`
