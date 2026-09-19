# Keyword and Topic Strategy

Status: user-requested capability expansion, 2026-09-19; scoring formula remains D-006. Requirement R-018. Reference: [Adaptify keyword strategy](https://adaptify.ai/features/keyword-strategy).

Extend one-time keyword discovery into a maintained strategy joining keyword candidates, AI questions, business goals, topic clusters and target pages. Support manual additions and CSV import, local intent, pillar-page assignment, cluster editing, ordering, and a content calendar. Prioritize opportunities with explained evidence for business relevance, attainable demand, difficulty and coverage gaps. Natural-language edits produce reviewable changes with an audit trail and a recoverable prior strategy revision.

## MOMS integration and controls

Use existing Search Intent/Keyword Candidate records. A cluster groups references; it does not create duplicate keyword facts. Link recommended changes to Marketing Work Items. Strategy displays a projection of the Calendar Entries owned by [content production](content-production-and-publishing.md), referencing planned content and approved capacity. It does not own a second scheduling store; ordering does not itself approve publication. Preserve provenance and unknown values when providers lack volume or difficulty data.

Strategy revision, not silent replacement, preserves historical reports and forecasts. Detect competing target pages and duplicate work before creating additional content. Undo restores internal planning state only; any external reversal needs a separately authorized action. Formula weights and numerical confidence scales remain unresolved.

## Demand research integration

[Consumer intelligence](consumer-and-market-intelligence.md) owns licensed search-demand series and cross-source research. Strategy consumes those observations to prioritize work; [AI visibility](ai-search-visibility.md) continues to own prompt sampling. Candidate terms, estimated demand and observed queries remain distinguishable.

## Acceptance

KS-01: Import the same candidates twice without creating duplicate targets within the same customer/geography context.

KS-02: A cluster can reference a pillar page and multiple work items while the source evidence remains traceable.

KS-03: A natural-language strategy revision shows affected records, preserves its predecessor and cannot trigger publication.

See [work items](marketing-work-item.md), [expansion roadmap](agency-growth-expansion.md) and [decisions](design-notes.md).
