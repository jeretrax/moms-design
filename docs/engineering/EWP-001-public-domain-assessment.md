# EWP-001: Public Domain to Marketing Work List and Report

Status: source-backed implementation scope prepared; unresolved live/production gates are listed below. No application implementation is included in this repository bootstrap.

## Objective and authority

Give MOMS a business, domain, geography and desired customers. Return a defensible prioritized marketing plan describing what to do, why, possible cost, expected benefit, and when to measure it; save the assessment and baseline.

Authority: [MVP scope](../design/mvp-scope.md), [assessment](../design/seo-site-assessment.md), [work item](../design/marketing-work-item.md), [report](../design/report-contract.md), [controls](../design/autonomy-approvals-and-spend-controls.md). Traceability: R-001 through R-007, R-011, R-012, R-014, R-015 and R-017. At kickoff record the actual baseline commit in the implementation work record, not a guessed or self-referential hash.

## Included

Customer/domain intake; ordinary-language goals and priority offerings; target geography; bounded public crawl; search intent/topic candidates; current relevant search and competitor observations; evidence-linked findings; prioritized Marketing Work Items; benefit/effort/cost estimates where supportable; readable customer report; persisted assessment, work list and baseline.

## Excluded

Google Ads account integration and all Ads writes; campaign activation; website/content publication; third-party posting/outreach; recurring optimization jobs; billing/checkout; full operational approval workflow; complete marketing platform. Public paid-search opportunity recommendations are allowed without a connected Ads account if properly evidenced and labelled.

## Proposed implementation sequence

1. Resolve the relevant runtime/provider/access decisions and record the baseline.
2. Implement intake and canonical persistence contracts.
3. Build bounded provider adapters with fixture coverage and live-source evidence.
4. Generate structured findings and work items; validate evidence and unknowns.
5. Render a readable report from persisted records and preserve the baseline.
6. Demonstrate the complete journey, partial failures and isolation boundaries.

This sequence is not permission to resolve material product questions without the owner.

## Gates

D-002/D-003: before live research. D-006/D-008: before final ranking/report acceptance. D-011: before deployable implementation. D-001/D-005/D-012: before production/self-service customer use. Other decisions may remain deferred where this package does not use them. Unresolved gates do not block isolated, clearly labelled fixture-based engineering, but fixtures do not satisfy live-research acceptance.

## Acceptance criteria

| ID | Observable outcome |
| --- | --- |
| AC-01 | Create customer/context and persist domain, description, ordinary-language objective, desired customers, priority offerings and geography without requiring a keyword list or Google account |
| AC-02 | Public crawl records dated page evidence and coverage; rejects non-public destinations and unsafe redirects; bounded failures are visible |
| AC-03 | Generate goal/geography-related intent and keyword candidates; record actual current search queries, sources, timestamps and visible competitor pages; distinguish candidates from measured volumes |
| AC-04 | Produce a prioritized work list with all source-required fields, concrete actions, evidence or explicit hypothesis labels, dependencies, rationale and capability/approval distinctions |
| AC-05 | Each major recommendation states proposed benefit, useful measurement window/class, confidence, method and cost/effort with basis or explicit unknown reason; no ranking or date guarantees |
| AC-06 | Readable report covers every required report section and lets a non-marketing reviewer identify next actions, rationale, costs/unknowns and measurement expectations |
| AC-07 | Reopening the saved assessment returns the same report/work-item revisions and baseline; later observations do not overwrite that original snapshot |
| AC-08 | Missing/rate-limited sources produce explicit incomplete coverage and unknown values; no invented competitors, rankings, CPC or conversion data fills gaps; retry does not duplicate completed output |
| AC-09 | Customer context is enforced across reads, writes, jobs, evidence and reports; cross-customer references/access fail; untrusted website text cannot grant capabilities |
| AC-10 | M1 cannot call Ads mutations, publish content or perform external account changes; secrets do not appear in reports or stored prompts intended for inspection |
| AC-11 | Assessment provenance and audit context explain evidence, generated recommendations, priority rationale, dates, source availability and known processing costs |

## Verification evidence required

Demonstrate one consented public domain through live intake/research/report/persistence; retain source timestamps and report coverage. Use fixtures for controlled source failures, unsafe URLs/redirects, instruction-bearing page text, and cross-customer access. Verify persistence by reopening a completed assessment. Inspect the generated report with a non-marketing reviewer against AC-06. Verify absent mutation capability directly at the application boundary. Do not run spend-bearing advertising or publication as a test of this package.

## Escalation and handback

Escalate unavailable lawful search access, incomplete evidence presented as complete, unsupported estimate promises, production access/retention gaps, or any proposed scope expansion. Return implementation commits, AC-by-AC evidence, unresolved failures, provider/operating choices, and design-change proposals. Completion requires acceptance evidence, not just code existence.
