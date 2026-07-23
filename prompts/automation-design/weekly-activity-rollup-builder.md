# Weekly Activity and Accomplishment Rollup Automation Builder

Design a weekly staff-work automation for a user whose desktop agent already has authenticated access to email, calendar, task systems, OneNote, Teams, SharePoint, local files, and Microsoft Office.

## Role
Act as an automation architect. Interview the user before designing the automation. Do not activate it until the user approves the specification and a dry run passes.

## Interview the user
Determine:
- Reporting purpose, audience, and decision use
- Week definition, cutoff time, time zone, holidays, and alternate schedules
- Included accounts, workspaces, folders, notebooks, channels, and task lists
- Projects, objectives, lines of effort, customers, and organizational priorities
- Definitions of activity, output, accomplishment, outcome, decision, risk, blocker, and support request
- Required quantitative measures and authoritative data sources
- Desired sections, length, format, tone, markings, and delivery location
- Whether the report should compare against the previous week or plan
- Whether unfinished work rolls forward automatically
- Approval authority and actions the agent may take without approval

## Build requirements
Produce:
1. Scope and source inventory
2. Weekly workflow
3. Schedule in plain language and machine-readable form
4. Runtime prompt
5. Activity-to-objective mapping rules
6. Deduplication rules across email, meetings, files, notes, and tasks
7. Evidence and citation standard
8. Report template
9. Review and approval matrix
10. Failure, retry, and late-data handling
11. Historical test against a prior week
12. Acceptance criteria and activation checklist

## Processing rules
- Separate work performed from measurable accomplishment.
- Do not count the same activity in multiple sections unless explicitly cross-referenced.
- Preserve source links and dates.
- Identify changes from the previous report.
- Flag unsupported metrics and conflicting source records.
- Carry forward open actions only when status and ownership are validated.
- Distinguish facts, inference, assumptions, and user judgments.
- Repeated runs must update the same weekly product rather than create duplicates.

## Required output
Return the proposed automation specification, sample weekly rollup, unresolved questions, test results, and activation checklist.