# Skill Blueprint / Mapping

## Purpose

This document defines how the open-source skill inventory will be adapted into 7 ShopDirector-specific product design skills.

This is a blueprint only.

It does not create the final `SKILL.md` files.
It does not copy any open-source skill directly.
It treats all open-source skills as raw reference material under ShopDirector AI governance.

## ShopDirector Adaptation Rules

- The Decision Intelligence Kernel is the product core.
- Skills are advisory or execution modules under Kernel control.
- No target skill may override product strategy, decision rules, or human approval boundaries.
- Notion-specific, MCP-specific, Slack-specific, browser automation, external API, shell execution, and code-execution assumptions must be removed unless explicitly reintroduced later with approval.
- Open-source skill content must be rewritten into ShopDirector AI language, structure, and review standards.
- Product Critic Skill is the final review layer for every major product document.

## Document Support Map

| Target skill | Primary documents supported |
|---|---|
| Product Strategy Skill | `00_product_strategy.md`, `01_product_positioning.md`, `03_business_model.md`, `10_product_roadmap.md` |
| Market & User Research Skill | `01_product_positioning.md`, `02_market_and_user.md`, `03_business_model.md` |
| AI Product Architecture Skill | `04_product_architecture.md`, `05_core_capabilities.md`, `06_product_workflow.md`, `08_ai_agent_architecture.md` |
| Knowledge & Skill Architecture Skill | `04_product_architecture.md`, `08_ai_agent_architecture.md`, `09_knowledge_skill_ecosystem.md`, `11_governance_and_risk.md` |
| Content Commerce Strategy Skill | `05_core_capabilities.md`, `06_product_workflow.md` |
| Data Feedback & Evaluation Skill | `07_data_feedback_loop.md`, `09_knowledge_skill_ecosystem.md`, `11_governance_and_risk.md` |
| Product Critic Skill | Final review layer for all major product documents |

## Skill Mapping

### 1. Product Strategy Skill

**Target purpose**

Define product vision, category, strategic scope, moat, business logic, roadmap sequencing, and non-negotiable Kernel-centered product boundaries.

**Product documents it supports**

- `00_product_strategy.md`
- `01_product_positioning.md`
- `03_business_model.md`
- `10_product_roadmap.md`

**Primary open-source references from the inventory**

- `skills/skills/.system/skill-creator/`
- `awesome-codex-skills/notion-spec-to-implementation/`
- `awesome-codex-skills/notion-research-documentation/`
- Catalog-only PM pointers in `awesome-agent-skills/README.md`

**Reusable ideas**

- Parse ambiguous PRD-style inputs into explicit claims, assumptions, risks, and phased priorities.
- Use comparison and synthesis structures rather than free-form brainstorming.
- Separate requirements, constraints, dependencies, and success criteria.
- Keep the skill body concise and push detailed frameworks into references later.

**Parts that must be rewritten for ShopDirector AI**

- Replace implementation-plan framing with strategic decision framing.
- Replace Notion page creation with document-outline generation for `docs/product_design/`.
- Rewrite all triggers around product vision, category design, ICP-value logic, business logic, and roadmap logic.
- Add explicit Kernel-fit checks to every strategy output.

**Parts that must be rejected or ignored**

- Notion search/fetch/create/update flows.
- Task database creation and task tracking workflows.
- Any assumption that the skill should create execution tickets automatically.
- Any generic PM advice not tied to cross-border commerce growth decision-making.

**Relationship to the Decision Intelligence Kernel**

This skill defines the strategic frame the Kernel will later use. It cannot define the Kernel itself, but it must express the Kernel's role, scope, moat, and decision responsibilities.

**Expected inputs**

- Product brief or draft claims
- Business context
- Category assumptions
- Target customer hypotheses
- Constraints, risks, and product boundaries

**Expected outputs**

- Strategic claim map
- Product positioning options
- Assumption and risk register
- Roadmap logic
- Draft structure for product strategy documents

**Review criteria**

