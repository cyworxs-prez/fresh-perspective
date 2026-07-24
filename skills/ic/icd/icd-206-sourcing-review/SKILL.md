---
name: icd-206-sourcing-review
summary: Assist a human analyst or reviewer in evaluating sourcing transparency, traceability, source descriptors, and source summaries for disseminated analytic products.
version: 0.1
maturity: draft
namespace: ic
human_role: analyst-or-reviewer
references:
  - ICD 206, Sourcing Requirements for Disseminated Analytic Products
  - ICS 206-01, public-source citation and reference guidance
  - ODNI Source Citations technical guidance
---

# ICD 206 Sourcing Review

## Purpose

Help a human analyst or reviewer assess whether a covered analytic product communicates the quality and scope of its underlying sources with sufficient transparency and traceability for the intended reader.

The model may map claims to sources, identify missing or weak sourcing, normalize citation fields, and draft source descriptors or summaries for analyst review. It does not invent sources, expose protected source details, determine classification, certify compliance, or approve dissemination.

## Required interview

Before reviewing, confirm:

- the product type, producing organization, and whether ICD 206 applies;
- applicable local sourcing, citation, retrieval, classification, disclosure, and product-line rules;
- whether ICS 206-01 or another implementation standard applies to publicly available, commercially available, or open-source material;
- the intended audience and their authorized access;
- the information cutoff and source universe used;
- whether source-identifying details may appear or protected descriptors are required;
- the source systems of record and retrieval conventions;
- who will adjudicate findings and approve the final sourcing treatment.

Request the draft product, source list, claim-and-evidence ledger, citation exports, source notes, and any existing source summary statement.

## Core principles

Sourcing should help the reader:

- understand the quality, credibility, scope, and limitations of the evidence;
- distinguish broad, diverse support from narrow or dependent reporting;
- retrieve or discover sources when authorized;
- evaluate how strongly the evidence supports key judgments;
- recognize important gaps, contradictions, and source constraints.

A citation count is not a source-quality assessment. Multiple derivative reports do not constitute independent corroboration.

## Review method

### Step 1: Confirm coverage and exceptions

Identify which product versions, sections, judgments, or source types are covered by the applicable sourcing policy. Record any authorized exception, waiver, or alternate presentation method. Do not infer an exception.

### Step 2: Build a claim-to-source map

For each material factual claim and key judgment, record:

```text
Claim or judgment ID:
Product location:
Source ID:
Source-reference citation:
Source descriptor:
Source-summary category:
Retrievable in authorized system: yes | no | unknown
Source date and information date:
Source type and origin:
Access, provenance, or methodology:
Quality and credibility considerations:
Independence group:
What the source supports:
What the source does not establish:
Corroborating sources:
Contradictory sources:
Handling or disclosure limitation:
Analyst adjudication:
```

Use local fields when required.

### Step 3: Review source-reference citations

Check whether citations:

- identify the source sufficiently for authorized discovery or retrieval;
- point to the correct source and relevant portion;
- use the required identifier, date, title, publisher, report number, URL, database field, or other metadata;
- remain stable enough for review and later retrieval;
- distinguish an original source from a derivative article, summary, or analytic product;
- avoid exposing protected source identities, methods, or relationships.

Do not create a plausible-looking citation when the source cannot be verified.

### Step 4: Review source descriptors

A descriptor should communicate material characteristics without exposing protected details. Depending on applicable rules, help the analyst describe:

- source type and origin;
- access or basis of knowledge;
- recency and proximity to the issue;
- methodology, sample, or data provenance;
- known strengths and limitations;
- possible bias, advocacy, incentives, or deception;
- whether reporting is direct, indirect, derivative, or aggregated.

Avoid boilerplate descriptors that imply quality without explaining it.

### Step 5: Review source-summary statements

Assess whether the product provides an accurate, concise overview of the evidence base. The summary should identify, as applicable:

- breadth and diversity of the source set;
- principal intelligence disciplines or source categories;
- the most important source strengths;
- material gaps, age, access, or representativeness limitations;
- dependence on a narrow source stream;
- contradictory reporting or significant source disagreement;
- whether key judgments rely predominantly on publicly or commercially available information;
- methodological or data constraints.

