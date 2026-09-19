# Marketing Work Item

Status: source-backed required fields and capability classes; storage shape and lifecycle proposal are provisional. Sources: H2, H3, H4.

A Marketing Work Item is the canonical actionable recommendation. Reports, opportunities, agent findings, and later executions reference it rather than maintaining competing copies of its action and status.

| Field | Meaning |
| --- | --- |
| ID; customer; goal | Stable identity and business context |
| Category; title; description | Kind of work and plain-language summary |
| Evidence | References to observations, sources, dates, and scope; explicit hypothesis if unverified |
| Recommended action | Concrete proposed work |
| Proposed benefit | Expected business/marketing effect and rationale |
| Expected measurement window | Activation/near-term/longer-term class plus useful window and assumptions |
| Estimated cost | Amount/range if available, currency, basis, and unknown reason otherwise |
| Estimated effort | Estimated labor/complexity with basis or unavailable reason |
| Priority; confidence | Relative importance and evidence confidence, each with rationale |
| Dependencies | Preconditions and related work item references |
| Execution capability | One of the five source-defined classes below |
| Approval requirement | Required authorization for the proposed action |
| Status | Work progress, separate from approval and integration state |
| Measurement method; baseline; result | Planned metric/source, starting observation, later result |
| Created date; last evaluated date | Creation and most recent evaluation timestamps |

## Execution capability

Informational only; Human task; Agent can draft; Agent can execute with approval; Agent can execute within standing authorization.

Capability describes technical ability, not permission. Effective execution authority additionally requires current customer, integration, capability, action-type, entitlement, approval, and spend controls.

## Prioritization

Explain relevance to the goal, observed severity/opportunity, plausible benefit, effort/cost, dependencies, and evidence confidence. The handoffs require priority but do not approve a weighted score or a numeric scale. Proposed M1 presentation is an ordered work list with a concise rationale; final scoring policy is D-006.

## Proposed lifecycle

Proposed → awaiting decision → ready → in progress → completed → measuring → evaluated, with rejected, cancelled, and blocked outcomes as needed. This is not an approved status enumeration. M1 only needs persisted recommendations; engineering must not introduce future execution transitions as approved behavior. Final transitions and approval-state separation require D-007.

Record new evidence and revised forecasts as later evaluations rather than overwriting what the customer was originally told. Completed work can have an inconclusive result; measurement does not imply success.

See [domain model](domain-model.md), [controls](autonomy-approvals-and-spend-controls.md), and [benefit model](benefit-and-time-model.md).
