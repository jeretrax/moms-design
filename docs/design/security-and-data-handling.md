# Security and Data Handling

Status: isolation, permissions, audit and deterministic control obligations are source-backed; detailed safeguards are derived engineering constraints. Sources: H4, H5.

## Boundaries

Enforce customer isolation on records, jobs, reports, evidence, integrations, caches and storage references. Never rely on a model to select or validate a customer's authority. Production membership, operator access and customer authentication require D-001.

Keep API/OAuth secrets outside source control, report output and prompts. Bind connections to authorized customer accounts. Use minimum required provider permissions; M1 has no need for Ads write credentials.

Public domain intake must not become access to private infrastructure. Validate URL schemes and resolved destinations, block private/local/metadata routes, recheck redirects, and apply bounded crawl/network behavior. Treat pages and third-party text as untrusted data rather than operational instructions.

## Accountability and storage

Audit consequential recommendations and actions with evidence, rationale, approval identity, before/after where applicable, outcome and costs. Do not log secrets. Preserve report/baseline lineage needed to compare forecasts with later results.

Retention, deletion, evidence capture limits, personal-data handling, residency, export, encryption/key-management design, backup policy and audit retention need explicit decisions before production. Public availability alone does not define an unlimited right to retain or republish source content.

Numeric rate/cost limits and crawl collection rules remain configurable decisions, not invented defaults. See [controls](autonomy-approvals-and-spend-controls.md), [assessment](seo-site-assessment.md), and D-003/D-005 in [design notes](design-notes.md).

## Expansion data boundaries

Apply isolation and retention to transcripts, expert profiles, unpublished content, media, prompts, quotes and proposal engagement data. Verify custom-domain/customer bindings and sharing scope server-side. Authenticate external callbacks and prevent replay. Branded presentation does not replace identity verification or justify hiding material limitations. See [portal](agency-portal-and-reporting.md), [proposals](proposals-and-onboarding.md) and D-014 through D-018.

## Service operations security

[Backend contracts](service-delivery-backend.md) extend isolation to events, cycle jobs, staff/vendor assignment, artifacts, costs and reporting projections. Restrict sensitive review cases, audience identifiers, messages, audio feedback and conversion data. Use credential references, authenticated callbacks, purpose-specific access and retention rules. Worker uploads/media processing require scanning and isolation. Backup/restore, recovery targets and deployment topology remain D-024; the design does not select a production platform.

## Intelligence source and identity controls

Shared observation storage preserves source/customer/purpose access and licensing restrictions in every index, model retrieval, export and cache. Separate private message access from public listening views. Derived sentiment/cohorts cannot automatically infer sensitive traits or resolve cross-network identities. Retention/deletion applies to imported first-party datasets and restricted creator contracts as well as raw evidence. D-026/D-029 define production policy; [ownership](capability-ownership-and-reconciliation.md) never overrides those boundaries.