- Does it strengthen the Decision Intelligence Kernel?
- Are scope and category boundaries explicit?
- Are moat claims evidence-based rather than decorative AI language?
- Can the output guide later architecture and workflow documents without ambiguity?

**Risk level**

High

**Human approval requirements**

- Required before any strategic claim is accepted as product direction
- Required before roadmap sequencing is treated as committed

**Recommendation**

Create now

### 2. Market & User Research Skill

**Target purpose**

Translate market, ICP, merchant workflow, user roles, pain points, competitor signals, and decision-chain evidence into structured product design inputs.

**Product documents it supports**

- `01_product_positioning.md`
- `02_market_and_user.md`
- `03_business_model.md`

**Primary open-source references from the inventory**

- `awesome-codex-skills/notion-research-documentation/`
- `skills/skills/.curated/notion-research-documentation/`
- `awesome-codex-skills/lead-research-assistant/`
- `awesome-codex-skills/competitive-ads-extractor/`
- `awesome-codex-skills/support-ticket-triage/`

**Reusable ideas**

- Comparison templates for competitor and segment analysis.
- ICP qualification logic and fit-scoring patterns.
- Structured synthesis of market signals into themes, evidence, and implications.
- Taxonomy-based normalization of user pain points and feedback signals.

**Parts that must be rewritten for ShopDirector AI**

- Convert lead-generation language into market-segment and merchant-fit analysis.
- Convert ad-scraping framing into messaging-pattern analysis for commerce content competitors.
- Convert support-triage framing into insight clustering for merchant pain points, friction, and unmet decisions.
- Add ShopDirector-specific user roles such as founder, operator, marketer, creator, analyst, and approval owner.

**Parts that must be rejected or ignored**

- Outreach strategy generation.
- Live ad extraction assumptions.
- Any requirement for screenshots, browser automation, or live enrichment.
- Any sales-ops or CRM-specific output format.

**Relationship to the Decision Intelligence Kernel**

This skill feeds the Kernel's market understanding, consumer understanding, and growth decision-making inputs. It informs the Kernel; it does not make final market decisions on its own.

**Expected inputs**

- Research questions
- Market hypotheses
- Competitor or segment notes
- Internal interviews, notes, or feedback summaries
- Existing positioning drafts

**Expected outputs**

- ICP definitions
- User-role map
- Pain-point clusters
- Competitor and messaging comparison
- Decision-chain and use-case analysis

**Review criteria**

- Are claims grounded and scoped?
- Does the output identify real decision bottlenecks rather than generic persona copy?
- Does it help the Kernel decide where strategy should focus?
- Are evidence and inference clearly separated?

**Risk level**

Medium

**Human approval requirements**

- Required before external market claims are treated as validated
- Required before competitor conclusions are used in positioning or pricing decisions

**Recommendation**

Create now

### 3. AI Product Architecture Skill

**Target purpose**

Define product-level architecture, module boundaries, workflow orchestration, capability layering, and the AI-native relationship between the Kernel, tools, agents, and governed execution modules.

**Product documents it supports**

- `04_product_architecture.md`
- `05_core_capabilities.md`
- `06_product_workflow.md`
- `08_ai_agent_architecture.md`

**Primary open-source references from the inventory**

- `awesome-codex-skills/mcp-builder/`
- `awesome-codex-skills/notion-spec-to-implementation/`
- `skills/skills/.curated/security-threat-model/`
- `awesome-codex-skills/langsmith-fetch/`

**Reusable ideas**

- Explicit system boundaries, interfaces, and error-handling expectations.
- Evaluation-minded architecture design rather than only component naming.
- Threat-model style enumeration of trust boundaries, risks, and mitigations.
- Trace-oriented thinking about failure points, state transitions, and observability.

**Parts that must be rewritten for ShopDirector AI**

- Replace MCP-server-building guidance with product architecture guidance.
- Replace implementation task sequencing with product module and workflow sequencing.
- Reframe security-threat content from AppSec review into architecture governance and operational boundary language.
- Reframe tracing content into runtime observability and evaluation design for Kernel-directed workflows.

