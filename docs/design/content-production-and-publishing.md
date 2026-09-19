# Content Production and Publishing

Status: user-requested capability expansion, 2026-09-19. Requirements R-020/R-021. Reference: [Adaptify content](https://adaptify.ai/features/content).

Add a production workflow for research, briefs, outlines, drafts, revision and editorial review. Apply customer brand voice, approved facts and linking preferences. Support uploaded/licensed/generated visuals with provenance and alt text, metadata and structured-data proposals. Own the single canonical Calendar Entry schedule for content production and publishing across CMS, social and email. Strategy and channel views project those entries rather than keeping independent schedules. Quality review covers factual support, readability, intent alignment, links and customer instructions; failed work returns for bounded revision or human review.

## MOMS publication contract

Content items attach to existing work items and goals. Preserve immutable revisions, sources, reviewer decisions and the exact version approved for publication. Brand instructions are versioned data and cannot override application controls. Do not invent author credentials or treat model quality scores as factual validation.

CMS adapters must declare supported draft/create/update/schedule/media/readback operations. Candidate targets are WordPress, Webflow, Shopify, Duda, Squarespace and HubSpot, subject to capability testing. Export is an explicit fallback where direct publishing is unsupported. A branded WordPress connector is a future packaging option, not a prerequisite for M1.

Approval may require agency review, customer review or both according to configured policy; no default production role policy is inferred. Recheck permissions and approval immediately before execution. Record destination, payload revision, idempotency reference and verified result. On timeout reconcile remote state before retrying. Detect remote edits before replacing content; preserve the previous revision and require authorization for rollback. Publishing success, indexing and ranking are separate observations. Only use indexing mechanisms supported for the particular content type; no universal indexing guarantee.

## Acceptance

CP-01: An unsupported factual claim or failed required check blocks publication.

CP-02: Changing approved content invalidates that approval; revoked authority blocks queued publication.

CP-03: A timed-out submission cannot create a duplicate page on retry; remote edits raise a conflict.

CP-04: Report publication only after readback; record unsupported operations as unavailable.

See [controls](autonomy-approvals-and-spend-controls.md) and D-015 in [decisions](design-notes.md).

## Service delivery and media extensions

The [web/commerce/creative backend](web-commerce-and-creative-backend.md) adds specialist production, store/listing artifacts and controlled website releases. Reuse Content/Revision and approval history for media/channel variants. Source rights and rejected-review state propagate to downstream publication targets.

## Shared planning and asset views

Extend planning with channel previews, labels, reviewer assignments and scoped external feedback. The creative backend owns source/derived assets and rights; this workflow references approved revisions as its shared asset library. A provider-specific publication record is an execution projection, not another calendar authority. Email recipient dispatch and provider scheduling remain transport details linked to the canonical entry.

Optional tracked/vanity links and link-in-bio pages are website/content artifacts with authorized domains and destination revisions. They use the existing deployment, attribution and approval controls. Mobile access is a responsive view of the same permissions; native mobile applications remain an implementation decision. Suggested publish times are hypotheses with evidence, not permission to reschedule approved work.
