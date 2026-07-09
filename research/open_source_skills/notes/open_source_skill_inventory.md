# Open Source Skill Inventory

## Scope

This document inventories the downloaded repositories under `research/open_source_skills/raw/` as raw reference material only.

Guardrails followed during this pass:
- No external skills were installed into Codex global paths.
- No scripts from downloaded skills were executed.
- No external APIs were called.
- `AGENTS.md` was not modified.
- No ShopDirector target skills were created yet.

## Repositories Downloaded

| Repository | Local path | Local `SKILL.md` count | What it contains | Initial relevance |
|---|---|---:|---|---|
| `awesome-agent-skills` | `research/open_source_skills/raw/awesome-agent-skills` | 0 | Index/catalog repo. Local content is mainly `README.md` links to many external skill collections. | Useful as a pointer map, not as direct adaptation source yet. |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills` | 880 | Large community skill collection. Mix of practical Codex skills plus a very large `composio-skills/` automation corpus. | Best local source for workflow ideas, but trust level is uneven. |
| `skills` | `research/open_source_skills/raw/skills` | 44 | Deprecated OpenAI skills repo with `.curated` and `.system` skills. | High-value reference for official structure and concise skill patterns. |
| `codex` | `research/open_source_skills/raw/codex` | 19 | Codex CLI source tree; includes internal `.codex/skills` and sample skill assets. | Useful for critique/orchestration/meta-skill patterns, not domain content. |

## Repository-Level Notes

- `awesome-agent-skills` is a catalog, not a local skill corpus. It does, however, point to product-management and marketing collections that may be worth fetching later.
- `awesome-codex-skills` has the broadest practical coverage for research, planning, knowledge capture, evaluation, and GTM content workflows.
- `skills` overlaps with `awesome-codex-skills` on several Notion and meta skills. For duplicated skills, prefer `skills` for official baseline structure and `awesome-codex-skills` for extra examples/references/evaluations.
- `codex` is most relevant for `Product Critic Skill` because its internal review skills are narrow, opinionated, and decomposed by critique lens.
- `awesome-codex-skills/composio-skills/` appears auto-generated at scale. It may be useful later for connector ideas, but should not be trusted as a primary design source for the 7 target ShopDirector skills.

## Best Candidate Map by ShopDirector Target Skill

| ShopDirector target skill | Best local candidate starting points |
|---|---|
| Product Strategy Skill | `notion-spec-to-implementation`, `notion-research-documentation`, catalog-only PM collections in `awesome-agent-skills` |
| Market & User Research Skill | `notion-research-documentation`, `lead-research-assistant`, `competitive-ads-extractor`, `support-ticket-triage` |
| AI Product Architecture Skill | `notion-spec-to-implementation`, `mcp-builder`, `security-threat-model`, `langsmith-fetch` |
| Knowledge & Skill Architecture Skill | `skill-creator`, `notion-knowledge-capture`, `skill-share`, `template-skill`, `mcp-builder` |
| Content Commerce Strategy Skill | `content-research-writer`, `competitive-ads-extractor`, `lead-research-assistant`, catalog-only marketing collections in `awesome-agent-skills` |
| Data Feedback & Evaluation Skill | `developer-growth-analysis`, `langsmith-fetch`, `issue-triage`, `support-ticket-triage`, `meeting-insights-analyzer`, `mcp-builder` evaluation docs |
| Product Critic Skill | `code-review`, `code-review-breaking-changes`, `code-review-context`, `developer-growth-analysis`, `meeting-insights-analyzer`, `security-threat-model` |

## Candidate Inventory

| Repository | Path | Original skill name | Likely target ShopDirector skill | Useful ideas | Risk notes | Consider for adaptation |
|---|---|---|---|---|---|---|
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/notion-spec-to-implementation/` | `notion-spec-to-implementation` | Product Strategy Skill | Parse PRDs/specs into requirements, acceptance criteria, phases, risks, dependencies, progress cadence. Good reference files and examples. | Hard-wired to Notion MCP and implementation execution. More delivery-oriented than strategy-oriented. | Yes |
| `skills` | `research/open_source_skills/raw/skills/skills/.curated/notion-spec-to-implementation/` | `notion-spec-to-implementation` | Product Strategy Skill | Same core workflow as above, but in the official curated repo. Good baseline for concise structure. | Deprecated repo overall; content still useful but should be treated as reference only. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/notion-research-documentation/` | `notion-research-documentation` | Market & User Research Skill | Strong synthesis patterns: format selection, comparison templates, citation discipline, examples for market/competitor research. | Notion-coupled. Outputs documents, not reusable insight models by itself. | Yes |
| `skills` | `research/open_source_skills/raw/skills/skills/.curated/notion-research-documentation/` | `notion-research-documentation` | Market & User Research Skill | Official duplicate of the above. Useful for preserving cleaner trigger metadata and concise workflow. | Same Notion dependency and doc-centric bias. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/lead-research-assistant/` | `lead-research-assistant` | Market & User Research Skill | ICP definition, signal-based qualification, fit scoring, and company-level prioritization can inform merchant/shop targeting logic. | Sales-lead bias; assumes live enrichment and outreach context. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/competitive-ads-extractor/` | `competitive-ads-extractor` | Content Commerce Strategy Skill | Good framework for competitor messaging analysis: themes, pain points, value props, CTA patterns, creative formats. | Assumes scraping ad libraries and screenshots. Tooling and legality constraints need review before any adaptation. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/content-research-writer/` | `content-research-writer` | Content Commerce Strategy Skill | Collaborative outline -> research -> drafting -> feedback loop. Useful for content planning and section-level review workflow. | Verbose and article-centric. Weak on structured commerce metrics and operational reuse. | Maybe |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/support-ticket-triage/` | `support-ticket-triage` | Data Feedback & Evaluation Skill | Clean pattern for classifying inbound feedback into category, priority, summary, next steps, and reply draft. Good for customer signal normalization. | Support queue framing is narrow; taxonomy likely needs redesign for product insight ingestion. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/issue-triage/` | `issue-triage` | Data Feedback & Evaluation Skill | Useful patterns for backlog clustering, dedupe, prioritization, and digest generation. | Strong Composio/Linear/Jira dependency. Operational issue triage is not the same as product insight evaluation. | Maybe |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/developer-growth-analysis/` | `developer-growth-analysis` | Data Feedback & Evaluation Skill | Evidence-based scoring of patterns, prioritized improvement areas, strengths, and action items is a strong evaluation/reporting model. | Depends on local Codex history, HackerNews search, and Slack DM delivery. Privacy and external dependency assumptions are high. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/langsmith-fetch/` | `langsmith-fetch` | Data Feedback & Evaluation Skill | Good trace-analysis workflow: recent traces, failure points, tool-call flow, token usage, exportable debug sessions. | Depends on external CLI, env vars, and LangSmith runtime. Specific to LangChain/LangGraph ecosystems. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/meeting-insights-analyzer/` | `meeting-insights-analyzer` | Product Critic Skill | Strong critique shape: pattern detection, evidence-backed examples, strengths vs. growth areas, concrete recommendations. | Transcript-centric and focused on human communication behavior, not product artifacts. | Maybe |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/mcp-builder/` | `mcp-builder` | AI Product Architecture Skill | Excellent references for architecture discipline: tool naming, response design, pagination, error handling, security, evaluation harness design. | Focused on MCP servers rather than product systems broadly. Some value is in references, not the main workflow. | Yes |
| `skills` | `research/open_source_skills/raw/skills/skills/.curated/security-threat-model/` | `security-threat-model` | AI Product Architecture Skill | Risk-first architecture review: trust boundaries, assets, attacker goals, abuse paths, mitigations, explicit assumptions. | Security-specific and repo-grounded; requires code/system evidence. Not a general architecture planning skill. | Maybe |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/notion-knowledge-capture/` | `notion-knowledge-capture` | Knowledge & Skill Architecture Skill | Strong model for converting conversations/decisions into structured knowledge types, schemas, relations, and reusable documentation views. | Heavily Notion/database-specific. Knowledge graph assumptions may need abstraction. | Yes |
| `skills` | `research/open_source_skills/raw/skills/skills/.system/skill-creator/` | `skill-creator` | Knowledge & Skill Architecture Skill | Most useful meta-skill found. Covers skill anatomy, naming, progressive disclosure, when to use `scripts/`, `references/`, and `assets/`, and what not to include. | Meta-only; no ShopDirector domain content. Must be combined with domain-specific patterns later. | Yes |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/skill-share/` | `skill-share` | Knowledge & Skill Architecture Skill | Adds ideas about validation, packaging, and team-level sharing/distribution workflow. | Slack/Rube-centric and automation-heavy. Trust boundary is weak for local-first design. | Maybe |
| `awesome-codex-skills` | `research/open_source_skills/raw/awesome-codex-skills/template-skill/` | `template-skill` | Knowledge & Skill Architecture Skill | Minimal reminder of the absolute required shape for a skill folder. | Too skeletal to learn much beyond required file presence. | No |
| `codex` | `research/open_source_skills/raw/codex/.codex/skills/code-review/` | `code-review` | Product Critic Skill | Useful orchestration pattern: split critique into lenses/subskills and aggregate all findings without collapsing severity. | Narrowly designed for PR review on code, not product artifacts. | Yes |
| `codex` | `research/open_source_skills/raw/codex/.codex/skills/code-review-breaking-changes/` | `code-breaking-changes` | Product Critic Skill | Good specialized critique lens for external surface regressions and compatibility impact. | Code/API specific. Needs reframing for product strategy or workflow critique. | Yes |
| `codex` | `research/open_source_skills/raw/codex/.codex/skills/code-review-context/` | `code-review-context` | Product Critic Skill | Good example of a narrow, high-signal review lens focused on bounded context, scale limits, and hidden system costs. | Extremely implementation-specific to Codex context mechanics. | Maybe |
| `awesome-agent-skills` | `research/open_source_skills/raw/awesome-agent-skills/README.md` | `Product Manager Skills by Dean Peters` (catalog only) | Product Strategy Skill | Indicates a large external PM skill collection focused on opportunity framing, validation, and killing weak bets. Worth selective fetch later. | No local skill files were downloaded here, so there is nothing inspectable/adaptable yet. | No, not until fetched |
| `awesome-agent-skills` | `research/open_source_skills/raw/awesome-agent-skills/README.md` | `Product Management Skills by Paweł Huryn` (catalog only) | Product Strategy Skill | Signals broader PM lifecycle coverage: discovery, strategy, execution, analytics, GTM. Worth selective fetch later. | Catalog pointer only; no local source content available for inspection. | No, not until fetched |
| `awesome-agent-skills` | `research/open_source_skills/raw/awesome-agent-skills/README.md` | `Marketing Skills by Corey Haines` (catalog only) | Content Commerce Strategy Skill | Signals likely future source material for content strategy, copywriting, analytics, and acquisition workflows. | Catalog pointer only; no local source content available for inspection. | No, not until fetched |

