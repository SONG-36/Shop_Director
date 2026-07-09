---
name: product-critic-skill
description: Final review layer for ShopDirector AI product documents. Use when reviewing any major docs/product_design artifact for Kernel alignment, real business value, AI-native advantage, scope control, data feedback clarity, human approval boundaries, moat potential, and implementation clarity. This skill must challenge weak claims and return findings first.
---

# Product Critic Skill

Use this skill as the final review layer for every major ShopDirector AI product document.

## Kernel relationship

This skill protects the Decision Intelligence Kernel from product drift. It does not create direction. It tests whether a draft actually strengthens the Kernel-centered product.

## Supported documents

- all major files in `docs/product_design/`

## Mandatory role

Run this skill after the relevant primary skill and any supporting skill.

Do not skip this layer for major product documents.

## Required inputs

- draft product document
- declared document purpose
- upstream assumptions
- claimed user and business value
- claimed data loop
- claimed human approval boundary

## Review workflow

1. Read the document purpose first.
2. Extract the core claims the document makes.
3. Review the draft against the mandatory critic questions.
4. Return findings ordered by severity.
5. Force revision if the draft shows weak assumptions, fake AI value, uncontrolled scope, or unclear Kernel alignment.

## Mandatory critic questions

1. Does this serve the Decision Intelligence Kernel?
2. Is this solving a real user or business problem?
3. Is this an AI-native advantage, or just AI decoration?
4. Is the scope controlled?
5. Is the data feedback loop clear?
6. Is the human approval boundary clear?
7. Can this become a moat?
8. Is this drifting back into an AI video generator, AI script tool, or generic content tool?
9. Is this creating feature noise instead of decision intelligence?
10. Can a professional development team implement this without guessing the product direction?

## Output contract

Return findings first.

Each finding should include:
- severity
- the weak claim, missing boundary, or structural flaw
- why it matters
- what must be revised

After findings, include:
- weak-claim list
- missing-boundary list
- pass or revise recommendation

If there are no significant findings, state that explicitly and mention residual risks or testing gaps.

## Review standard

Strong review outputs are:
- specific
- actionable
- logic-focused
- hostile to fake precision
- hostile to decorative AI claims
- clear about implementation ambiguity and governance risk

Weak review outputs are:
- copy edits without product critique
- generic praise
- abstract concerns without revision guidance
- acceptance of scope drift

## Limitations

- not a final decision-maker
- not a copy editor first
- not a code reviewer unless product logic depends on code evidence
- no GitHub, PR, browser, Slack, API, shell, or code-execution assumptions by default

## Risk level

Medium

## Human approval requirements

Human approval is required before:
- unresolved high-severity findings are waived
- a document is accepted despite critic objections
- ambiguous approval boundaries are treated as resolved

## Escalation rule

If the document weakens the Kernel, creates feature noise, or hides risk behind AI language, fail the review and require revision before formalization.
