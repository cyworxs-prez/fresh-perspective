# Skills

Reusable capability packages that teach an LLM or agent how to perform a class of work with consistent tradecraft, quality controls, and outputs.

A skill is broader than a single prompt. It defines the method, required inputs, assumptions, evidence standards, processing sequence, quality checks, and expected artifacts for a recurring category of work.

## When to use a skill

Use a skill when:

- the task requires more than a one-step prompt;
- quality depends on a repeatable analytical or writing method;
- multiple subskills must be sequenced or combined;
- the output needs consistent evidence, confidence, or reporting standards;
- the same capability should be reused across countries, organizations, projects, or users;
- a desktop agent should perform work in a controlled and auditable way.

## Day-to-day use

1. Open the collection README.
2. Complete the required scope or configuration profile.
3. Select the relevant subskills.
4. Provide the permitted source material and identify the system of record.
5. Run the skills in the recommended sequence.
6. Review assumptions, evidence, confidence, gaps, and quality checks.
7. Produce the final artifact using the reporting or writing skill.
8. Save reusable ledgers, templates, and validated outputs for future work.

A skill may be used manually, embedded in a larger prompt, or referenced by an automation. When used inside an automation, the runtime package should state which skill version it relies on.

## Required collection structure

```text
skills/<collection-name>/
  README.md
  <skill-name>/
    SKILL.md
  templates/
  examples/
```

Each collection README should explain:

- purpose and intended users;
- required scope or configuration;
- included skills;
- recommended execution sequence;
- inputs and source requirements;
- expected outputs;
- quality and safety controls;
- limitations and prohibited assumptions;
- day-to-day usage examples.

## Skill quality standard

Every skill should include:

- role and objective;
- activation criteria;
- required inputs;
- clarification questions;
- method and processing steps;
- source and evidence rules;
- output structure;
- confidence or quality language;
- stop conditions and limitations;
- related skills and templates.

## Current collection

- `influence-access-analysis/` — generalized, actor-neutral skills for area baselining, source tradecraft, environmental mapping, actor-network analysis, critical-node analysis, indicators and warning, analytic integration, and commander or executive reporting.