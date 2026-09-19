# Engagement Inbox and Cases

Status: canonical owner for inbound engagement, replacing the inline inbox description in the social/email backend; extends R-028/R-030 with R-038. Reference: [Brandwatch Engage](https://www.brandwatch.com/products/engage/).

Provide one permission-filtered operational inbox for authorized comments, direct messages and review-response work. Include saved feeds, labels, ownership, internal notes, response templates, reply suggestions, escalation and response-time reporting. Group related interactions into cases and support explicit external CRM/service handoff.

## Canonical model and workflow

InboundConversation remains the canonical provider thread reference, with provider-account identity, participants as verified external references, message/review observation links and source capabilities. An EngagementCase groups one or more conversations/findings around an issue, with customer, assigned owner/team, priority, status and linked Marketing Work Items. Cases group context; WorkAssignment owns execution responsibility, and Execution owns sends. Customer-care and reputation are case types/views, not separate ticket databases.

Claim and transfer operations require expected revision/concurrency checks. A reply draft binds to target account/thread, content revision and observed conversation version. If another agent replies or materially new content arrives, re-evaluate before sending. Record sent/failed/unknown separately and reconcile unknown outcomes before retry. Private replies, public replies, moderation and paid boosting have different grants. Saved replies and AI suggestions cannot bypass them.

Review responses retain ReviewObservation identity and reputation-specific rules. Where APIs do not support review replies, create human work with evidence requirements; do not pretend a draft was sent. External CRM handoff stores stable external case reference, owner-of-record and sync direction; prevent bidirectional event loops and do not silently duplicate case ownership.

## Access and timing

Internal notes, private messages and customer-visible replies are separate access projections. A public-source finding grants no private contact rights. Response target clocks record timezone, business-hours policy, wait/paused conditions and first/subsequent response definitions. Numeric targets and role matrix remain D-027. Proposed resolution requires evidence or a documented reason; reopening preserves history.

## Acceptance

EN-01: Two concurrent claim/send attempts cannot silently create duplicate ownership or replies.

EN-02: A private note or message cannot appear in a public reply/export through an authorized public-view query.

EN-03: A shared review/social case reuses source records and existing work/approval state.

EN-04: Handoff callbacks cannot loop into duplicate cases; response metrics use the configured clock definition.

See [channel transport](social-email-and-community-backend.md), [reputation policy](local-presence-and-reputation-backend.md) and [controls](autonomy-approvals-and-spend-controls.md).
