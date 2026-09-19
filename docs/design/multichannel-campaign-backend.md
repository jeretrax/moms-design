# Multichannel Campaign Backend

Status: user-requested capability expansion; R-027. Reference: [Search Berg paid marketing](https://www.searchberg.com/ppc-marketing/). Comparable service areas include search, display, shopping, remarketing and video advertising with campaign analysis and landing-page work. Candidate integrations extend Google Ads with Meta, Microsoft Advertising and Amazon Ads; actual channel support requires verification.

## Backend requirements

CampaignPlan links customer, goal, external accounts, channel-specific configuration, creative revisions, landing pages, forecast and approved funding. Keep normalized summaries alongside original provider identifiers and metric definitions. Do not force incompatible account/ad-group/audience structures into one lossy schema. Read/sync adapters precede mutation adapters for each channel. Missing access and unsupported operations are explicit capability states.

Maintain per-channel budgets and an aggregate customer media policy. Amounts carry currency, accounting period, timezone and source timestamp. Atomic reservations prevent two MOMS jobs from independently allocating the same remaining allowance. Concurrent/external provider edits and billing lag still require reconciliation; reservations do not guarantee a provider billing cap. No budget is reallocated between channels without authority covering both the source and destination. Keep service fees, media spend, vendor costs and model usage separate.

Track campaign drafts, creatives, targeting, schedules, landing-page revisions and proposed changes. Activation requires authorized account binding, compatible creative approval, measurement-readiness checks and the applicable spending policy. Provider disapproval is a distinct status, not a successful launch. Audience upload, retargeting and tag installation have separate purpose/permission checks. Anomaly findings create reviewable work; they do not prove fraud or authorize blocking users.

## Acceptance

MC-01: Two simultaneous reservations cannot exceed the MOMS-controlled remaining allocation.

MC-02: A revoked channel connection blocks writes; reporting distinguishes stale data and unknown spend.

MC-03: Cross-channel transfers require explicit permitted scope; approval for one account cannot be reused on another.

MC-04: A provider rejection or ambiguous response cannot be reported as an active campaign.

See [Google Ads](google-ads-management.md), [attribution](measurement-and-crm-backend.md), and D-010/D-020 in [decisions](design-notes.md).
