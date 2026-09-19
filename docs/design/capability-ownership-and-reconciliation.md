# Capability Ownership and Reconciliation

Status: user-directed consolidation, 2026-09-19. R-040. Integrate Brandwatch-like functions into existing MOMS capabilities, preserving useful specializations. [Reference review](../reference/brandwatch-capability-review.md). This supersedes earlier overlapping ownership descriptions; original requirement IDs remain valid.

## Canonical ownership

| Capability | Canonical owner | Reused by / boundary |
| --- | --- | --- |
| Evidence collection and research queries | [Intelligence](consumer-and-market-intelligence.md) with existing Observation store | Listening, search, reputation and competitor views reference observations; no separate raw-data silos |
| Keyword/topic planning | [Strategy](keyword-and-topic-strategy.md) | Uses demand evidence; does not own publishing or a separate calendar |
| AI-answer testing | [AI visibility](ai-search-visibility.md) | Owns prompt/sample methods; intelligence correlates references, never treats responses as search volume |
| Content revisions, calendar and publication coordination | [Content](content-production-and-publishing.md) | Social/CMS/email channel plans reference the same revisions and Calendar Entries |
| Media artifacts and rights | [Creative backend](web-commerce-and-creative-backend.md) | Shared asset library; no social-specific copy of media storage |
| Inbound interactions and response work | [Engagement inbox](engagement-inbox-and-cases.md) | Social comments/messages, review-response projections and authorized channel replies; never a second social/reputation inbox |
| Audience consent and promotional email | [Social/email backend](social-email-and-community-backend.md) | Remains distinct from market-research cohorts and operational replies |
| Creator lifecycle | [Creator relationships](creator-relationship-management.md) | Extends existing InfluencerEngagement; outreach transports and commercial controls are shared |
| Listing corrections and review disputes | [Local/reputation](local-presence-and-reputation-backend.md) | Retains source-specific business rules; references shared evidence and cases |
| Issue detection and analyst briefings | [Intelligence](consumer-and-market-intelligence.md) | Creates findings/cases/work, not a second notification or report-delivery service |
| Paid execution and funding | [Campaign backend](multichannel-campaign-backend.md) | A social boost is an ad action under the same gateway and allocation policy |
| Metric definitions and comparisons | [Measurement](measurement-and-crm-backend.md) | Benchmark views use shared definitions and snapshots; no separate analytics warehouse authority |
| Report rendering, branding and delivery | [Agency reporting](agency-portal-and-reporting.md) | Research briefings, benchmark exports and cycle reports use the same snapshots and access policy |
| Work assignments, jobs and review | [Service delivery](service-delivery-backend.md) | Research, engagement cases and creator deliverables reference existing work items |

## Before-to-after reconciliation

- Replace the inline social-inbox design with the engagement owner and a cross-reference. Its original SE acceptance criteria still apply to channel transport.
- Move the inline influencer lifecycle into the creator owner; preserve InfluencerEngagement identity and rights/compensation controls.
- Replace standalone review-reply language with the shared inbox plus reputation-specific policy. Review facts remain observations; cases group response work.
- Replace strategy calendar ownership with a view of canonical Calendar Entries. Content owns scheduling state; channel adapters own transport outcomes.
- Route all benchmark calculations to measurement and all briefing delivery to reporting. Research produces referenced findings, not detached scores or emails.

## Data reconciliation and rollout

This is a design refactor, not a claim of a live database migration. If prototypes exist, inventory duplicate identifiers before migration. Preserve source IDs, historical revisions, access grants and approval digests; merge only verified same-source records. Use an explicit old-to-canonical mapping and replay checks. Ambiguous entity matches require review. No display-name match may combine people across channels or customers.

Suggested sequence: canonical ownership/contracts first; licensed read-only intelligence/benchmarks next; inbox and creator workflows after identity/permission decisions; then separately gated actions. EWP-001 remains unchanged. New bounded EWPs must reference retained R-018 through R-034 plus applicable R-035 through R-040.

## Acceptance

CO-01: The same provider item used by research, reputation and an inbox has one canonical observation identity, scoped authorized projections and preserved lineage.

CO-02: Updating a calendar entry changes strategy/social/CMS views of that entry without creating duplicate scheduled executions.

CO-03: A finding generates or links one canonical work item/case according to a stable deduplication rule; every report uses the same metric snapshot.
