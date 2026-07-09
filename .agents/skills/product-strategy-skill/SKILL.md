---
name: product-strategy-skill
description: Create or review ShopDirector AI product strategy artifacts when the task is to define vision, positioning, business logic, strategic scope, moat, document structure, or roadmap logic for docs/product_design. Use for 00_product_strategy.md, 01_product_positioning.md, 03_business_model.md, and 10_product_roadmap.md. This skill is advisory only and must keep the Decision Intelligence Kernel as the product core.
---

# Product Strategy Skill

Use this skill to shape ShopDirector AI strategy documents without drifting into generic AI tooling or execution planning.

## Kernel relationship

The Decision Intelligence Kernel is the product core. This skill defines the strategic frame around the Kernel:
- what the Kernel is responsible for
- what business problem it solves
- what strategic boundaries it must keep
- why the Kernel creates moat

This skill must not redefine the Kernel as a generic agent platform, content generator, or feature marketplace.

## Supported documents

- `docs/product_design/00_product_strategy.md`
- `docs/product_design/01_product_positioning.md`
- `docs/product_design/03_business_model.md`
- `docs/product_design/10_product_roadmap.md`

## Use when

Use this skill when the task is to:
- define or refine product vision, mission, category, or strategic beliefs
- clarify product boundary, moat, or non-goals
- structure product positioning or category narrative
- define pricing logic, value logic, or business model assumptions
- sequence roadmap priorities at the product level

Do not use this skill for code design, tool implementation, market data collection, or final critique.

## Required inputs

- document target and purpose
- current strategic claims or draft notes
- business context and constraints
- target customer hypotheses
- known risks, assumptions, and non-goals

If inputs are incomplete, first surface the missing assumptions instead of inventing certainty.

## Workflow

1. Clarify the document purpose and decision it must support.
2. Extract the core strategic claims.
3. Separate:
   - goals
   - assumptions
   - constraints
   - risks
   - non-goals
4. Test whether each claim strengthens the Decision Intelligence Kernel.
5. Produce a clean document structure before drafting content.
6. When multiple directions exist, present bounded options with tradeoffs.
7. Flag claims that require human approval before they can become product truth.

## Output contract

Produce advisory outputs such as:
- strategic claim map
- product boundary definition
- positioning options
- assumption and risk register
- business model logic
- roadmap sequencing logic
- recommended outline for the target product document

Keep outputs concise, explicit, and decision-oriented.

## Review standard

Before considering the output usable, check:
- Does this strengthen the Decision Intelligence Kernel?
- Is the product still clearly not a generic AI video generator, script tool, or editing assistant?
- Are scope boundaries explicit?
- Are moat claims specific rather than decorative AI language?
- Can architecture and workflow teams use this without guessing product intent?

## Limitations

- advisory only
- no direct market validation
- no execution-ticket generation
- no task database, project management, or implementation planning behavior
- no Notion, Slack, MCP, browser, API, shell, or code-execution assumptions

## Risk level

High

## Human approval requirements

Human approval is required before:
- strategic claims become source-of-truth direction
- category or positioning decisions are treated as final
- roadmap sequencing is treated as committed

## Escalation rule

If the strategy appears to weaken the Kernel, blur product scope, or introduce fake AI value, stop and surface the problem explicitly.
