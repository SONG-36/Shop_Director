---
name: market-user-research-skill
description: Create or review ShopDirector AI market and user research artifacts when the task is to define ICPs, user roles, pain points, decision chains, use cases, competitor patterns, or evidence-backed positioning inputs for docs/product_design. Use for 01_product_positioning.md, 02_market_and_user.md, and 03_business_model.md. This skill informs the Decision Intelligence Kernel and does not make final product decisions on its own.
---

# Market & User Research Skill

Use this skill to translate market and user signals into structured product-design inputs for ShopDirector AI.

## Kernel relationship

This skill feeds the Decision Intelligence Kernel:
- market understanding
- consumer understanding
- platform and growth context
- decision bottleneck discovery

It informs the Kernel. It does not define final strategy on its own.

## Supported documents

- `docs/product_design/01_product_positioning.md`
- `docs/product_design/02_market_and_user.md`
- `docs/product_design/03_business_model.md`

## Use when

Use this skill when the task is to:
- define ICPs or merchant segments
- map user roles and decision chains
- cluster pain points, unmet needs, or workflow friction
- compare competitor messaging or category patterns
- ground positioning or pricing assumptions in evidence

Do not use this skill for product architecture, direct content generation, or final review.

## Required inputs

- research question or document goal
- known market hypotheses
- draft positioning or business assumptions
- internal notes, interviews, feedback, or competitor observations
- any available segment constraints or regional context

## Workflow

1. Clarify the research objective and the decision the document must support.
2. Identify the relevant entities:
   - market segments
   - ICPs
   - user roles
   - decision-makers
   - competitors
3. Separate evidence from inference.
4. Normalize signals into structured groups:
   - pain points
   - goals
   - blockers
   - buying triggers
   - decision risks
5. Convert findings into product-design implications.
6. Flag weak evidence, missing validation, and assumptions that need human confirmation.

## Output contract

Produce advisory outputs such as:
- ICP definitions
- user-role map
- pain-point clusters
- decision-chain analysis
- competitor and messaging comparison
- product implications for positioning and value logic

## Review standard

Before considering the output usable, check:
- Are claims grounded and scoped?
- Does the output identify real decision bottlenecks instead of generic personas?
- Does the research help the Kernel decide where strategy should focus?
- Are evidence and inference clearly separated?

## Limitations

- no outreach generation
- no CRM or sales-ops output
- no browser scraping assumptions
- no live ad extraction assumptions
- no screenshots, Slack, Notion, MCP, API, shell, or code-execution assumptions by default

## Risk level

Medium

## Human approval requirements

Human approval is required before:
- external market claims are treated as validated truth
- competitor conclusions are used in positioning or pricing decisions
- unverified user-segment assumptions are promoted to product direction

## Escalation rule

If the output collapses into vague personas, generic market copy, or unsupported competitor claims, mark it as insufficient and request stronger grounding.
