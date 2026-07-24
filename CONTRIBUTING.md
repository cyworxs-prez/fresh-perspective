# Contributing to Fresh Perspective

Fresh Perspective is a human-led library of reusable AI skills, prompts, workflows, automations, templates, and reference material. Contributions must improve the work of an analyst, planner, researcher, or staff officer without representing the model as the accountable decision-maker.

## Non-negotiable design principles

### 1. Human analyst remains accountable

The model may organize evidence, surface inconsistencies, apply a defined method, propose alternatives, draft language, and perform quality checks. The human analyst owns:

- the intelligence question and decision context;
- source selection and access authorization;
- interpretation of evidence;
- assumptions and analytic judgments;
- confidence levels and estimative language;
- classification, handling, release, and dissemination decisions;
- final approval of every product.

No skill or prompt may claim that the model has independently completed an intelligence assessment.

### 2. Interview before substantive work

Every analytic skill and prompt must begin by confirming the task profile. At minimum, determine:

- mission or decision to support;
- intelligence question or planning problem;
- intended audience and required product;
- geographic, functional, actor, and temporal scope;
- operational environment and planning horizon;
- available evidence, repositories, and systems of record;
- classification, compartmentation, disclosure, privacy, and handling constraints;
- deadline, update cadence, and review authority.

Ask only the questions that materially affect the work, but do not silently invent missing scope. Restate the agreed scope before processing evidence.

### 3. Evidence before assessment

A contribution must prohibit fabricated reporting, citations, quotations, source descriptions, collection results, doctrine, confidence, and analytic judgments. Unknowns must remain unknown. When evidence is missing or inaccessible, the output must state the limitation and identify the resulting collection or research gap.

Models must distinguish:

- reported or observed information;
- source characterization;
- analytic inference;
- explicit assumption;
- alternative explanation;
- judgment;
- confidence;
- implication or planning consideration.

### 4. Traceability is required

Material claims and judgments must be traceable to analyst-provided or explicitly retrieved evidence. Skills should create or update a claim-and-evidence ledger when the task is sufficiently complex. A citation may show where information came from, but it does not by itself establish source quality, independence, credibility, or relevance.

### 5. Doctrine informs; local authority governs

Public doctrine and Intelligence Community policy may be used as a methodological baseline. Contributions must distinguish:

- **mandatory policy or local production requirements**;
- **authoritative doctrine**;
- **recommended tradecraft**;
- **repository conventions**.

The current publication, command or agency standard operating procedure, product-line guide, security classification guide, foreign disclosure authority, records policy, and supervisory direction take precedence over repository defaults.

### 6. No unauthorized collection or access

A skill may work only with information and systems the user is authorized to access. It may not direct the user or model to bypass access controls, retrieve unavailable classified material, defeat monitoring, conceal activity, or use personal or commercially available information contrary to law, policy, contract, or approved purpose.

### 7. Consequential actions require approval

Prompts and automations must identify actions that require human approval. Sending, publishing, disseminating, tasking collection, changing authoritative records, assigning formal confidence, applying classification or release markings, making policy recommendations, or committing an organization must not occur automatically unless an approved workflow explicitly authorizes it.

## Repository namespaces

Organize reusable assets by the community or doctrine that primarily governs the capability.

```text
skills/
  shared/
  joint/
    intelligence/
  ic/
    icd/
  army/
    intelligence/
  navy/
    intelligence/
  marine-corps/
    intelligence/
  air-force/
    intelligence/
  space-force/
    intelligence/
  functional/
    <methodology-collection>/

prompts/
  shared/
  joint/
    intelligence/
  ic/
    icd/
  <service>/intelligence/
  functional/
    <methodology-collection>/
```

Use `shared/` for methods that are substantially common across communities, such as evidence ledgers, structured analytic techniques, assumption checks, confidence support, and analytic writing. Place a service- or joint-specific implementation in its own namespace when doctrine, terminology, workflow, or required artifact materially differs.

