---
name: intelligence-requirements-and-collection-support
summary: Help a human analyst convert validated gaps into candidate PIRs, EEIs, SIRs, RFIs, and a tracked collection-support matrix without tasking collection.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst-or-collection-manager
references:
  - Joint Publication 2-0, Joint Intelligence
  - Joint Publication 2-01, Joint and National Intelligence Support to Military Operations
  - ATP 2-01, Plan Requirements and Assess Collection
---

# Intelligence Requirements and Collection Support

## Purpose

Help a human analyst or collection manager run the requirement lifecycle that the library's analytic skills feed: consolidate information gaps from working artifacts, draft candidate priority intelligence requirements and supporting requirements, decompose them into observable elements, prepare requests for information, and track status through to assessment.

The model drafts and organizes candidates. It does not validate requirements, set priorities, task collection, commit collection resources, or represent any candidate as approved or tasked. Those authorities belong to the command or organization's requirements-management process.

## Activation criteria

Use when a confirmed task profile has produced information gaps that need to become managed requirements: after JIPOE or IPB gap identification, after an evidence ledger exposes unanswerable claims, after indicators-and-warning development, or when an existing requirement set needs consolidation, refresh, or status review.

## Non-use cases

Do not use as a substitute for:

- the organization's formal requirements-validation and prioritization board or process;
- collection-management authority, tasking systems, or sensor allocation;
- the indicators-and-warning skills, which design indicators (this skill manages the requirements they generate);
- source-evaluation skills, which assess evidence already in hand.

## Mandatory interview

Confirm before drafting:

- supported command or organization, decisions, and decision timeline;
- the upstream working artifacts supplying gaps (ledger, JIPOE/IPB products, indicator registers);
- the existing requirement set, if any, and its system of record;
- the organization's requirement terminology, formats, and validation process;
- available request channels and their authorities (RFI, production request, collection request);
- classification, handling, and dissemination constraints for requirement text;
- update cadence, aging thresholds, and who adjudicates status;
- the approving authority for anything leaving the working set.

Restate the confirmed configuration before drafting.

## Required inputs

- gap registers or working artifacts from upstream skills, with source links;
- the decisions each gap ultimately supports;
- existing requirements and their status, when a set exists;
- organizational formats and validation rules, when defined.

## Method

1. **Consolidate gaps.** Collect gaps from the identified artifacts; merge duplicates; preserve each gap's origin, decision linkage, and gap type (collection, access, processing, exploitation, translation, research, coordination).
2. **Screen for requirement fitness.** A gap becomes a candidate requirement only if answering it changes a decision. Route research-answerable gaps to research, not collection.
3. **Draft candidate PIRs and IRs.** Each candidate must be decision-linked, answerable, time-bounded, and behavior- or condition-specific — the same standard the indicators-and-warning skills apply. Record the decision, latest-time-of-value, and originating gap for each.
4. **Decompose into EEIs and SIRs.** Break each candidate into observable elements: what to observe, where, when, expected signature, and what a positive or negative observation would establish.
5. **Draft requests.** Where the answer lies outside local holdings, draft RFI text using `templates/intelligence/rfi-register.md`: question, context, decision supported, latest time of value, requested format, and handling. Mark every draft as unsubmitted candidate text.
6. **Build the collection-support matrix.** Populate `templates/intelligence/collection-requirements-matrix.md`: requirement → elements → candidate source class or discipline → owning organization → status → aging.
7. **Track and age.** On each update cycle, refresh status, flag requirements approaching or past their latest time of value, flag answered requirements for closure, and flag unanswered aging requirements for re-validation or escalation — all as recommendations to the human owner.
8. **Feed back.** When reporting answers a requirement, record what was answered, at what confidence, and what residue remains; return the residue to the gap register.

## Source and evidence rules

- Every requirement traces to a real gap in a real working artifact — do not invent gaps or requirements to fill a matrix.
- Do not fabricate collection capabilities, source availability, organizational ownership, or submission channels; where unknown, mark unknown.
- Requirement text must not embed unproven premises about the actor or outcome.

## Uncertainty and alternatives

Where a gap could be answered by multiple approaches (research versus request versus new observation), present the options with cost and latency trade-offs rather than selecting one. Record disagreement about a requirement's priority as a note for the validation authority, not a resolved ranking.

## Output

- consolidated gap register with origins and decision links;
- candidate PIR/IR set with decomposed EEIs/SIRs;
- draft RFI texts, marked unsubmitted;
- collection-support matrix with status and aging;
- closure and escalation recommendations;
- items requiring validation-authority decision.

## Quality-control checklist

- [ ] Every requirement links to a decision and an originating gap.
- [ ] Candidates are answerable and time-bounded, with latest time of value stated.
- [ ] Research-answerable gaps were not converted into collection requirements.
- [ ] No candidate is represented as validated, prioritized, or tasked.
- [ ] Draft RFIs are marked unsubmitted and carry handling notes.
- [ ] Aging and closure recommendations are visible with rationale.

## Stop conditions

Stop and ask the analyst when the supported decisions cannot be identified; when the organization's validation process or terminology is unknown and would change the draft; when the user asks the model to submit, task, or prioritize; or when requirement text would require classification or handling decisions the model must not make.

## Human approval gate

The human analyst or collection manager approves the candidate set before it enters any validation process, and the organization's requirements authority validates, prioritizes, and tasks. Nothing in this skill's output is actionable until then.

## Doctrine and limitations

JP 2-0/2-01 and ATP 2-01 provide the methodological baseline; the current command or agency requirements-management SOP, tasking authorities, and product-line rules govern over these defaults.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/functional/influence-access-analysis/indicators-warning/`
- `skills/functional/homeland-indicators-warning/homeland-strategic-warning/`
- `templates/intelligence/collection-requirements-matrix.md`
- `templates/intelligence/rfi-register.md`
- `prompts/shared/intelligence-tradecraft/manage-requirements-and-collection-support.md`
