# Managed Marketing Backend Expansion

Decision scope: 2026-09-19 user request to add the backend needed for Search Berg-like services. This document extends the [Adaptify-informed expansion](agency-growth-expansion.md). It specifies capability requirements and proposed backend contracts, not running software or knowledge of Search Berg's private architecture.

[Reference review](../reference/searchberg-capability-review.md) separates publicly advertised service areas from MOMS engineering design. Existing SEO assessment, strategy, content, AI visibility, outreach, reports and proposals retain their owners.

| Requirement | Backend capability | Delivery output | Dependency |
| --- | --- | --- | --- |
| R-026 | [Service delivery](service-delivery-backend.md) | Engagements, recurring cycles, assignments, review, costs, runtime recovery | Shared records/policy; D-019/D-024 |
| R-027 | [Multichannel campaigns](multichannel-campaign-backend.md) | Paid-channel plans, observed performance, controlled execution | Google Ads foundation; D-010/D-020 |
| R-028 | [Social/community](social-email-and-community-backend.md) | Channel publishing, inbox, moderation and influencer work | Content, identity, action gateway; D-021 |
| R-029 | [Email operations](social-email-and-community-backend.md) | Audiences, consent, suppression, campaigns and feedback | Sender/recipient policy; D-021 |
| R-030 | [Local/reputation](local-presence-and-reputation-backend.md) | Location facts, listing changes, review cases and responses | Evidence, ownership and access; D-022 |
| R-031 | [Web delivery](web-commerce-and-creative-backend.md) | Development, maintenance, hosting and release engagements | Scoped project/release authorization; D-023 |
| R-032 | [Commerce](web-commerce-and-creative-backend.md) | Catalog references, listing/feed changes and promotion work | External catalog ownership; D-020/D-023 |
| R-033 | [Creative production](web-commerce-and-creative-backend.md) | Reviewed media assets with rights and revision lineage | Artifact store, workers, reviewers; D-023 |
| R-034 | [Measurement/CRM](measurement-and-crm-backend.md) | Tracking plans, conversions, outcomes and attributed reporting | Consent and metric definitions; D-009/D-025 |

## Phasing and engineering handoff

Keep EWP-001 assessment scope unchanged. Reuse its canonical records as the foundation. Next backend package candidates are engagement/cycle orchestration and read-only measurement ingestion, followed by channel-specific read adapters and drafting, then separately gated mutations. These are dependency suggestions, not approved release dates or executable work packages.

Before implementation, create bounded EWPs using the existing template and map the acceptance IDs in each owner document. Do not bundle every channel into one engineering milestone. Human-assisted delivery must be a first-class supported mode for unavailable APIs, design work, specialist judgments and provider disputes.

Backend gates include account/access verification, applicable service scope, provider capability support, source/evidence availability, action authority, commercial limits and verified outcomes. Catalog selection cannot bypass any gate.

## Service coverage reconciliation

National/international and industry SEO are strategy scope and locale/geography dimensions. On-page audits, technical work and backlink analysis remain existing assessment/authority capabilities. Suspect-link removal or disavowal is a reviewed specialist action, never automatically triggered by a score. Guest posts and press releases use existing content/outreach with rights and approval controls. White-label service delivery reuses the agency portal.

Website/application delivery is managed project orchestration with scoped specifications; MOMS does not promise to recreate every application backend, host infrastructure itself or replace the customer's CRM/store operations.

## Cross-capability acceptance

MB-01: One accepted engagement can coordinate research, creative and channel work without creating duplicate customer, budget or approval records.

MB-02: Cycle reports distinguish proposed, submitted, verified and measured results, including human delivery evidence.

MB-03: A provider outage, expired credential or revoked grant produces visible blocked/recovery work without silent data fabrication or external replay.
