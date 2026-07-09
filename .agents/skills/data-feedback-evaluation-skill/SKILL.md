---
name: data-feedback-evaluation-skill
description: Create or review ShopDirector AI data feedback and evaluation artifacts when the task is to define feedback loops, evaluation criteria, signal taxonomy, failure analysis, or Kernel learning logic for docs/product_design. Use for 07_data_feedback_loop.md, 09_knowledge_skill_ecosystem.md, and 11_governance_and_risk.md. This skill defines how the Decision Intelligence Kernel learns and must not assume external services or automation by default.
---

# Data Feedback & Evaluation Skill

Use this skill to define how ShopDirector AI evaluates outcomes and learns from signals under governance.

## Kernel relationship

This skill defines how the Decision Intelligence Kernel learns:
- what signals matter
- how signals are classified
- how outcomes are evaluated
- how failure patterns are surfaced
- how approved learning feeds future decisions

It does not directly change policy on its own.

## Supported documents

- `docs/product_design/07_data_feedback_loop.md`
- `docs/product_design/09_knowledge_skill_ecosystem.md`
- `docs/product_design/11_governance_and_risk.md`

## Use when

Use this skill when the task is to:
- define feedback taxonomy
- define evaluation questions or criteria
- classify product, workflow, or skill failure patterns
- map learning loops back to the Kernel and skill governance
- define how signals become approved improvements

Do not use this skill for live analytics integration, external API setup, or operational alerting workflows.

## Required inputs

- output samples or draft artifacts
- feedback summaries or issue clusters
- workflow traces or event descriptions
- known failure cases
- evaluation questions
- governance constraints

## Workflow

1. Clarify the evaluation objective.
2. Identify signal types:
   - user feedback
   - workflow outcomes
   - quality failures
   - approval overrides
   - performance or reasoning issues
3. Define ranking logic based on decision relevance.
4. Convert signals into:
   - taxonomy
   - evaluation criteria
   - failure patterns
   - improvement priorities
5. Check whether the loop is auditable and actionable.
6. Flag any learning rule that would silently modify the Kernel or widen autonomy without approval.

## Output contract

Produce advisory outputs such as:
- feedback taxonomy
- evaluation criteria
- failure pattern summaries
- learning-loop design
- improvement priorities for Kernel and skill layer
- governance notes for approved feedback use

## Review standard

Before considering the output usable, check:
- Is the loop specific enough to improve future decisions?
- Are signals ranked by decision relevance?
- Are evaluation outputs auditable and comparable?
- Is there a clear path from evidence to approved action?

## Limitations

- no external service setup
- no API credentials or trace-platform dependency by default
- no Slack or notification assumptions
- no browser, shell, or code-execution assumptions by default
- no automatic policy mutation

## Risk level

High

## Human approval requirements

Human approval is required before:
- metrics or evaluation rules become governance standards
- feedback changes decision policy
- automation boundaries are widened based on observed outcomes
- learning outputs are treated as self-updating product truth

## Escalation rule

If the evaluation design cannot connect evidence to action, or if it encourages uncontrolled self-modification, reject it and surface the governance risk.
