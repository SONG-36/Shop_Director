---
name: knowledge-skill-architecture-skill
description: Create or review ShopDirector AI knowledge and skill ecosystem artifacts when the task is to define knowledge objects, skill taxonomy, registry rules, adaptation policy, governance, permissions, or approval boundaries for docs/product_design. Use for 04_product_architecture.md, 08_ai_agent_architecture.md, 09_knowledge_skill_ecosystem.md, and 11_governance_and_risk.md. This skill must keep all skills subordinate to the Decision Intelligence Kernel.
---

# Knowledge & Skill Architecture Skill

Use this skill to define how ShopDirector AI governs knowledge and skills under the Kernel + Skill architecture.

## Kernel relationship

This skill protects the central role of the Decision Intelligence Kernel by defining:
- what counts as knowledge versus execution logic
- how skills are typed, registered, and evaluated
- what permissions and risks each skill class may carry
- how external skills are adapted without becoming product truth

The Kernel governs the ecosystem. This skill defines the ecosystem rules.

## Supported documents

- `docs/product_design/04_product_architecture.md`
- `docs/product_design/08_ai_agent_architecture.md`
- `docs/product_design/09_knowledge_skill_ecosystem.md`
- `docs/product_design/11_governance_and_risk.md`

## Use when

Use this skill when the task is to:
- define skill taxonomy or registry structure
- define knowledge object types and lifecycle
- define adaptation, approval, or evaluation rules for skills
- define permission classes and governance boundaries
- explain how private, generated, official, and open-source skills coexist

Do not use this skill for direct product strategy, market research, or code implementation.

## Required inputs

- architecture assumptions
- governance constraints
- open-source skill inventory or adaptation candidates
- target skill types
- required permissions and approval boundaries

## Workflow

1. Clarify the governance or ecosystem question being solved.
2. Separate the layers:
   - Kernel
   - knowledge layer
   - skill layer
   - execution layer
   - approval layer
3. Define the object model:
   - knowledge types
   - skill types
   - registration metadata
   - evaluation methods
   - permission classes
4. Check whether each rule keeps skills subordinate to the Kernel.
5. Flag any workflow that would allow unreviewed import, unsafe execution, or uncontrolled autonomy.

## Output contract

Produce advisory outputs such as:
- skill taxonomy
- registry schema
- knowledge object model
- adaptation policy
- governance rules
- approval workflow
- evaluation and registration criteria

## Review standard

Before considering the output usable, check:
- Are skills clearly subordinate to the Kernel?
- Are registration, evaluation, and permission rules explicit?
- Is there a clear distinction between knowledge, execution, and decision layers?
- Can private, official, generated, and open-source skills coexist safely under these rules?

## Limitations

- no Slack, broadcast, or public-sharing workflow by default
- no direct external skill import
- no packaging or distribution automation as a default behavior
- no Notion, MCP, browser, API, shell, or code-execution assumptions by default

## Risk level

High

## Human approval requirements

Human approval is required before:
- registry rules become policy
- external skill adaptation rules are accepted
- any high-risk permission class is allowed
- any skill is approved to bypass normal review

## Escalation rule

If the proposed ecosystem weakens governance, hides permissions, or lets skills override product direction, reject the design and surface the control failure directly.
