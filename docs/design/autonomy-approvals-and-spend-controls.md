# Autonomy, Approvals, and Spend Controls

Status: source-backed control requirements with derived enforcement sequence. Sources: H3, H4, H5.

| Level | Authority |
| --- | --- |
| 0: Observe | Read and analyze |
| 1: Recommend | Create recommendations and work items |
| 2: Draft | Prepare content/configuration for approval |
| 3: Execute With Approval | Execute one specific approved action |
| 4: Standing Authorization | Execute authorized action classes within deterministic limits |

Grant authority per customer, integration, capability, and action type. A level is not a global permission switch. Drafting never implies publication authority. M1 supports observation/recommendation, with no external mutation pathway.

## Deterministic enforcement

Application logic, not AI judgment alone, enforces authentication, authorization, customer isolation, API permissions, allowed actions, approvals, ad-spending ceilings, subscription entitlements, rate limits, publication permissions, and audit logging.

Before consequential execution, a derived control sequence is: authenticate actor/job; validate customer/account binding; check current entitlements and integration permissions; validate allowed action and publication rules; match the exact proposal to current approval or standing authorization; evaluate current budget policy and concurrent work; record intended execution; perform the bounded action; verify external state; record outcome and measurement linkage.

Approvals must bind to the proposed scope and version. Changed cost, target account, payload, or material preconditions require re-evaluation. Approval expiry rules, role authority, and thresholds are unresolved, not assumed.

## Required audit questions

What was observed? Which evidence was used? What was recommended and why prioritized? Who approved it? What action occurred? What did it cost? What changed afterward?

Record before/after state for Ads writes, approval identity, timestamps, target, outcome, and verification. A timeout after submission is an unknown outcome until reconciled; do not blindly retry a mutation. Never mark an action completed solely because a request was submitted. Revocation blocks new writes and queued jobs must recheck current authority.

## Spend controls

Evaluate customer total ad budget, account policy, campaign limits, action types, and approval thresholds together. MOMS service fees, ad media spend, and internal API/model costs are separate amounts. Deny writes when the required budget/authority data is missing or stale under the selected policy. Provider enforcement semantics, budget periods, currencies, concurrency, external edits, and emergency pause behavior require D-010 before writes are enabled.

No agent may redefine policy or grant itself permission. See [Ads](google-ads-management.md), [security](security-and-data-handling.md), and [design notes](design-notes.md).

## Expanded action classes

Scope grants separately for content drafting, CMS create/update/publish, outreach send, report delivery, proposal issuance and commercial activation. Apply customer/account/version-bound approvals and recheck before queued execution. Third-party content/placement purchases have separate spending policy from Google Ads budgets. Buying a subscription or accepting a proposal does not grant external write authority. See [expansion owners](agency-growth-expansion.md) for failure and verification requirements.

## Managed-service action boundaries

Paid-channel allocation, social posting/replies/moderation/boosting, promotional email, review requests/responses, listing updates, marketplace promotions, deployment/DNS changes and vendor compensation are separate action types. [Backend owners](managed-marketing-backend-expansion.md) specify required scope and evidence. Validate consent/suppression, current account permissions, artifact revision and available funding at execution, not only scheduling. Budget reservation protects MOMS concurrency; provider billing limits still require D-010 resolution. Service purchase alone grants none of these actions.
