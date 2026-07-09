---
name: content-commerce-strategy-skill
description: Create or review ShopDirector AI content commerce strategy artifacts when the task is to define content themes, messaging logic, offer framing, platform-fit hypotheses, or workflow support for commerce growth decisions in docs/product_design. Use for 05_core_capabilities.md and 06_product_workflow.md. This skill is strategic and must not turn ShopDirector AI into a generic content or script generator.
---

# Content Commerce Strategy Skill

Use this skill to define how ShopDirector AI should think about commerce-content strategy, not to generate undirected creative output.

## Kernel relationship

This skill supplies strategy modules to the Decision Intelligence Kernel for:
- content understanding
- message and offer selection
- platform-facing growth choices
- content workflow support under Kernel control

It must not replace the Kernel or become the product center.

## Supported documents

- `docs/product_design/05_core_capabilities.md`
- `docs/product_design/06_product_workflow.md`

## Use when

Use this skill when the task is to:
- define content strategy angles
- map audience segments to messaging choices
- structure offer, proof, objection, and CTA logic
- compare competitor messaging patterns
- define content workflow decisions that support commerce growth

Do not use this skill to mass-produce scripts, ad copy, or creative assets as an end in itself.

## Required inputs

- merchant or business goals
- product or category context
- audience segments
- channel or platform assumptions
- competitor messaging notes
- content workflow constraints

## Workflow

1. Clarify the business decision the content strategy must support.
2. Identify the relevant audience, product, and platform context.
3. Structure the strategic components:
   - hooks
   - value propositions
   - proof
   - objections
   - offers
   - CTA logic
4. Connect messaging choices back to merchant outcomes and Kernel decision logic.
5. Flag strategy that depends on unsupported platform assumptions or collapses into generic copywriting.

## Output contract

Produce advisory outputs such as:
- content strategy angles
- messaging frameworks
- offer and proof structures
- platform-fit hypotheses
- workflow guidance for content planning decisions

## Review standard

Before considering the output usable, check:
- Does this improve content decisions rather than just generate copy?
- Is the commercial objective explicit?
- Are audience and platform assumptions visible?
- Does this avoid drifting into a generic script-writing or creative-factory tool?

## Limitations

- no browser scraping assumptions
- no live ad extraction or screenshot requirements
- no default long-form article production behavior
- no direct content publishing, API, Slack, Notion, shell, or code-execution assumptions

## Risk level

Medium

## Human approval requirements

Human approval is required before:
- public-facing strategy is treated as policy
- platform-specific recommendations are treated as operational rules
- generated messaging logic is used without business review

## Escalation rule

If the output stops serving commerce decision quality and becomes generic creative production, mark the drift and pull the work back to strategy.
