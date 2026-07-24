---
name: public-source-evaluation
summary: Evaluate publicly and commercially available sources — hierarchy, decomposition, ratings, independence, deception screening, revalidation, and corroboration — for any analytic task.
version: 0.1
maturity: draft
namespace: shared
human_role: analyst
references:
  - ICD 206, Sourcing Requirements for Disseminated Analytic Products
  - ICS 206-01, public-source citation and reference guidance
---

# Public Source Evaluation

## Purpose

Give any analytic task a disciplined method for evaluating publicly and commercially available information: what class of source it is, what it actually proves, how reliable and credible it is, whether apparent corroboration is real, whether the source may be deceptive or agenda-driven, and whether it is still current.

The model applies the method and proposes assessments. The human analyst owns final source ratings, corroboration status, and every judgment built on the evidence.

## Activation criteria

Use whenever an analytic task ingests open or commercial sources — during evidence-ledger construction, source extraction, standing-assessment updates, or review of a draft's public sourcing.

## Non-use cases

Do not use as a substitute for:

- the evidence-and-claim-ledger skill, which defines the ledger this method feeds;
- ICD 206 sourcing review of a finished product;
- classified or controlled source-handling processes;
- authorization to collect — this skill evaluates material the user lawfully holds or may lawfully retrieve.

## Mandatory interview

Confirm: the task profile and question the evidence supports; the authorized source set and retrieval permissions; the organization's source-rating scheme (propose the neutral A–F / 1–6 scheme only if none is mandated, and get approval); citation and retrieval requirements; the information cutoff; and handling constraints on source descriptions.

## Required inputs

The candidate sources or retrieval authorization, the claims they are offered to support, and any existing ledger rows they extend.

## Method

1. **Classify by source hierarchy.** Prefer, in order: primary official records (laws, gazettes, regulators, registries, courts, procurement portals); the subject actor's own official output; other governments' and multilateral official sources; audited filings and disclosure documents; peer-reviewed research and established institutions; reputable journalism; specialist databases and commercial providers; social media and unattributed claims as leads only, never as sole support.
2. **Decompose what the evidence establishes.** Record separately whether it establishes contact, relationship, payment or contract, ownership or control, access, intent, activation, or effect. These are not interchangeable, and a source proving one does not prove the next.
3. **Rate.** Propose source reliability (A–F) and information credibility (1–6), with rationale, for analyst review. A rating is a proposal until adjudicated.
4. **Test independence.** Assign every item an independence group; reports deriving from the same press release, briefing, anonymous source, dataset, wire article, or recirculated post share a group, and repetition within a group is never corroboration.
5. **Screen for deception and agenda.** For every critical source assess access, incentives, advocacy, intended audience effect, alternative explanations for publication, and whether the disclosure itself could be an influence action.
6. **Revalidate currency.** Immediately before any release, re-check officeholders, leadership, ownership, contracts, project and operating status, legal authorities, and dates.
7. **Apply the corroboration minimum.** For high-impact claims: one primary source plus one independent corroborating source, or two independent high-quality sources with distinct access. If unmet, lower the proposed confidence contribution and state the collection or research gap.

## Source and evidence rules

Never fabricate a source, citation, rating, access description, or corroboration. Record what each source does not establish alongside what it does. Preserve original wording separately from summaries.

## Uncertainty and alternatives

Where sources conflict, keep both in the ledger with their independence groups and present the conflict; do not resolve it by rating alone. Where a single source class dominates, say so as a structural limitation.

## Output

Rated, decomposed, independence-grouped ledger rows; the deception-screen notes for critical sources; the revalidation record; and the corroboration shortfalls with their resulting gaps.

## Quality-control checklist

- [ ] Every material claim's source has class, ratings, and an independence group.
- [ ] What each source does not establish is recorded.
- [ ] No corroboration counted within an independence group.
- [ ] Critical sources passed (or failed visibly) the deception screen.
- [ ] Currency revalidation ran before release.
- [ ] Unmet corroboration minimums lowered confidence and produced a stated gap.

## Stop conditions

Stop and ask the analyst when a required source is unavailable or unauthorized; when the user asks the model to upgrade, invent, or launder sourcing; when a critical source fails the deception screen with no independent alternative; or when source descriptions would expose protected or restricted information.

## Human approval gate

The human analyst adjudicates ratings, independence groupings, corroboration status, and deception-screen conclusions before any judgment relies on them.

## Doctrine and limitations

ICD 206 and ICS 206-01 provide the public baseline for sourcing transparency; the organization's own source-evaluation scheme, citation rules, and handling policies govern where they differ.

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/ic/icd/icd-206-sourcing-review/`
- `skills/functional/influence-access-analysis/source-tradecraft/`
- `templates/intelligence/evidence-claim-ledger.md`
- `prompts/shared/intelligence-tradecraft/evaluate-public-sources.md`
- `prompts/functional/research-analysis/all-source/03-source-extraction.md`
