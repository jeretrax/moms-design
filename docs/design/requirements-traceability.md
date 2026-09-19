# Requirements Traceability

Status: source-reconciled baseline. [Source register](../reference/handoffs/README.md). AC references identify criteria in [EWP-001](../engineering/EWP-001-public-domain-assessment.md). Deferred requirements need later work packages; they are not claimed implemented.

| ID | Source section | Requirement | Canonical owner | Verification / allocation |
| --- | --- | --- | --- | --- |
| R-001 | H1; H5: governance | Canonical design authority and bounded engineering | [design-to-implementation-governance](design-to-implementation-governance.md) | Repository / EWP authority |
| R-002 | H2: intake; H3: inputs | Domain, business intent, offerings, desired customers and geography | [customer-experience](customer-experience.md) | AC-01 |
| R-003 | H3: Function 1 processing | Public site assessment with technical/content/local coverage | [seo-site-assessment](seo-site-assessment.md) | AC-02, AC-08 |
| R-004 | H2: core loop; H3: processing | Search intent, keyword candidates and current competitor research | [seo-site-assessment](seo-site-assessment.md) | AC-03, AC-08 |
| R-005 | H3: Marketing Work Item | Required work-item fields and execution capability classes | [marketing-work-item](marketing-work-item.md) | AC-04 |
| R-006 | H3: Function 1 output | Readable report and next decisions | [report-contract](report-contract.md) | AC-06 |
| R-007 | H3: Function 3; first slice | Benefit hypothesis, measurement window and saved baseline | [benefit-and-time-model](benefit-and-time-model.md) | AC-05, AC-07 |
| R-008 | H2: paid search; H3: Phase A | Authorized Google Ads read and recommend | [google-ads-management](google-ads-management.md) | Deferred: M2; no EWP-001 integration |
| R-009 | H3: Phase B; H4: Ads safety | Controlled Ads writes, before/after and verification | [google-ads-management](google-ads-management.md) | Deferred: later gated EWP |
| R-010 | H3: Function 3 | Ongoing expected-versus-actual comparison | [benefit-and-time-model](benefit-and-time-model.md) | Deferred: M3; forecast portion AC-05 |
| R-011 | H4: deterministic controls | Deterministic isolation, permissions, entitlements and resource controls | [autonomy-approvals-and-spend-controls](autonomy-approvals-and-spend-controls.md) | AC-09, AC-10; later spend gates |
| R-012 | H4: operating pattern and roles | Bounded jobs with internal logical responsibilities | [agent-operating-model](agent-operating-model.md) | AC-08, AC-11; later triggers deferred |
| R-013 | H2: presence/content | Legitimate presence opportunities, eventual drafts, separate publication authority | [product-definition](product-definition.md) | M1 report coverage AC-06; content execution deferred |
| R-014 | H4: data sources and AI provider | Replaceable data/model providers | [integrations-and-provider-interfaces](integrations-and-provider-interfaces.md) | Adapter review; AC-03, AC-08 |
| R-015 | H4: auditability | Evidence, recommendation rationale and action accountability | [autonomy-approvals-and-spend-controls](autonomy-approvals-and-spend-controls.md) | AC-11; execution audit deferred |
| R-016 | H2/H3: subscription; H4: entitlements | Subscription service with deterministic entitlements | [subscription-model](subscription-model.md) | Commercial rules unresolved D-004; production gate |
| R-017 | H1/H3/H5: first milestone | Assessment-only first EWP; no Ads writes | [mvp-scope](mvp-scope.md) | AC-01 through AC-11; AC-10 boundary |

Implementation handback must record EWP, baseline design commit, implementation commit, acceptance evidence and outstanding issues. Proposed schemas and architecture are explicitly marked in their owner documents; the five source handoffs do not select a technology stack.

## User-requested expansion (2026-09-19)

Source: explicit user request and [reference review](../reference/adaptify-capability-review.md). These requirements are design additions; they are not implemented or part of EWP-001.

| ID | Requirement | Canonical owner | Future verification |
| --- | --- | --- | --- |
| R-018 | Maintained topic/keyword strategy | [Strategy](keyword-and-topic-strategy.md) | KS-01 through KS-03 |
| R-019 | Sampled AI-search visibility and gap work | [Visibility](ai-search-visibility.md) | AI-01 through AI-03 |
| R-020 | Versioned content production and quality review | [Content](content-production-and-publishing.md) | CP-01, CP-02 |
| R-021 | Authorized CMS publication and verification | [Publishing](content-production-and-publishing.md) | CP-02 through CP-04 |
| R-022 | Legitimate outreach and placement monitoring | [Authority](authority-and-outreach.md) | AO-01 through AO-03 |
| R-023 | Scoped agency portfolio and customer access | [Portal](agency-portal-and-reporting.md) | AR-01, AR-03 |
| R-024 | Branded reports and scheduled deliveries | [Reporting](agency-portal-and-reporting.md) | AR-02, AR-03 |
| R-025 | Proposals, acceptance and onboarding | [Proposals](proposals-and-onboarding.md) | PO-01 through PO-03 |

Cross-capability acceptance: EX-01 through EX-03 in [expansion roadmap](agency-growth-expansion.md). Future EWPs must map these IDs to executable verification before release.

## Managed-service backend request (2026-09-19)

Source: explicit user request and [Search Berg review](../reference/searchberg-capability-review.md). Architecture is original MOMS design. Requirements are future capabilities, not implemented features or additions to EWP-001.

| ID | Requirement | Canonical owner | Future verification |
| --- | --- | --- | --- |
| R-026 | Engagement/cycle execution and durable backend | [Delivery](service-delivery-backend.md) | SD-01 through SD-05 |
| R-027 | Multichannel paid campaign operations | [Campaigns](multichannel-campaign-backend.md) | MC-01 through MC-04 |
| R-028 | Social, community and influencer operations | [Social/email](social-email-and-community-backend.md) | SE-01, SE-03, SE-04 |
| R-029 | Audience, consent and email campaign execution | [Social/email](social-email-and-community-backend.md) | SE-01, SE-02 |
| R-030 | Local listings and reputation operations | [Local/reputation](local-presence-and-reputation-backend.md) | LR-01 through LR-03 |
| R-031 | Web/deployment/maintenance engagements | [Web/commerce/creative](web-commerce-and-creative-backend.md) | WC-01 |
| R-032 | Marketplace/catalog operation boundaries | [Web/commerce/creative](web-commerce-and-creative-backend.md) | WC-02 |
| R-033 | Versioned creative assets and rights | [Web/commerce/creative](web-commerce-and-creative-backend.md) | WC-03 |
| R-034 | Conversion definitions, CRM outcomes and attribution | [Measurement](measurement-and-crm-backend.md) | ME-01 through ME-03 |

Cross-capability acceptance MB-01 through MB-03 is in the [backend expansion](managed-marketing-backend-expansion.md). A future implementation handback must map these criteria to evidence and resolved release gates.
