# Google Ads Management

Status: source-backed phased capability. Sources: H2, H3, H4, H5. Provider-specific API behavior is intentionally not asserted here; engineering must verify current official documentation when selecting the integration.

## Phase A: Read and recommend

Connect only to an explicitly authorized customer account. Read campaigns, ad groups, keywords, available search terms, ads, spend, budgets, CPC, clicks, impressions, configured conversions and conversion cost, geographic targeting, negative keywords, landing pages, and performance history.

Generate keyword candidates/groupings, negative-keyword recommendations, budget and campaign recommendations, CPC observations/estimates, landing-page work, waste/anomaly findings, pacing, and proposed changes. Distinguish reported historical CPC, provider forecasts, and calculated planning scenarios. Preserve geography, date range, currency, and estimate assumptions.

Conversion data depends on configured tracking. Missing conversion tracking must not be shown as zero leads or a definitive return-on-spend judgment. Recommendations remain useful but must explain that limitation.

## Phase B: Controlled execution

Recommendation → customer/internal approval according to an approved role policy → authorized change → verification → measurement.

Require explicit account write authorization and enforce customer total budget, account policy, campaign limits, allowed actions, and approval thresholds through deterministic application logic. Log proposed payload, before/after state, approver or standing authorization, execution result, and verification. Revocation must prevent subsequent writes. Role assignments and numeric thresholds remain open decisions.

## Spend boundary

A MOMS permission limit and a provider's actual billing behavior are different things. Do not promise that setting a campaign budget produces an exact billing cap. Before live write enablement, engineering must establish provider budget semantics, reporting lag, concurrent and external edits, enforcement latency, pacing, and responses to policy breaches. Model output cannot change these rules. If the required hard ceiling cannot be guaranteed through the chosen integration and operating model, escalate D-010 and keep writes disabled.

## Estimates

A planning scenario may show `estimated clicks = proposed budget / estimated CPC` when CPC is positive and both values have compatible currency/time assumptions. Label it illustrative, not a guarantee of impressions, clicks, leads, or revenue. Lead estimates require an explicitly supported conversion-rate assumption and a range.

Ads integration and writes are outside EWP-001. See [controls](autonomy-approvals-and-spend-controls.md), [benefit model](benefit-and-time-model.md), and [open decisions](design-notes.md).
