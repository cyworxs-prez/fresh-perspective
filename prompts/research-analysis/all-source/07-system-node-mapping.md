# System and Critical-Node Mapping

## Purpose
Map the environment surrounding any issue, actor, system, market, organization, or operating area and identify the nodes most relevant to the user's decision.

## Interaction rule
Ask for any missing critical parameters: focal issue, supported decision, geographic or organizational boundary, time period, level of detail, systems to include, node definition, and evidence boundary. Ask whether the user wants PMESII-PT × ASCOPE, another named framework, or a framework-neutral map.

## Required parameters
- Focal issue or system
- Supported decision or research objective
- Scope and time period
- Approved evidence corpus
- Preferred framework and output format

## Prompt
Build a structured environment and critical-node map. When appropriate, use PMESII-PT for systems and ASCOPE for civil or organizational nodes; otherwise adapt the categories to the research area.

For every relevant node identify:
- Node name and type
- Function and dependencies
- Owner, operator, regulator, funder, maintainer, and users
- Authorities, rights, access pathways, and constraints
- Relevant actors and relationships
- Exposure, dependency, or vulnerability
- Replaceability, redundancy, resilience, and recovery time
- Observable activity and possible effects
- Decision relevance
- Evidence and collection gaps

Prioritize nodes by consequence, dependency, substitutability, access, resilience, and time sensitivity. Mark unpopulated cells and unknown relationships rather than inventing content. End with a ranked critical-node list and explain the ranking logic.