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
