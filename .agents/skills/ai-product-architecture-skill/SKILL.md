---
name: ai-product-architecture-skill
description: Create or review ShopDirector AI product architecture artifacts when the task is to define product modules, boundaries, orchestration, capabilities, workflows, AI architecture, or governed autonomy for docs/product_design. Use for 04_product_architecture.md, 05_core_capabilities.md, 06_product_workflow.md, and 08_ai_agent_architecture.md. This skill must keep the Decision Intelligence Kernel central and treat skills as subordinate modules.
---

# AI Product Architecture Skill

Use this skill to define ShopDirector AI at the product-architecture level, not the code-implementation level.

## Kernel relationship

The Decision Intelligence Kernel must remain central. This skill explains:
- how the Kernel governs skills, tools, agents, memory, and workflows
- what stays inside the Kernel versus the skill layer
- where human approval boundaries sit
- how feedback and observability return to the Kernel

Skills are replaceable modules. The Kernel is the product core.

## Supported documents

- `docs/product_design/04_product_architecture.md`
- `docs/product_design/05_core_capabilities.md`
- `docs/product_design/06_product_workflow.md`
- `docs/product_design/08_ai_agent_architecture.md`

## Use when

Use this skill when the task is to:
- define product modules or system boundaries
- describe capability layering
- define workflow orchestration or human-in-the-loop checkpoints
- explain AI agents, tools, memory, and autonomy boundaries
- map architecture risks, trust boundaries, or observability needs

Do not use this skill to produce source code, API specs, or infrastructure commands.

## Required inputs

- product strategy outputs
- capability requirements
- workflow or user-journey expectations
- draft architecture assumptions
- known risks, constraints, and approval boundaries

## Workflow

1. Clarify the product decision the architecture must support.
2. Identify major modules and their responsibilities.
3. Separate:
   - Kernel responsibilities
   - skill-layer responsibilities
   - memory and knowledge roles
   - tool and execution roles
   - human approval checkpoints
4. Define boundaries, handoffs, and failure surfaces.
5. Check whether the architecture supports feedback and evaluation loops.
6. Flag ambiguity that would force engineering to invent product logic.

## Output contract

Produce advisory outputs such as:
- module map
- product boundary definitions
- orchestration model
- capability-to-component mapping
- workflow checkpoints
- trust-boundary and risk notes
- observability and evaluation considerations

## Review standard

Before considering the output usable, check:
- Is the Kernel clearly separated from skills and tool execution?
- Are reasoning, memory, tools, and approval boundaries explicit?
- Can an implementation team proceed without guessing product intent?
- Does the architecture support feedback, evaluation, and control loops?

## Limitations

- no code generation
- no MCP server design as a default frame
- no external CLI setup or runtime configuration instructions
- no API, browser, shell, or code-execution assumptions by default
- no permission widening without explicit approval

## Risk level

High

## Human approval requirements

Human approval is required before:
- architecture becomes a source-of-truth product boundary
- autonomy or permission boundaries are widened
- tool execution assumptions are promoted into default product behavior

## Escalation rule

If the architecture causes the product to become a disconnected agent stack, generic tool wrapper, or feature pile without Kernel control, stop and mark the drift explicitly.
