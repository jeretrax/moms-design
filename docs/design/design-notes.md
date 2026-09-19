# Design Notes and Open Decisions

Status: unresolved items, not approved defaults. Product owner: Jeremiah; engineering supplies options/evidence. Prepared 2026-09-18 from five supplied handoffs.

## Reconciliation decisions grounded in sources

- The three-function MVP is a roadmap; the first EWP remains public assessment only (H1/H3/H5).
- Expected benefit and measurement plans belong in M1; ongoing actual-versus-forecast evaluation follows later (H3).
- Google Ads read/recommend and controlled execution are retained as product design but excluded from EWP-001 (H3/H5).
- Logical agent responsibilities do not require separate processes; customer workflows do not expose agent administration (H4).
- Required assessment fields come from H3; broader business intake in H2 is retained without requiring keywords or connected accounts.
- Work items are canonical recommendations referenced by reports; original handoffs remain unchanged reference material.
- No unresolved commercial terms, numeric limits, stack, provider or production access policy has been promoted to an approved decision.

## Decision register

| ID | Unresolved decision | Gate / impact |
| --- | --- | --- |
| D-001 | Customer identity, login/provisioning, memberships, operator/customer roles, multi-business access and approval authority | Before production access or approvals; isolated development can proceed |
| D-002 | Search/SERP and keyword/CPC providers, API access, licensing, geography support and cost | Before live M1 search acceptance; fixture-based adapter work can proceed |
| D-003 | Crawl policy, pages/depth, robots handling, render strategy, timeouts, source/job/model budgets, retry/rate limits | Before live collection; no unlimited crawl or spend assumption |
| D-004 | Subscription tiers, prices, entitlements, cadence, trial, billing, cancellation and human labor | Before commercial launch or billing work |
| D-005 | Evidence/raw content retention, deletion, privacy, residency, security operations and audit retention | Before production customer data |
| D-006 | Priority ordering policy, optional scoring, effort/cost/confidence scales | Before accepting production ranking behavior; rationale-based prototype is provisional |
| D-007 | Work statuses, approval roles/transitions, expiry, standing authorization and revocation semantics | Before operational work execution; M1 recommendations need no external execution |
| D-008 | Report format/branding/export, customer delivery, acceptable partial-result publication and review policy | Before final report UX acceptance and customer release |
| D-009 | Metrics, attribution, useful sample/window thresholds and recurring measurement schedule | Before automated claims of measured effectiveness; M1 still records hypotheses |
| D-010 | Budget periods/currencies, account/campaign ceiling semantics, external edits, provider lag, enforcement and emergency pause | Hard gate before any Ads writes |
| D-011 | Runtime, hosting, persistence, orchestration, AI model configuration and credentials | Before deployable implementation; conceptual design is provider-neutral |
| D-012 | Website/domain ownership verification and consent requirements for public assessments versus connected properties | Before self-service production assessment/connection |
| D-013 (resolved) | Confirm remote location/access and visibility for moms-design | Resolved 2026-09-19: user directed publication to `jeretrax/moms-design`; repository is public and connected account has push/admin access |

## Capability expansion decision: 2026-09-19

Jeremiah requested additional features comparable to Adaptify. [R-018 through R-025](agency-growth-expansion.md) are added to product scope based on the [public reference review](../reference/adaptify-capability-review.md). They extend the five-handoff baseline. M1 and EWP-001 remain unchanged; exact implementation and numerical policy choices are not approved by analogy to a vendor.

D-008 is partially resolved: branded PDFs and recurring delivery are future requirements, while format specifics, access, cadence and partial-result policy remain open. D-004 now includes proposal/payment integration and expansion entitlements; no pricing is selected.

| ID | Open decision | Gate |
| --- | --- | --- |
| D-014 | AI collection surfaces/providers, prompt sampling, score definitions, retest cadence and costs | Before production visibility claims |
| D-015 | CMS rollout, editorial checks, brand policy, revision limits, author/media rules and publication approvals | Before content production/publishing release |
| D-016 | Outreach sender/recipient policy, suppression, permitted placements, costs and corrective service terms | Before outbound outreach or purchased placement |
| D-017 | Agency memberships, portal sharing/authentication, domain ownership, delivery recipients and schedules | Before customer portal/report delivery |
| D-018 | Quote/catalog rules, signatures/payments, refunds, activation and consent for proposal analytics | Before commercial proposal execution |

## Resolved repository decision

D-013 originally blocked remote publication. On 2026-09-19, Jeremiah directed the completed design into the now-accessible `jeretrax/moms-design` repository. Its existing public visibility is preserved. This resolves destination/access only; product, pricing, provider and production release decisions remain unchanged. The previous ZIP is a historical bootstrap snapshot, not the ongoing source of truth.

## Not imported

No prices or feature promises from unrelated prototypes are part of this baseline. No exact Google API endpoint/version or current API capability is asserted. Engineering must verify current provider documentation at integration time.

## Future decision entry

For each resolution record decision ID, date, owner/approver, choice, rationale, affected requirement/document/EWP, and any migration or acceptance impact. Retain the original question and decision history.

See [governance](design-to-implementation-governance.md) and [first EWP](../engineering/EWP-001-public-domain-assessment.md).

## Managed-service backend decision: 2026-09-19

Jeremiah requested the backend required to support services comparable to Search Berg. [R-026 through R-034](managed-marketing-backend-expansion.md) add capability requirements and explicitly proposed architecture/contracts. Public service descriptions do not reveal the competitor's internal implementation. M1/EWP-001 remain unchanged; this authorizes design, not sending campaigns, buying services or deploying infrastructure.

| ID | Open decision | Gate |
| --- | --- | --- |
| D-019 | Service catalog/version rules, cycle status transitions, ownership, capacity, acceptance and change orders | Before managed-service production |
| D-020 | Paid/marketplace provider rollout, supported account types, permissions and normalized metrics | Before each channel integration/write release |
| D-021 | Social/inbox/moderation roles, email consent/retention/suppression policy, influencer rights and compensation | Before social/email/creator execution |
| D-022 | Location verification, review request/response policy, reputation privacy and provider dispute handling | Before local/reputation production |
| D-023 | Web/hosting responsibility, deployment authorization, catalog ownership, media rights and creative acceptance | Before delivery integrations and production release |
| D-024 | Backend technology/topology, queues/storage, operating budgets, backup/restore and recovery objectives | Before production backend deployment; extends D-011 |
| D-025 | Tracking consent, CRM source ownership, lead/call scope, event identity and attribution rules | Before outcome ingestion and effectiveness claims; extends D-009 |