Do not imply comprehensive coverage when the accessible source universe is unknown.

### Step 6: Evaluate independence and corroboration

Group sources that derive from the same original information. Check for:

- press-release amplification;
- wire-service repetition;
- social-media recirculation;
- multiple analytic products citing the same report;
- commercial datasets that share an upstream provider;
- government statements repeated by aligned outlets;
- translations or summaries of the same original item.

Flag judgments whose apparent corroboration collapses after dependence is accounted for.

### Step 7: Evaluate source-to-judgment fit

For each key judgment, ask:

- Does the source directly support the proposition?
- Is an inferential step being hidden inside a citation?
- Is evidence of capability being used as evidence of intent?
- Is contact being used as proof of control or coordination?
- Is correlation being used as proof of causation?
- Is a contextual source being presented as diagnostic evidence?
- Is stale reporting being used for a current-status claim?

### Step 8: Normalize public and commercial source treatment

When applicable, use the current public implementation guidance to normalize citations for publicly available information, commercially available information, and open-source intelligence. Record:

- original publisher or creator;
- title or description;
- publication or observation date;
- access date where required;
- stable locator or authorized system identifier;
- version, edition, dataset, query, or methodology when material;
- archive or preservation status if links may change;
- licensing or contractual restrictions when relevant.

The analyst must confirm that use and retention comply with law, policy, contract, privacy, and civil-liberties requirements.

## Finding structure

```text
Finding ID:
Affected claim, judgment, citation, or source summary:
Issue type: missing | incorrect | unretrievable | weak descriptor | dependence | mismatch | disclosure risk | stale | other
Observed issue:
Why it matters:
Requirement type: directive | implementation standard | local rule | recommended tradecraft
Suggested analyst action:
Information needed to resolve:
Analyst adjudication:
Reviewer disposition:
```

## Required outputs

1. sourcing-coverage matrix;
2. claim-to-source map;
3. citation and retrieval exceptions;
4. source-dependence and corroboration findings;
5. draft source descriptors for analyst review;
6. draft source-summary statement;
7. unresolved sourcing risks and gaps;
8. analyst adjudication log.

## Quality-control checklist

- [ ] Applicability and local implementation were confirmed.
- [ ] Material claims and judgments are mapped to actual authorized sources.
- [ ] Citations support discovery or retrieval where authorized.
- [ ] Protected source details are not exposed.
- [ ] Descriptors explain source quality and limitations rather than merely labeling them.
- [ ] Derivative reporting is not counted as independent corroboration.
- [ ] Sources support the proposition for which they are cited.
- [ ] Stale, contradictory, narrow, or methodologically limited evidence is disclosed.
- [ ] The source-summary statement accurately represents the evidence base.
- [ ] No citation, source, descriptor, or retrieval status was fabricated.
- [ ] The human analyst or reviewer adjudicated all material findings.

## Stop conditions

Stop and ask the analyst when:

- ICD 206 applicability or the local implementation is unclear;
- a source cannot be retrieved or verified;
- required source metadata is unavailable;
- a descriptor could reveal protected identities, access, methods, or relationships;
- classification, disclosure, privacy, legal, or contractual rules are uncertain;
- the user asks the model to fabricate a citation or conceal a material source limitation;
- the source universe is too incomplete to support the product's sourcing claim.

## Human approval gate

The responsible analyst and authorized review chain must approve citations, descriptors, source-summary statements, exceptions, and disclosure treatment before dissemination.

## Public references

- https://www.odni.gov/files/documents/ICD/ICD-206.pdf
- https://www.odni.gov/index.php/who-we-are/organizations/ic-cio/ic-technical-specifications/source-citations

## Related assets

- `skills/shared/intelligence-tradecraft/evidence-and-claim-ledger/`
- `skills/ic/icd/icd-203-analytic-standards/`
- `templates/intelligence/evidence-claim-ledger.md`
- `prompts/ic/icd/icd-206-sourcing-reviewer.md`
