# Social, Email and Community Backend

Status: user-requested capability expansion; R-028/R-029. References: [Search Berg social services](https://www.searchberg.com/social-media-management/) and [email services](https://www.searchberg.com/email-marketing/). MOMS adds execution infrastructure for social content, customer engagement and email campaigns; architecture below is original MOMS design.

## Social and community

Reuse Content Item/Revision and Calendar Entry. A SocialPublication records target account, platform-specific payload, scheduled timezone/time, approval digest and external post ID. Platform constraints are validated before dispatch. A common post may have several channel variants, each with its own execution and verification; partial success is visible.

The [Engagement Inbox and Cases](engagement-inbox-and-cases.md) document now exclusively owns inbound conversation routing, reply workflows, team ownership and customer-care cases. This backend owns platform transport, supported message/moderation operations, provider event ingestion and send/readback results. It submits observations to the shared evidence store and routes authorized interactions into the canonical inbox; it does not create a separate community inbox.

[Creator Relationship Management](creator-relationship-management.md) owns discovery, roster and InfluencerEngagement lifecycle. Channel posting and boosting consume its approved content/rights references and existing campaign controls.

## Email campaigns

Use a contact identity reference with customer-scoped channel addresses, provenance, purpose-specific consent/preference events and suppression state. CRM contact presence alone is not sending permission. Versioned segments produce auditable recipient snapshots; re-evaluate suppression immediately before each dispatch. Keep promotional campaigns separate from operational report delivery.

An EmailCampaign links approved template/content revision, segment, sender identity, schedule, measurement plan and provider connection. Sends have idempotency keys per campaign revision/recipient. Authenticated callbacks record delivery, bounce, complaint and unsubscribe events with deduplication and out-of-order handling. Unsubscribe processing suppresses pending sends. Provider-accepted mail is not confirmed inbox delivery; opens are an imperfect signal and must not stand in for revenue.

## Acceptance

SE-01: Replaying a schedule or callback does not duplicate a post, reply or email.

SE-02: Unsubscribing after scheduling but before dispatch blocks the promotional send.

SE-03: One failed social destination does not cause successful destinations to republish on retry.

SE-04: A user cannot reply, moderate, boost or pay a creator using unrelated drafting authority.

See [content](content-production-and-publishing.md), [outreach](authority-and-outreach.md), [controls](autonomy-approvals-and-spend-controls.md) and D-021.