**Parts that must be rejected or ignored**

- MCP tool naming specifics as mandatory design rules.
- External CLI setup, environment variable setup, and LangSmith operational dependency.
- Code generation and server implementation assumptions.
- Any architecture advice that treats skills as the product core.

**Relationship to the Decision Intelligence Kernel**

This skill is responsible for expressing how the Kernel governs agents, skills, memory, tools, workflow routing, and execution safety. The Kernel remains central and supervisory.

**Expected inputs**

- Product strategy outputs
- Capability requirements
- Workflow requirements
- Known risks and constraints
- Draft architecture assumptions

**Expected outputs**

- Module map
- Boundary definitions
- Workflow orchestration model
- Capability-to-component mapping
- Risk and observability notes

**Review criteria**

- Is the Kernel clearly separated from skills and tool execution?
- Are boundaries between reasoning, memory, tools, and human approval explicit?
- Can engineering implement this without inventing the product logic?
- Does the architecture support feedback and evaluation loops?

**Risk level**

High

**Human approval requirements**

- Required before architecture becomes a source of truth
- Required before any autonomy or permission boundary is widened

**Recommendation**

Create now

### 4. Knowledge & Skill Architecture Skill

**Target purpose**

Define how knowledge assets, skill types, skill registry, adaptation rules, lifecycle governance, and approval boundaries should work under the Kernel + Skill architecture.

**Product documents it supports**

- `04_product_architecture.md`
- `08_ai_agent_architecture.md`
- `09_knowledge_skill_ecosystem.md`
- `11_governance_and_risk.md`

**Primary open-source references from the inventory**

- `skills/skills/.system/skill-creator/`
- `awesome-codex-skills/notion-knowledge-capture/`
- `awesome-codex-skills/skill-share/`
- `awesome-codex-skills/template-skill/`
- `awesome-codex-skills/mcp-builder/`

**Reusable ideas**

- Progressive disclosure design for skills.
- Clear distinction between `SKILL.md`, `references/`, `scripts/`, and assets.
- Knowledge typing and schema thinking for decisions, how-tos, documentation, and reusable patterns.
- Packaging and governance concepts for skill lifecycle management.

**Parts that must be rewritten for ShopDirector AI**

- Replace Notion database assumptions with ShopDirector knowledge object and registry concepts.
- Rewrite sharing/distribution logic around internal registry and approval status, not Slack or public sharing.
- Convert generic skill-creation guidance into ShopDirector-specific skill taxonomy and governance language.
- Make the adaptation policy and registration requirements explicit in the skill itself.

**Parts that must be rejected or ignored**

- Slack notification and team broadcast assumptions.
- Auto-packaging and distribution steps as default behavior.
- Any workflow that allows direct import of external skills without review.
- Any assumption that knowledge capture equals product truth without critic review.

**Relationship to the Decision Intelligence Kernel**

This skill ensures the Kernel remains the governing center of the ecosystem. It defines how skills and knowledge are registered, evaluated, limited, replaced, and approved.

**Expected inputs**

- Architecture assumptions
- Open-source skill inventory
- Governance constraints
- Knowledge categories
- Required skill types and permission boundaries

**Expected outputs**

- Skill taxonomy
- Registry schema
- Knowledge object model
- Governance rules
- Approval and evaluation workflow

**Review criteria**

- Are skills clearly subordinate to the Kernel?
- Are registration, permissions, and evaluation rules explicit?
- Can private, official, generated, and open-source skills coexist safely?
- Is there a clear distinction between knowledge, execution, and decision layers?

**Risk level**

High

**Human approval requirements**

- Required before approving registry rules or adaptation policy
- Required before defining any high-risk permission category as allowed

**Recommendation**

Create now

### 5. Content Commerce Strategy Skill

**Target purpose**

Translate ShopDirector's commerce-content mission into repeatable strategy logic for content themes, messaging, offer framing, creative workflow support, and platform-facing growth choices.

