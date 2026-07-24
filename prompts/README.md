# Prompts

Model-ready instructions for bounded tasks, guided interviews, configuration sessions, diagnostic reviews, and reusable interactions with an LLM or desktop agent.

Prompts are design-time or task-time assets. They may help a human perform work directly or help design a workflow and automation. A prompt is not automatically an approved operating procedure and must not be treated as an active automation unless it has been reviewed, tested, and translated into the appropriate runtime artifact.

## Human-led analytic requirement

For intelligence analysis and planning, the prompt must position the model as an assistant to a trained human analyst, planner, or reviewer. It must not represent the model as the accountable analyst.

Every substantive analytic prompt must:

- interview the user before beginning substantive work;
- confirm the mission or decision, intelligence question, consumer, scope, timeframe, actors, authorized source set, information cutoff, handling constraints, deliverable, and approval authority;
- prohibit fabricated reporting, sources, citations, doctrine, collection, confidence, and judgments;
- distinguish reported information, source characterization, inference, assumption, judgment, likelihood, confidence, and implication;
- expose contradictory evidence, plausible alternatives, uncertainty, and gaps;
- identify actions and conclusions requiring human adjudication;
- require explicit human approval before finalization, release, dissemination, tasking, or other consequential action.

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for the complete standard.

## Prompt types

- **Task prompt:** guides a bounded analyst-assistance task.
- **Builder prompt:** interviews the user and generates a proposed workflow, configuration, or automation.
- **Reviewer prompt:** evaluates an artifact against defined doctrine, policy, tradecraft, or local standards.
- **Transformation prompt:** converts authorized input into a required format without changing the underlying judgment.
- **Facilitator prompt:** supports a structured analytic technique or collaborative review while preserving human adjudication.
- **Runtime prompt:** governs model behavior inside an approved automation. Once deployed, runtime prompts belong with the automation package.

## Namespace structure

The top-level folder identifies the asset as a prompt. Subfolders identify the governing community, doctrine, service, or shared methodology.

```text
prompts/
  shared/
    intelligence-tradecraft/
      README.md
      <prompt>.md
  joint/
    intelligence/
      README.md
      <prompt>.md
  ic/
    icd/
      README.md
      <prompt>.md
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
  automation-design/
  <other-domain-or-function>/
```

Use `shared/` for methods that are substantially common across communities. Use Joint, IC, or Service namespaces when doctrine, terminology, workflow, authority, or required artifacts materially differ. Publication-specific prompts belong under the governing namespace, such as `prompts/ic/icd/icd-203-product-reviewer.md`.

## Day-to-day analytic use

1. Select the prompt that matches the approved task or review requirement.
2. Read its role, assumptions, inputs, source boundaries, and stop conditions.
3. Complete the required interview and confirm the task profile.
4. Provide only authorized sources or explicitly authorize retrieval from identified systems.
5. Review intermediate working artifacts before requesting polished prose.
6. Adjudicate assumptions, source characterizations, alternatives, gaps, likelihood, and confidence.
7. Apply applicable Joint, Service, IC, organizational, classification, disclosure, and product-line reviews.
8. Save durable outputs in the correct location:
   - reusable capability guidance under `skills/`;
   - approved operating procedures under `workflows/`;
   - tested runtime configurations under `automations/`;
   - reusable schemas and forms under `templates/`.
9. Do not activate recurring or consequential behavior directly from a draft prompt.

## Builder-prompt lifecycle

A builder prompt should:

1. Explain the intended outcome and the model's supporting role.
2. Interview the user in manageable sections.
3. Inspect only user-approved resources.
4. Define scope, exclusions, schedule, systems of record, output requirements, and information cutoff.
5. Establish automatic actions and approval-required actions.
6. Generate a plain-language workflow.
7. Generate a machine-readable or platform-translatable automation specification.
8. Produce test cases, acceptance criteria, failure handling, disable, and rollback instructions.
9. Require explicit approval before activation.

The approved workflow belongs under `workflows/`. The tested runtime package belongs under `automations/`.

## Prompt quality standard

Every reusable prompt should identify:

- the model's supporting role and the human accountable role;
- the skill and version implemented, when applicable;
- required interview and scope confirmation;
- required inputs and authorized source boundaries;
- authoritative doctrine, policy, or systems of record;
- assumptions and prohibited assumptions;
- processing steps and working artifacts;
- output structure;
- source, evidence, uncertainty, and quality checks;
- permissions and approval boundaries;
- failure, stop, and escalation conditions;
- related skills, workflows, templates, automations, and tests.

Analytic prompts should be tested against normal, ambiguous, evidence-gap, contradictory, and authority-boundary cases.

## Current collections

- `shared/intelligence-tradecraft/` — interview and scoping, evidence ledgers, structured analytic technique facilitation, and key-judgment drafting.
- `joint/intelligence/` — JIPOE operational-environment and actor/course-of-action support.
- `ic/icd/` — ICD 203 analytic-standards and ICD 206 sourcing review prompts.
- `automation-design/` — discovery-first builder prompts for recurring staff work on an already authenticated desktop agent or LLM environment.