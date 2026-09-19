# MOMS Agent and Autonomy Handoff

## Purpose

Define how AI operates inside MOMS without making the customer manage or
understand AI agents.

## Customer Abstraction

Customers purchase a marketing service.

They should not need to select models, write agent prompts, understand
tool calls, or operate an agent framework.

MOMS internally decides which specialized capability performs a task.

## Agent Operating Pattern

Agents should normally run as bounded jobs rather than as permanently
active token-consuming processes.

Typical triggers:

-   New customer assessment
-   Customer changes business goal
-   Scheduled weekly analysis
-   New Search Console/Analytics/Ads data
-   Material performance change
-   Budget pacing condition
-   New approval
-   New campaign
-   Scheduled monthly report

## Logical Agent Roles

These are internal responsibilities, not necessarily separate software
processes in V1.

### Business Intent Analyst

Converts ordinary-language customer goals into structured marketing
objectives.

### Search Research Analyst

Develops search intents, keyword/topic families, SERP observations, and
competitor discoveries.

### Website Analyst

Crawls and evaluates the customer's website.

### SEO Strategist

Turns evidence into prioritized organic recommendations.

### Paid Search Analyst

Analyzes Google Ads, candidate keywords, CPC, budgets, search terms, and
campaign performance.

### Presence and Authority Analyst

Finds relevant directories, communities, social properties,
associations, citation opportunities, and legitimate participation
opportunities.

### Content Strategist

Identifies content gaps and produces briefs/drafts.

### Measurement Analyst

Compares baselines, expected benefit, and actual results.

### Marketing Planner

Reconciles findings from other capabilities into the prioritized
Marketing Work List.

## Deterministic Controls

AI reasoning must not be the sole enforcement mechanism for:

-   Ad spending ceilings
-   Authentication/authorization
-   Approval requirements
-   Customer isolation
-   API permissions
-   Allowed actions
-   audit logging
-   subscription entitlements
-   rate limits
-   publication permissions

These must be enforced by application logic.

## Autonomy Levels

MOMS should support progressively greater autonomy.

### Level 0 - Observe

Read and analyze only.

### Level 1 - Recommend

Create recommendations and work items.

### Level 2 - Draft

Prepare content/configuration for approval.

### Level 3 - Execute With Approval

Execute a specific approved action.

### Level 4 - Standing Authorization

Execute approved classes of actions inside deterministic limits.

Autonomy is granted per customer, integration, capability, and action
type. It is not a single global on/off switch.

## Google Ads Safety Boundary

Initial implementation should be read-only.

When write support is introduced:

-   Require explicit account authorization.
-   Enforce hard spend ceilings in application logic.
-   Log before/after state.
-   Record who or what approved the action.
-   Verify the result after execution.
-   Allow customers/internal operators to revoke write authority.
-   Do not allow the language model to redefine spending policy.

## Data Sources

MOMS should be designed to combine data from sources such as:

-   Public website crawl
-   Search engine result observations
-   Google Search Console
-   Google Analytics
-   Google Business Profile
-   Google Ads
-   keyword/search-volume/CPC data providers
-   PageSpeed/performance data
-   DNS/public-domain information where relevant
-   approved social/business directory sources

Data provider selection should remain replaceable behind provider
interfaces where practical.

## AI Provider

The initial implementation may use OpenAI as the reasoning/model
provider.

Do not couple the canonical product/domain model directly to one model
version. Model and tool providers are implementation dependencies, not
the product's conceptual data model.

## Auditability

For consequential recommendations and actions, preserve enough context
to answer:

-   What did MOMS observe?
-   What evidence did it use?
-   What did it recommend?
-   Why was it prioritized?
-   Who approved it?
-   What action occurred?
-   What did it cost?
-   What changed afterward?