Use `functional/` for methodology collections that apply across communities and are not owned by any one doctrine or service — for example influence and access analysis, homeland indicators and warning, or generalized all-source research. A collection belongs in a community namespace when a specific community's doctrine or policy governs it; it belongs in `functional/` when the method itself is the organizing principle.

Do not create a top-level folder for each publication. Place publication-specific implementation under the relevant namespace, such as `skills/ic/icd/icd-203-analytic-standards/`.

## Required skill structure

Each skill folder must contain `SKILL.md`. Recommended front matter:

```yaml
---
name: stable-machine-readable-name
summary: One-sentence capability description.
version: 0.1
maturity: draft
namespace: shared | joint | ic | army | navy | marine-corps | air-force | space-force | functional
human_role: analyst | planner | reviewer | manager
references:
  - publication or policy title
---
```

Every `SKILL.md` must include:

1. purpose and intended human user;
2. activation criteria and non-use cases;
3. mandatory interview and scope confirmation;
4. required inputs and authorized source boundaries;
5. method, decision points, and working artifacts;
6. source, evidence, and citation rules;
7. uncertainty, confidence, and alternative-analysis requirements where relevant;
8. output structure;
9. quality-control checks;
10. stop conditions and escalation points;
11. explicit human review and approval gate;
12. applicable doctrine, policy, and limitations;
13. related skills, prompts, templates, and workflows.

## Required prompt structure

Every reusable analytic prompt must:

- identify the model as an assistant to the human analyst;
- conduct an interview before substantive analysis;
- confirm the final task profile with the user;
- state that it cannot invent evidence or sources;
- use only authorized, identified information;
- preserve fact, inference, assumption, judgment, and confidence distinctions;
- expose gaps, conflicting reporting, and alternative explanations;
- produce working artifacts before polished prose when appropriate;
- include a human approval gate;
- identify the skill and version it implements.

A prompt should not contain hidden mission assumptions, actors, locations, desired conclusions, confidence levels, or dissemination permissions.

### Companion prompts are thin executors

A prompt that implements a skill must not restate the skill's method, schemas, or checklists. It carries only: the `**Implements:**` header naming the skill and version, the model-role framing, a directive to load and follow the skill file for the method, any runtime-specific behavior the skill does not contain, a brief output summary, and the stop-and-approval gate. This keeps one source of truth per capability — edits land in the skill, not in two places. Only standalone prompts with no governing skill (for example the all-source research sequence) carry their full method inline.

## Quality and test requirements

Before merging a new or materially revised asset, test at least:

1. **Normal case:** sufficient evidence and clearly defined scope.
2. **Ambiguous case:** incomplete task definition that should trigger interview questions.
3. **Evidence-gap case:** insufficient or inaccessible sources that must not be fabricated.
4. **Contradictory case:** credible reporting supports competing explanations.
5. **Boundary case:** the user requests an action outside authority, policy, or classification limits.

Record expected behavior. A passing asset should preserve uncertainty, stop when necessary, and require human approval rather than forcing a complete-looking answer.

## Public-source doctrine baseline

The repository may reference publicly releasable doctrine and policy, including applicable Joint Publications, Service doctrine, Intelligence Community Directives, Intelligence Community Standards, and official implementation guidance. Contributors must verify the current public version before asserting a publication date, mandatory requirement, or exact doctrinal sequence.

Draft doctrine is not authoritative. Restricted or classified guidance must not be copied into this public repository.

## Review checklist

Before submission, confirm:

- [ ] The asset supplements rather than replaces the human analyst.
- [ ] The user is interviewed and the scope is confirmed.
- [ ] No source, citation, fact, confidence level, or doctrine can be fabricated.
- [ ] Facts, assumptions, inferences, judgments, and alternatives remain distinct.
- [ ] Evidence and judgments are traceable.
- [ ] Current and local authority takes precedence over repository defaults.
- [ ] Security, privacy, disclosure, and access boundaries are explicit.
- [ ] Human approval is required before finalization or consequential action.
- [ ] Normal, ambiguous, gap, contradictory, and boundary cases were considered.
- [ ] Related skills, prompts, templates, workflows, and references are linked.
