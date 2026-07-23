# Baseline Scoring Model

Configure the actor and area labels before scoring. Scores support prioritization; they do not replace analytic judgment.

Score each issue from 0 to 4.

| Dimension | 0 | 2 | 4 |
|---|---|---|---|
| Target-actor access | No meaningful access | Indirect, intermittent, or limited access | Persistent, privileged, or embedded access |
| Leverage | No identifiable leverage | Moderate dependency, inducement, or bargaining power | Strong coercive, financial, political, informational, technical, or institutional leverage |
| Intent evidence | No evidence | Inferred from pattern or incentives | Clear tasking, signaling, coordination, or repeated purposeful behavior |
| Activation | Dormant or latent | Preparatory, testing, or limited use | Active pressure, exploitation, mobilization, or denial |
| Local or partner vulnerability | Strong safeguards and alternatives | Mixed safeguards or partial dependency | Weak safeguards, concentrated dependency, or high exposure |
| Operational or decision relevance | No material effect | Secondary requirement affected | Key decision, capability, or requirement may be denied or critically delayed |
| Immediacy | Long-term structural condition | Within the planning horizon | Active or likely in the current decision window |
| Reversibility | Easily mitigated | Requires time, coordination, or resources | Difficult to reverse before or during the relevant contingency |

## Optional weighted risk score

Use only as a prioritization aid and adjust weights to the mission:

- Operational or decision relevance: 25%
- Local or partner vulnerability: 15%
- Leverage: 15%
- Activation: 15%
- Immediacy: 10%
- Reversibility: 10%
- Target-actor access: 5%
- Intent evidence: 5%

Convert the weighted average from 0–4 to 0–100 by multiplying by 25.

Confidence remains separate:

- **High:** strong, consistent, recent, independently corroborated evidence; limited sensitivity to assumptions.
- **Moderate:** credible but incomplete or partially inferential evidence; some sensitivity to assumptions.
- **Low:** fragmentary, conflicting, dated, weakly corroborated, or highly assumption-sensitive evidence.
