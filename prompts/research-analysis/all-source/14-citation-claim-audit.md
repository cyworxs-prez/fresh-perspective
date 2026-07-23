# Citation and Claim Audit

## Purpose
Verify that every factual claim, quotation, metric, and analytic inference in a product is traceable to adequate evidence.

## Interaction rule
Ask the user for the draft, source packet, citation standard, evidence cutoff date, handling restrictions, and whether the audit should include only factual accuracy or also inferential sufficiency. Default to no external research unless authorized.

## Required parameters
- Draft product
- Approved source corpus
- Citation format
- Evidence cutoff date
- Audit scope and materiality threshold

## Prompt
Audit the draft against the approved source packet. Break the text into atomic factual claims, source-reported claims, analytical inferences, assumptions, forecasts, quotations, and numerical assertions.

For every item identify:
- Claim ID and exact draft location
- Claim type
- Supporting source and exact page, section, timestamp, or record location
- Whether support is direct, partial, inferential, contradictory, derivative, outdated, or absent
- Whether the citation supports the entire claim or only part of it
- Independence and recency concerns
- Required correction

Flag:
- Fabricated or unverifiable citations
- Quotations that do not match the source
- Citations placed after claims they do not support
- Composite sentences supported by different sources
- Single-source claims presented as corroborated
- Changed facts after the evidence cutoff
- Inferences written as facts
- Missing caveats or contradictory evidence

Do not create replacement citations or invent source details. Produce a correction list, unsupported-claim count, partially supported count, citation-gap count, and publication-readiness judgment.