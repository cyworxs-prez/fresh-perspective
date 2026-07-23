# Prompts

Model-ready instructions for bounded tasks, guided interviews, configuration sessions, and reusable interactions with an LLM or desktop agent.

Prompts are design-time or task-time assets. They may help a user perform work directly, or they may help design a workflow and automation. A prompt is not automatically an approved operating procedure and should not be treated as an active automation unless it has been reviewed, tested, and translated into the appropriate runtime artifact.

## Prompt types

- **Task prompt:** directs a model to perform a bounded task.
- **Builder prompt:** interviews the user and generates a proposed workflow, configuration, or automation.
- **Reviewer prompt:** evaluates an artifact against defined standards.
- **Transformation prompt:** converts an input into a required format or structure.
- **Runtime prompt:** governs the model behavior inside an approved automation. Runtime prompts should be stored with the automation package once deployed.

## Day-to-day use

1. Select the prompt that matches the desired task.
2. Read its assumptions, required inputs, and authority boundaries.
3. Provide the model or agent with the requested context and permitted source access.
4. Answer clarification questions rather than allowing the model to invent material preferences or permissions.
5. Review the resulting artifact, assumptions, and unresolved choices.
6. Save durable outputs in the correct location:
   - reusable capability guidance under `skills/`;
   - approved operating procedures under `workflows/`;
   - tested runtime configurations under `automations/`;
   - reusable schemas and forms under `templates/`.
7. Do not activate recurring or consequential behavior directly from a draft builder prompt.

## Builder-prompt lifecycle

A builder prompt should:

1. Explain the intended outcome.
2. Interview the user in manageable sections.
3. Inspect only user-approved resources.
4. Define scope, exclusions, schedule, systems of record, and output requirements.
5. Establish automatic actions and approval-required actions.
6. Generate a plain-language workflow.
7. Generate a machine-readable or platform-translatable automation specification.
8. Produce test cases, acceptance criteria, and rollback instructions.
9. Require explicit approval before activation.

The approved workflow should be committed under `workflows/`. The tested runtime package should be committed under `automations/`.

## Prompt quality standard

Every reusable prompt should identify:

- role and objective;
- required inputs;
- questions to ask when information is missing;
- authoritative sources or systems of record;
- assumptions and prohibited assumptions;
- processing steps;
- output structure;
- quality checks;
- permissions and approval boundaries;
- failure and stop conditions;
- related skills, workflows, templates, or automations.

## Current collection

- `automation-design/` — interview-first builder prompts for recurring staff work on an already authenticated desktop agent or LLM environment.