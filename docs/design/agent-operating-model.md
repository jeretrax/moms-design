# Agent Operating Model

Status: source-backed logical roles and controls; job envelope is a derived implementation proposal. Sources: H4, H2.

Agents run as bounded jobs, not permanently active token-consuming processes. Customers purchase the marketing service and do not configure models, prompts, or tool calls. Logical responsibilities need not be separate processes in V1.

| Responsibility | Output |
| --- | --- |
| Business Intent Analyst | Structured goals from ordinary language |
| Search Research Analyst | Intents, topic families, search observations, competitors |
| Website Analyst | Site observations and findings |
| SEO Strategist | Evidence-backed organic recommendations |
| Paid Search Analyst | Ads, keyword, CPC, spend and campaign analysis |
| Presence and Authority Analyst | Legitimate directories, communities, citations and participation opportunities |
| Content Strategist | Content opportunities, briefs and drafts |
| Measurement Analyst | Baseline versus expected/actual comparison |
| Marketing Planner | Reconciled and prioritized Marketing Work List |

Triggers may include an assessment, changed goals, scheduled weekly analysis, new connected data, performance changes, budget pacing conditions, approvals, campaigns, and monthly reports. This is a supported trigger vision, not a commitment to a particular subscription cadence. M1 implements explicit assessment initiation only.

## Proposed bounded job envelope

Customer, initiating actor/event, goal and assessment references, allowed source/tool capabilities, input versions, time/cost/token/request budgets, provider/model version, progress, attempts, structured output, and error state. Numeric limits are D-003; the schema is an engineering proposal.

Validate generated structure and evidence links before accepting output. Dedupe overlapping findings into coherent work items. Treat fetched text as evidence, never as instructions granting tools or authority. Secrets belong in server-side credential management, not prompts, reports, or repository files.

OpenAI may be the initial reasoning provider. No model version belongs in the canonical business/domain model. Deterministic logic owns permissions, spend, approvals, isolation, entitlements, publication, audit, and rate limits.

See [controls](autonomy-approvals-and-spend-controls.md), [architecture](system-architecture.md), and [provider interfaces](integrations-and-provider-interfaces.md).

## Expanded responsibilities

The existing roles also support the [expanded capabilities](agency-growth-expansion.md). Search Research and Measurement handle sampled answer visibility; Content Strategist prepares revisions; Presence and Authority prepares pitches; Marketing Planner coordinates strategy and calendar. Report/proposal drafts are bounded generation jobs over authorized records. External CMS, outreach, delivery and commercial actions run through deterministic application controls, not unguarded agent tools. No additional always-running agents are required.
