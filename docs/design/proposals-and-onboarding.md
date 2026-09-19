# Proposals and Onboarding

Status: user-requested capability expansion, 2026-09-19. Requirement R-025. Reference: [Adaptify proposals](https://adaptify.ai/features/proposals).

Create branded proposals from an existing prospect assessment, selected recommended work and optional authorized sales-call notes/transcripts. Include business goals, research, proposed content and authority activity, scope, sample deliverables, approved pricing and assumptions. Support editable versions, approved case-study/testimonial assets, prospect engagement events, signature/payment integrations and conversion into onboarding. Later proposal analytics can inform reviewed template improvements.

## MOMS commercial boundary

Prospect is a lifecycle state of the customer context, not a separate duplicated customer database. Proposal lines reference work items and immutable quote versions. Samples remain labelled examples. Prices come from configured approved commercial rules, never AI invention. Do not reuse another customer's private results, transcript or testimonial without permission.

Acceptance binds to exact scope, terms and price revision. Keep signature, payment status, entitlement activation and action authorization separate. A paid proposal does not authorize ad spending, CMS publishing or outreach. Verify signed webhook events and process them idempotently. Record failed, refunded and disputed states without silently starting work. Provider, contract terms, refund/activation rules and analytics consent remain D-018.

## Acceptance

PO-01: Proposal numbers and evidence reconcile to the source assessment and configured quote version.

PO-02: Acceptance creates one onboarding engagement even when callbacks repeat; existing customer/property records are reused.

PO-03: Payment alone cannot trigger external marketing actions or confer customer access.

See [subscription model](subscription-model.md), [controls](autonomy-approvals-and-spend-controls.md) and [domain model](domain-model.md).