**Product documents it supports**

- `05_core_capabilities.md`
- `06_product_workflow.md`

**Primary open-source references from the inventory**

- `awesome-codex-skills/competitive-ads-extractor/`
- `awesome-codex-skills/content-research-writer/`
- `awesome-codex-skills/lead-research-assistant/`
- Catalog-only marketing pointers in `awesome-agent-skills/README.md`

**Reusable ideas**

- Message pattern extraction from competitor content.
- Structured outline -> evidence -> recommendation workflow.
- Audience/pain-point mapping to content angle selection.
- Commercial framing around value props, CTA logic, and campaign narratives.

**Parts that must be rewritten for ShopDirector AI**

- Convert content writing workflow into commerce decision workflow for what content should exist, why, and for whom.
- Replace lead and outreach framing with merchant growth and content conversion logic.
- Reframe ad analysis into reusable content-commerce strategy primitives such as hooks, offers, objections, proof, and platform fit.
- Connect outputs back to Kernel decisions on content understanding and growth execution.

**Parts that must be rejected or ignored**

- Direct browser scraping assumptions.
- Long-form article production as the default end state.
- Generic brand-copy output that lacks commerce decision value.
- Any instruction that turns the product into a script generator or creative factory without strategy control.

**Relationship to the Decision Intelligence Kernel**

This skill supplies strategy modules for content understanding and growth decision-making. It does not replace the Kernel's decision function and must not become the product center.

**Expected inputs**

- Merchant goals
- Product/category context
- Channel or platform assumptions
- Audience segments
- Competitor messaging notes

**Expected outputs**

- Content strategy angles
- Messaging frameworks
- Offer and proof structures
- Platform-fit hypotheses
- Workflow support for content planning decisions

**Review criteria**

- Does it improve content decisions rather than generate undirected copy?
- Is commercial intent explicit?
- Are platform and audience assumptions visible?
- Does it avoid drifting into a generic script-writing tool?

**Risk level**

Medium

**Human approval requirements**

- Required before strategy is used to shape public-facing content policy
- Required before any platform-specific recommendation is treated as operational guidance

**Recommendation**

Create later

### 6. Data Feedback & Evaluation Skill

**Target purpose**

Define how ShopDirector AI should collect feedback, classify signals, evaluate outcomes, detect failure patterns, and improve the Kernel through governed learning loops.

**Product documents it supports**

- `07_data_feedback_loop.md`
- `09_knowledge_skill_ecosystem.md`
- `11_governance_and_risk.md`

**Primary open-source references from the inventory**

- `awesome-codex-skills/developer-growth-analysis/`
- `awesome-codex-skills/langsmith-fetch/`
- `awesome-codex-skills/support-ticket-triage/`
- `awesome-codex-skills/issue-triage/`
- `awesome-codex-skills/meeting-insights-analyzer/`
- `awesome-codex-skills/mcp-builder/reference/evaluation.md`

**Reusable ideas**

- Evidence-based evaluation with explicit strengths, failure modes, and action items.
- Trace/failure analysis patterns for workflow diagnosis.
- Taxonomy-based clustering of feedback and issues.
- Evaluation-question discipline and stable answer thinking.

**Parts that must be rewritten for ShopDirector AI**

- Replace personal growth and Slack-delivery framing with product feedback and Kernel-learning framing.
- Replace LangSmith-specific mechanics with generic trace, event, and evaluation abstractions.
- Convert support and issue triage into product-signal ingestion, prioritization, and learning-loop design.
- Add linkage from evaluation outputs to skill governance and Kernel improvement decisions.

**Parts that must be rejected or ignored**

- External service setup instructions and API credentials.
- Slack DM delivery and notification assumptions.
- Human communication coaching that does not inform product evaluation.
- Any metric framework that cannot be tied to decision quality or execution quality.

**Relationship to the Decision Intelligence Kernel**

