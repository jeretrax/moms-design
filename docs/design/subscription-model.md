# Subscription Model

Status: subscription service and deterministic entitlements are source-backed; commercial terms remain unresolved. Sources: H2, H3, H4.

MOMS is a subscription marketing service. Customers buy marketing outcomes and managed work, not agent instances or model versions. Subscription entitlements must be enforced in application logic.

The handoffs do not establish tier names, prices, free trials, quotas, billing provider, checkout behavior, overages, cancellation rules, or included human labor. No pricing from a different site or prior experiment is imported into this design.

## Commercial decisions to resolve

- What assessment, reporting, analysis, drafting, and managed execution each plan includes.
- Number of businesses/domains/accounts and cadence or usage allowances.
- Human review and implementation services included versus separately quoted.
- Fees for the service versus customer ad media spend and optional third-party charges.
- Trial/free offering, overage consent, cancellation, retention, and paused-service behavior.

An entitlement answers whether a capability is included. It does not authorize spending or publishing. Customer consent and integration/action permission still apply.

Billing/checkout implementation is outside EWP-001. See D-004 in [design notes](design-notes.md) and [controls](autonomy-approvals-and-spend-controls.md).

## Expansion entitlement dimensions

Future commercial configuration may meter managed properties, strategy jobs, visibility samples, content production, CMS targets, outreach work and reporting deliveries. Record usage and costs against the applicable entitlement; limits and overage prices remain D-004. [Proposal acceptance](proposals-and-onboarding.md) can activate configured service entitlements only under approved commercial rules. Billing integration is now a later capability, still outside EWP-001.