## Duplicates Worth Noting

- `notion-spec-to-implementation` exists in both `awesome-codex-skills` and `skills/.curated`.
- `notion-research-documentation` exists in both `awesome-codex-skills` and `skills/.curated`.
- `notion-knowledge-capture` exists in both `awesome-codex-skills` and `skills/.curated`.
- `notion-meeting-intelligence` exists in both `awesome-codex-skills` and `skills/.curated`.
- `skill-creator` appears in `skills/.system`, `awesome-codex-skills`, and `codex` sample assets.

Recommended default when duplicates exist:
- Use `skills` for the most official baseline structure.
- Use `awesome-codex-skills` for richer `reference/`, `examples/`, and `evaluations/` directories.

## Preliminary Shortlist

If Step 2 later becomes "select the strongest raw inputs for adaptation", the highest-value local references appear to be:

1. `skills/skills/.system/skill-creator/`
2. `awesome-codex-skills/notion-spec-to-implementation/`
3. `awesome-codex-skills/notion-research-documentation/`
4. `awesome-codex-skills/notion-knowledge-capture/`
5. `awesome-codex-skills/mcp-builder/`
6. `awesome-codex-skills/lead-research-assistant/`
7. `awesome-codex-skills/competitive-ads-extractor/`
8. `awesome-codex-skills/developer-growth-analysis/`
9. `awesome-codex-skills/langsmith-fetch/`
10. `codex/.codex/skills/code-review/`

## Bottom Line

The strongest local raw material is not a single repo but a combination:
- `skills` for official skill-shape and concise meta patterns.
- `awesome-codex-skills` for practical research, planning, knowledge capture, GTM, and evaluation workflows.
- `codex` for critique decomposition patterns.
- `awesome-agent-skills` only as a fetch-later map for PM/marketing collections not yet present locally.
