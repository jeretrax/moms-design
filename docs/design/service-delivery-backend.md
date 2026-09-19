# Service Delivery Backend

Status: user-requested backend design expansion, 2026-09-19. Requirement R-026. These are MOMS requirements and proposed implementation contracts, not a description of Search Berg's private software. [Reference review](../reference/searchberg-capability-review.md).

## Purpose and ownership

Run managed marketing services through one customer/goal/work/approval/measurement model. An engagement coordinates human, vendor and automated delivery. Existing Marketing Work Items remain the action records; engagement tasks reference them. Service packages configure capability entitlements, deliverable types and cadence without hard-coded prices or vendor promises.

| Logical component | Owned responsibility | Durable records |
| --- | --- | --- |
| Service catalog and engagement service | Version scope, expected deliverables, periods, responsible manager and acceptance conditions | OfferingVersion, ServiceEngagement, DeliveryCycle |
| Work orchestration | Instantiate bounded work from approved templates; route specialist/human/automation assignments | WorkflowVersion, WorkAssignment, Dependency, Job |
| Collaboration | Collect briefs, customer requests and text/audio feedback with explicit internal/customer visibility | FeedbackRevision, Attachment, DecisionRequest |
| Deliverable registry | Link artifacts, quality checks and acceptance to canonical work | DeliverableRevision, QualityReview |
| Policy/action gateway | Validate current authority and reserve allowed resources before external action | Existing Approval, SpendPolicy, Execution; new CostReservation |
| Evidence and reporting | Join performed work to sources, results and cycle reports | Existing Observation, Measurement and Report |
| Usage and service cost | Record model/provider/human/vendor costs, allowance use and commitments | UsageEntry, CostEntry, Reservation |

These are logical boundaries. A modular application with workers may implement them; separate microservices are not mandated. D-011 governs technology choices.

## Proposed engagement workflow

Accepted scope → onboarding/access readiness → active delivery cycle → work and quality review → customer acceptance where required → cycle report → next authorized cycle or closure. Paused, waiting-customer, blocked and cancelled conditions suspend relevant scheduling. Final status names and role permissions require D-019; transition invariants below are requirements.

Each cycle is generated once for an engagement and period. A scope change creates a new version and explicitly reconciles pending work; it does not rewrite previous commitments. Account managers assign work to approved internal staff or scoped vendors. Completing a human task requires artifact/evidence and reviewer outcome, not simply elapsed time. Feedback attaches to exact artifact revisions. Audio transcripts are derivative records and do not grant action authority.

## Proposed API/event contracts

| Command or query | Required context | Outcome |
| --- | --- | --- |
| CreateEngagement | Authorized customer, offering/scope version, accepted proposal if present | Stable engagement; no automatic external action |
| StartDeliveryCycle | Engagement, period, template version, idempotency key | One cycle and linked work references |
| AssignWork / SubmitDeliverable | Work ID, actor, expected revision, artifact refs | Version-checked assignment or reviewable submission |
| ApproveAction | Action digest, target/account, scope, approver, expiry policy | Approval bound to immutable proposed action |
| ExecuteAction | Work/action revision, current grant, cost reservation | Audited queued execution or explicit rejection |
| GetCycleReport | Customer access, cycle and report revision | Scoped report from recorded outcomes |

Events include CycleStarted, DeliverableSubmitted, ReviewRequested, ActionAuthorized, ExecutionVerified and CycleClosed. Each envelope carries event ID, schema version, customer ID, aggregate ID/revision, occurred/received time and correlation/causation IDs. These are proposed contracts, not deployed API endpoints.

## Runtime and failure handling

Persist canonical changes and an outbox event in one transaction. Workers use leases, bounded retries and idempotent consumers; recover expired leases without assuming external failure. Recheck permissions and cancellation at execution time. Use provider idempotency where supported and reconcile by remote reference otherwise. Ambiguous outcomes enter reconciliation, never automatic success or blind replay. Failed jobs retain an error category and an operator-visible recovery task; retries consume bounded budgets.

Durable relational records hold identities and state; scoped object storage holds artifacts/evidence; a durable queue drives jobs; metrics/read projections serve reporting. These are proposed storage roles, not selected products. Preserve revision history, audit integrity and customer filters across all stores, caches and exports. Secrets use credential references. Provider callbacks authenticate, deduplicate and reject invalid customer/account associations.

## Operations

Measure queue age, retries, denied actions, provider sync lag, token expiry, evidence availability, actual versus reserved costs and unresolved outcomes. Alert operators using configured policy. Customer/connection/action kill switches stop new writes and require reconciliation for in-flight operations. Establish backups, restore checks, retention/deletion and recovery objectives before production; numeric targets remain D-024.

## Acceptance

SD-01: Replaying a cycle-start event produces one cycle and one intended set of work references.

SD-02: A revoked or paused engagement cannot execute queued external actions.

SD-03: A reviewer can trace scope → work → artifact revision → approval → execution → evidence → report without duplicate customer records.

SD-04: Worker recovery and webhook replay do not duplicate external delivery; ambiguous outcomes remain unresolved until verified.

SD-05: Cross-customer artifact, event, job and report access fails, including guessed identifiers.

See [channel design](multichannel-campaign-backend.md), [roadmap](managed-marketing-backend-expansion.md) and [controls](autonomy-approvals-and-spend-controls.md).

## Research and case routing

[Findings/alerts](consumer-and-market-intelligence.md) and [engagement cases](engagement-inbox-and-cases.md) reuse WorkAssignments, deliverable review and verified execution. A case groups context; it does not create a competing task engine. Analyst reviews and creator deliverables are typed work on existing engagement cycles. Scheduled briefings use report delivery; alert notifications do not acquire a second send queue.