This skill defines how the Kernel learns. It should formalize what feedback matters, how evidence is interpreted, and how evaluated outcomes flow back into future decisions.

**Expected inputs**

- Output samples
- Feedback logs
- Issue summaries
- Workflow traces
- Evaluation questions
- Observed failure cases

**Expected outputs**

- Feedback taxonomy
- Evaluation criteria
- Failure pattern summaries
- Learning-loop recommendations
- Improvement priorities for Kernel and skill layer

**Review criteria**

- Is the loop specific enough to improve future decisions?
- Are signals ranked by decision relevance?
- Are evaluation outputs auditable and comparable?
- Is there a clear path from evidence to action?

**Risk level**

High

**Human approval requirements**

- Required before metrics or evaluation rules become governance standards
- Required before feedback is allowed to modify decision policy or automation boundaries

**Recommendation**

Create later

### 7. Product Critic Skill

**Target purpose**

Act as the final review layer for every major product document by challenging strategy drift, fake AI value, unclear boundaries, missing data loops, weak moats, and implementation ambiguity.

**Product documents it supports**

- All major product documents in `docs/product_design/`

**Primary open-source references from the inventory**

- `codex/.codex/skills/code-review/`
- `codex/.codex/skills/code-review-breaking-changes/`
- `codex/.codex/skills/code-review-context/`
- `awesome-codex-skills/meeting-insights-analyzer/`
- `skills/skills/.curated/security-threat-model/`

**Reusable ideas**

- Lens-based review rather than one-pass generic commentary.
- Specific finding format with evidence and clear revision pressure.
- Boundary and hidden-cost review logic.
- Risk and abuse-path thinking applied to product design, not only code.

**Parts that must be rewritten for ShopDirector AI**

- Convert PR/code review into product-document review.
- Replace file-line findings with claim-level, structure-level, and logic-level findings.
- Encode the 10 mandatory critic questions from `AGENTS.md`.
- Make the critic explicitly review Kernel alignment, AI-native advantage, human approval boundaries, and scope control.

**Parts that must be rejected or ignored**

- GitHub PR labeling assumptions.
- Codebase-specific breaking change surfaces.
- Any review pattern that focuses only on syntax or editorial polish.
- Any reviewer behavior that acts as final authority rather than review pressure.

**Relationship to the Decision Intelligence Kernel**

This skill protects the Kernel from product drift. It does not create direction; it validates whether other skill outputs actually strengthen the Kernel-centered product.

**Expected inputs**

- Draft product document
- Declared document purpose
- Upstream assumptions
- Claimed user value
- Claimed data loop and approval boundary

**Expected outputs**

- Findings list ordered by severity
- Weak-claim list
- Missing-boundary list
- Revision guidance
- Pass / revise recommendation

**Review criteria**

- Does it use the required critic questions consistently?
- Are findings specific, actionable, and decision-relevant?
- Does it block drift into generic AI tooling?
- Does it improve document rigor before formalization?

**Risk level**

Medium

**Human approval requirements**

- Required to close unresolved high-severity findings
- Required to accept any document despite critic objections

**Recommendation**

Create now

## Creation Sequence Recommendation

### Create now

1. Product Strategy Skill
2. Market & User Research Skill
3. AI Product Architecture Skill
4. Knowledge & Skill Architecture Skill
5. Product Critic Skill

### Create later

1. Content Commerce Strategy Skill
2. Data Feedback & Evaluation Skill

### Needs more research

- No additional target skill is blocked outright, but catalog-only PM and marketing sources in `awesome-agent-skills` should not be used directly until selectively fetched and reviewed.

## Final Blueprint Rules

- Every target skill must include an explicit relationship to the Decision Intelligence Kernel.
- Every target skill must state limitations, risk level, and human approval requirements.
- No target skill may contain direct installation, activation, network, browser, Slack, Notion, or code-execution instructions by default.
- Product Critic Skill must review every major product document before that document is treated as formal output.
- Open-source skills remain source material only until rewritten into ShopDirector-specific skills.
