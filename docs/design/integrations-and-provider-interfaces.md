# Integrations and Provider Interfaces

Status: replaceable providers are source-backed; interface shape is proposed. Sources: H4, H3.

| Source | Intended use | Phase |
| --- | --- | --- |
| Public website crawl | Technical/content/structure observations | M1 |
| Current search observations | Intent validation and visible competitor evidence | M1 |
| Keyword/volume/CPC sources | Available demand and paid planning estimates | M1 where available; deepen in M2 |
| Performance/PageSpeed source | Available site performance measurements | Assessment enrichment |
| DNS/public domain data | Relevant domain observations | Assessment enrichment |
| Search Console | Authorized search performance | Later connected measurement |
| Analytics | Authorized traffic/conversion measurements | Later connected measurement |
| Business Profile | Authorized local presence information | Later connected capability |
| Google Ads | Account read/recommend, then separately gated writes | M2 / later Phase B |
| Approved directory/social sources | Legitimate presence and authority observations | Available assessment / later expansion |

## Proposed adapter contract

Requests include customer/job context, requested capability, query/property/account, geography, date range and bounded resource allowance. Results identify provider, request/capture time, scope, normalized observations, provenance references, units/currency, coverage, quota/cost metadata where available, and classified errors.

Differentiate unauthorized, unavailable, rate-limited, invalid input, partial, and failed responses. Do not silently replace live search results with model-generated knowledge. Missing data must propagate to the report and confidence assessment.

Secrets remain server-side and account scoped. Validate that a connection belongs to the current customer. Track authorized read/write capabilities independently. Revocation prevents future use. Availability of a provider feature is not implied by its presence in this table.

Provider selection requires checking current official APIs, permissions, access eligibility, licensing, quotas and supported fields. This repository has not selected a provider or verified current API endpoints. See D-002 and D-011 in [design notes](design-notes.md).

## Expansion adapters

The [capability expansion](agency-growth-expansion.md) adds AI-answer collection, CMS, media provenance, outreach/email delivery, backlink observation, signature and payment adapters. Each declares supported operations, read/write authority, account/customer binding, quota, idempotency/reconciliation behavior and evidence availability. A named candidate integration is not a support claim.

CMS and AI-platform coverage require current capability verification. Treat payment webhooks as untrusted until authenticated and deduplicated. Delivery adapters must enforce current recipient access and suppression policy. No adapter may turn a recommendation or commercial payment into write authority.

## Managed-service adapter additions

[Backend expansion](managed-marketing-backend-expansion.md) adds social publishing/inbox, email campaign delivery, local listings/reviews, marketplace feeds, media processing, hosting/deployment and CRM/outcome adapters. Specify current supported actions, authentication scope, webhook verification, quota, read freshness, pagination/checkpoints, retry/idempotency and customer mapping before enablement. Read/recommend is separate from write support for every provider. Human-assisted completion must attach evidence when an API is unavailable; it may not masquerade as verified API execution.
