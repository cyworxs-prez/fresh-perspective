# Army Intelligence Prompts

Thin executor prompts for the Army IPB skills under `skills/army/intelligence/`. Each prompt identifies the skill and version it implements, frames the model as an assistant to a trained Army intelligence analyst or planner, and defers to the skill file for the interview, method, quality checks, and stop conditions.

## Prompts

Run in IPB order:

1. `ipb-define-operational-environment.md` — implements `skills/army/intelligence/ipb-define-operational-environment/`.
2. `ipb-describe-environmental-effects.md` — implements `skills/army/intelligence/ipb-describe-environmental-effects/`.
3. `ipb-evaluate-threat.md` — implements `skills/army/intelligence/ipb-evaluate-threat/`.
4. `ipb-determine-threat-courses-of-action.md` — implements `skills/army/intelligence/ipb-determine-threat-courses-of-action/`.

## Usage

1. Start with `prompts/shared/intelligence-tradecraft/interview-and-scope.md` if no confirmed task profile exists.
2. Each step's output is the next step's input; do not skip the human approval gate between steps.
3. Later steps must trace their scope back to the approved step-one environment definition.
4. Local command standard operating procedures, product-line guidance, and classification rules govern over these defaults.

Related working artifacts: `templates/intelligence/analysis-profile.md`, `templates/intelligence/evidence-claim-ledger.md`.
