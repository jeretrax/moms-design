# System Architecture

Status: proposed logical architecture derived from the handoffs. This document does not approve a language, framework, database, hosting provider, agent SDK, or deployment topology.

## Logical components

| Component | Responsibility |
| --- | --- |
| Intake and customer experience | Capture business context and render work/report views |
| Application service | Validate inputs, enforce customer access and entitlements, own canonical records |
| Job orchestration | Run bounded assessment stages with progress, retries and cost limits |
| Provider adapters | Public crawl, current search, optional metrics and connected properties |
| Analysis capabilities | Produce structured, evidence-linked findings and recommendations |
| Marketing planner | Reconcile findings and produce prioritized work items |
| Report and measurement service | Persist readable snapshots, forecasts and baselines; later compare results |
| Policy/action gateway | Independently authorize future writes and enforce budget/action rules |
| Data and audit persistence | Preserve customer records, provenance, versions and accountability |

## M1 data flow

Validated intake creates customer/property/goal context and assessment job. The crawl and search adapters collect dated observations. Analysis derives search intent and evidence-linked findings. The planner creates the work list and benefit hypotheses. Report generation renders the same saved work-item revisions, and the assessment persists its baseline and coverage.

Stage boundaries should preserve enough state to resume bounded failures and avoid duplicate output. Raw provider responses and extracted facts should be distinguishable from generated summaries. Customer-visible progress reflects recorded job state.

## External-action boundary

Future agent output proposes actions; it does not invoke unguarded provider mutations. A deterministic gateway validates current policy, permissions and approval before a write, then records verification. Read-only M1 should have no external write capability wired into its workflow.

## Decisions before deployment

Select runtime, database, queue/job design, hosting, account/membership model, source vendors, credential storage and operating limits through [design notes](design-notes.md). An isolated engineering prototype may use documented replaceable implementations, but it cannot declare unresolved production behavior approved.

See [provider contracts](integrations-and-provider-interfaces.md), [agent model](agent-operating-model.md), [security](security-and-data-handling.md), and [EWP-001](../engineering/EWP-001-public-domain-assessment.md).

## Expansion integration

The [agency growth capabilities](agency-growth-expansion.md) extend existing services: strategy/visibility use research and measurement; content/proposals produce versioned artifacts; portfolio/reporting apply scoped views; CMS/outreach/delivery/commerce use declared adapters and the policy gateway. Reuse persistence, audit and job controls. Add event reconciliation for external callbacks and ambiguous execution outcomes; do not create parallel customer or approval stores.

## Managed-service backend

The [service delivery backend](service-delivery-backend.md) owns engagement/cycle orchestration, proposed command/event contracts, durable jobs, transactional outbox, execution reconciliation and cost reservations. [Channel backends](managed-marketing-backend-expansion.md) reuse the existing application, policy gateway, evidence and provider boundaries. Components remain logical responsibilities, not a mandatory microservice deployment.
