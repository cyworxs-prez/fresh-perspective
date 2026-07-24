# Skills

Reusable capability packages that help an LLM or agent support a human user with consistent methods, evidence standards, decision points, quality controls, and outputs.

A skill is broader than a single prompt. It defines the capability, required interview, inputs, assumptions, source boundaries, processing sequence, working artifacts, quality checks, stop conditions, and human approval gate for a recurring category of work.

## Human-led requirement

For analytic and planning work, the model supplements the trained analyst or planner. It does not become the accountable analyst.

Every substantive skill must:

- interview the user and confirm the task profile before processing evidence;
- use only authorized and identified information;
- prohibit fabricated sources, reporting, citations, doctrine, confidence, and judgments;
- preserve distinctions among reported information, source characterization, inference, assumption, judgment, likelihood, confidence, and implication;
- expose alternatives, contradictory evidence, uncertainty, and gaps;
- require human adjudication before finalization or consequential action.

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for the complete standard.

## When to use a skill

Use a skill when:

- the task requires more than a one-step prompt;
- quality depends on a repeatable analytical, planning, review, or writing method;
- multiple subskills must be sequenced or combined;
- the output needs consistent evidence, confidence, sourcing, or reporting standards;
- the capability should be reused across countries, organizations, missions, projects, or users;
- an agent should perform bounded staff work in a controlled and auditable way.

## Day-to-day use

1. Open the relevant namespace and collection README.
2. Run the required analyst interview and confirm the task profile.
3. Identify authorized sources, systems of record, information cutoff, and handling boundaries.
4. Select and sequence the relevant skills.
5. Create or update required working artifacts before polished prose.
6. Review evidence, dependencies, assumptions, alternatives, confidence, and gaps.
7. Apply applicable Joint, Service, IC, organizational, sourcing, and quality reviews.
8. Obtain human approval for judgments, confidence, indicators, markings, release, and dissemination.
9. Save approved ledgers, templates, and lessons for future updates.

A skill may be used manually, embedded in a prompt, called by another skill, or referenced by an automation. A prompt or runtime package should identify the skill version it implements.

## Namespace structure

Organize a skill by the community or doctrine that primarily governs the capability.

```text
skills/
  shared/
    intelligence-tradecraft/
      README.md
      <skill-name>/SKILL.md
  joint/
    intelligence/
      README.md
      <skill-name>/SKILL.md
  ic/
    icd/
      README.md
      <directive-or-skill-name>/SKILL.md
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
  <other-collection>/
```

Use `shared/` for methods that are substantially common across communities. Use Joint, IC, or Service namespaces when doctrine, terminology, workflow, authority, or required artifacts materially differ.

Do not create a top-level folder for every publication. Publication-specific implementation belongs under the governing namespace, such as `ic/icd/icd-203-analytic-standards/`.

## Required skill structure

Every skill folder contains `SKILL.md` with recommended front matter:

```yaml
---
name: stable-machine-readable-name
summary: One-sentence capability description.
version: 0.1
maturity: draft
namespace: shared | joint | ic | army | navy | marine-corps | air-force | space-force
human_role: analyst | planner | reviewer | manager
references:
  - applicable publication or policy
---
```

Every skill should include:

- purpose and intended human user;
- activation criteria and non-use cases;
- required interview and scope confirmation;
- required inputs and authorized-source boundaries;
- method, decision points, and working artifacts;
- source, evidence, and citation rules;
- uncertainty, alternatives, and confidence requirements where relevant;
- output structure;
- quality-control checks;
- stop conditions and escalation points;
- explicit human approval gate;
- applicable doctrine, policy, local-authority caveat, and limitations;
- related skills, prompts, templates, workflows, and tests.

## Current collections

- `shared/intelligence-tradecraft/` — analyst interview and scoping, evidence and claim ledgers, structured analytic technique facilitation, and assessment-language and confidence support.
- `joint/intelligence/` — JIPOE operational-environment, actor, capability, course-of-action, indicator, and gap support.
- `ic/icd/` — public ICD 203 analytic-standards and ICD 206 sourcing reviews.
- `influence-access-analysis/` — generalized, actor-neutral skills for baselining, source tradecraft, environmental mapping, actor-network analysis, critical-node analysis, indications and warning, integration, and executive reporting.

## Quality and maturity

Test at least normal, ambiguous, evidence-gap, contradictory, and authority-boundary cases. Declare each asset as draft, tested, operational, or reference. Local command, agency, product-line, classification, disclosure, legal, privacy, and supervisory requirements govern actual use.