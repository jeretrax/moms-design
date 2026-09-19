# Repository work instructions

Read REPO_START_HERE.md, docs/design/design-to-implementation-governance.md, and docs/design/design-notes.md before changes.

This is a design repository. Do not turn a document-maintenance task into application implementation. Canonical owner documents define concepts; other documents link to them. Preserve supplied handoffs unchanged as provenance.

Maintain the master index and requirements traceability for material changes. Do not mark a proposed design decision approved without user authorization. Do not select pricing, providers, production tenancy, role policies, or numeric operating limits by assumption.

The first engineering package excludes Google Ads writes, website publication, and billing implementation. Spend, isolation, authentication, approvals, API permissions, entitlements, rate limits, and publication permissions must be deterministic controls.

Validate relative Markdown links and acceptance-criterion references before committing. Report what changed, unresolved decisions, verification performed, and publication status. Never claim a local commit was pushed without checking the remote.
