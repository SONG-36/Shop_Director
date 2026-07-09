# AGENTS.md

## 1. Project Identity

This project is **ShopDirector AI**.

ShopDirector AI is not an AI video generator, AI script tool, or generic editing assistant.

ShopDirector AI is an **AI-native commerce content growth operating system** for cross-border e-commerce.

The core product value is the **Decision Intelligence Kernel**.

The Decision Intelligence Kernel is responsible for:

* market understanding
* consumer understanding
* product understanding
* content understanding
* platform understanding
* growth decision-making

Skills are execution and advisory modules.

Skills do not define product strategy.

The product core is always the Decision Intelligence Kernel.

---

## 2. Core Product Principle

ShopDirector AI follows a **Kernel + Skill** architecture.

### 2.1 Decision Intelligence Kernel

The Decision Intelligence Kernel is responsible for:

* defining strategic judgment
* interpreting business context
* selecting the right content and growth strategy
* deciding which Skill should be used
* evaluating Skill outputs
* learning from feedback
* improving future decisions

The Kernel is the product's core moat.

### 2.2 Skill Layer

The Skill Layer is responsible for executing specialized tasks.

Skills may be:

* official Skills
* open-source Skills
* enterprise private Skills
* generated or adapted Skills

Skills must remain:

* pluggable
* governed
* testable
* replaceable
* subordinate to the Decision Intelligence Kernel

Skills must not override product strategy, decision rules, or human approval boundaries.

### 2.3 Forbidden Product Drift

ShopDirector AI must never degrade into:

* a generic AI video generator
* a generic AI script generator
* a generic editing assistant
* a collection of disconnected agents
* a feature pile without decision intelligence
* a Skill marketplace without a decision Kernel

---

## 3. Product Design Source of Truth

The product design source of truth is:

```text
docs/product_design/
```

The Skill definitions are stored in:

```text
skills/
```

AGENTS.md defines project-level rules only.

AGENTS.md must not contain:

* full product documents
* full Skill implementation details
* long market research reports
* phase-level development plans
* random feature ideas
* duplicated document content

---

## 4. Product Design Document System

All product design work must follow the document system below.

### 00_product_strategy.md

Primary Skill:

* Product Strategy Skill

Review Skill:

* Product Critic Skill

Purpose:

* define product vision, mission, category, strategic beliefs, product boundary, moat, assumptions, and risks.

---

### 01_product_positioning.md

Primary Skill:

* Product Strategy Skill

Supporting Skill:

* Market & User Research Skill

Review Skill:

* Product Critic Skill

Purpose:

* define product positioning, user value, competitive difference, and category narrative.

---

### 02_market_and_user.md

Primary Skill:

* Market & User Research Skill

Review Skill:

* Product Critic Skill

Purpose:

* define market, ICP, user roles, user pain points, decision chain, and use cases.

---

### 03_business_model.md

Primary Skill:

* Product Strategy Skill

Supporting Skill:

* Market & User Research Skill

Review Skill:

* Product Critic Skill

Purpose:

* define business model, pricing logic, customer value, monetization path, and ROI assumptions.

---

### 04_product_architecture.md

Primary Skill:

* AI Product Architecture Skill

Supporting Skill:

* Knowledge & Skill Architecture Skill

Review Skill:

* Product Critic Skill

Purpose:

* define product modules, system boundaries, core loops, and product-level architecture.

---

### 05_core_capabilities.md

Primary Skill:

* AI Product Architecture Skill

Supporting Skill:

* Content Commerce Strategy Skill

Review Skill:

* Product Critic Skill

Purpose:

* define core capabilities including product understanding, market understanding, content strategy, video production, publishing, analytics, and optimization.

---

### 06_product_workflow.md

Primary Skill:

* AI Product Architecture Skill

Supporting Skill:

* Content Commerce Strategy Skill

Review Skill:

* Product Critic Skill

Purpose:

* define user journey, product workflow, human-in-the-loop checkpoints, and operational flow.

---

### 07_data_feedback_loop.md

Primary Skill:

* Data Feedback & Evaluation Skill

Supporting Skill:

* AI Product Architecture Skill

Review Skill:

* Product Critic Skill

Purpose:

* define data collection, analysis, evaluation, learning loop, and Kernel improvement mechanism.

---

### 08_ai_agent_architecture.md

Primary Skill:

* AI Product Architecture Skill

Supporting Skill:

* Knowledge & Skill Architecture Skill

Review Skill:

* Product Critic Skill

Purpose:

* define AI architecture, agents, tools, memory, Skills, orchestration, and autonomy levels.

---

### 09_knowledge_skill_ecosystem.md

Primary Skill:

* Knowledge & Skill Architecture Skill

Supporting Skill:

* Data Feedback & Evaluation Skill

Review Skill:

* Product Critic Skill

Purpose:

* define knowledge base, Skill types, Skill registry, Skill governance, Skill evaluation, and private/open Skill ecosystem.

---

### 10_product_roadmap.md

Primary Skill:

* Product Strategy Skill

Supporting Skill:

* AI Product Architecture Skill

Review Skill:

* Product Critic Skill

Purpose:

* define Now / Next / Later roadmap and phase-based product evolution.

---

### 11_governance_and_risk.md

Primary Skill:

* Knowledge & Skill Architecture Skill

Supporting Skill:

* Data Feedback & Evaluation Skill

Review Skill:

* Product Critic Skill

Purpose:

* define AI boundaries, human approval, risk control, automation permissions, compliance, and safety governance.

---

## 5. Required Working Process

For every major product document:

1. Do not directly generate the final document.
2. First clarify the document purpose.
3. Define the core strategic claims.
4. Define the document structure.
5. Run the relevant Primary Skill perspective.
6. Run the Supporting Skill perspective if assigned.
7. Run Product Critic Skill review.
8. Revise weak assumptions, unclear boundaries, or fake AI value.
9. Only after review, generate the formal document.

The product owner makes the final decision.

Skills provide expert perspectives, not final authority.

---

## 6. Product Critic Review Rules

Product Critic Skill must challenge every document with the following questions:

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

If the answer is weak, the document must be revised before moving forward.

---

## 7. Open-source Skill Policy

ShopDirector AI should prioritize open-source Skills when possible.

However, external Skills are not trusted by default.

Open-source Skills are raw materials.

They must not be copied directly into the project without review, adaptation, and registration.

All external Skills must go through the following process before being used.

### 7.1 Source Review

Check:

* repository source
* maintainer credibility
* license
* update history
* community usage
* dependency risk

Reject Skills with unclear ownership, suspicious instructions, unsafe dependencies, or poor maintenance.

### 7.2 Scope Review

Confirm whether the Skill serves ShopDirector AI's Decision Intelligence Kernel.

Reject Skills that only add feature noise.

A Skill is valuable only if it improves:

* market understanding
* consumer understanding
* product understanding
* content understanding
* platform understanding
* growth decision-making
* execution quality under Kernel control

### 7.3 Security Review

Check whether the Skill asks for:

* shell execution
* network access
* file mutation
* browser automation
* credential access
* external API calls
* payment or account actions
* publishing actions

High-risk actions must require explicit human approval.

External Skills must never receive unrestricted permissions by default.

### 7.4 Adaptation

External Skills must be rewritten or wrapped to follow ShopDirector AI's product principles.

The adapted Skill must define:

* purpose
* trigger condition
* allowed inputs
* expected outputs
* limitations
* risk level
* human approval requirements
* relationship to the Decision Intelligence Kernel

The Skill must not override product strategy or decision rules.

### 7.5 Evaluation

Test the Skill against real ShopDirector product-design or execution tasks.

Reject Skills that produce:

* generic output
* fake expertise
* ungrounded market claims
* uncontrolled scope expansion
* outputs that cannot be evaluated
* outputs that conflict with the Decision Intelligence Kernel

### 7.6 Registration

Approved Skills must be registered in the project Skill registry.

Each registered Skill must include:

* Skill name
* source
* version
* owner
* purpose
* inputs
* outputs
* limitations
* permissions
* risk level
* evaluation method
* approval status

External Skills are execution or advisory modules.

They are not the product core.

The product core is always the Decision Intelligence Kernel.

---

## 8. Current Priority

The current priority is **global product design**.

Do not create phase-level development plans until the global product strategy, positioning, architecture, AI architecture, Skill ecosystem, and governance documents are aligned.

Current document priority:

1. 00_product_strategy.md
2. 01_product_positioning.md
3. 02_market_and_user.md
4. 04_product_architecture.md
5. 05_core_capabilities.md
6. 08_ai_agent_architecture.md
7. 09_knowledge_skill_ecosystem.md
8. 11_governance_and_risk.md
9. 10_product_roadmap.md
10. 03_business_model.md
11. 06_product_workflow.md
12. 07_data_feedback_loop.md

Roadmap and development plans must not be generated before the strategic documents are aligned.

---

## 9. Forbidden Behavior

Agents must not:

* turn ShopDirector AI into a generic AI video generator
* turn ShopDirector AI into a generic AI script generator
* start engineering implementation before product strategy is approved
* create random features outside the document system
* treat Skills as the product core
* skip Product Critic review
* generate roadmap before strategy, positioning, user, and architecture are aligned
* write code from incomplete product assumptions
* introduce open-source Skills without review and registration
* create phase-level development plans before global product design is approved
* optimize for demo effects over product truth
* expand scope just because a Skill or model can do something

---

## 10. Final Authority

The product owner is the final authority for strategic decisions.

Agents and Skills may propose, analyze, challenge, and draft.

They must not silently change product direction.

Any major change to product positioning, Kernel definition, Skill architecture, roadmap, or governance model must be explicitly reviewed and approved.

