# Local Presence and Reputation Backend

Status: user-requested capability expansion; R-030. References: [Search Berg local SEO](https://www.searchberg.com/local-seo-services/) and [reputation services](https://www.searchberg.com/reputation-management-services/). Local listing/citation work and reputation service delivery extend the existing presence capability.

## Local identity and evidence

BusinessLocation belongs to the customer and records approved business name, address/service area, contact details, hours and location-specific offerings with revision history. ListingBinding joins a location to a provider account/profile and stores ownership/verification evidence. A citation observation records source URL, capture time, observed values and mismatch findings. Do not overwrite canonical customer facts with a scraped directory value.

Profile changes create work items, field-level proposed diffs and scoped authorization. Execute through declared provider capabilities; verify resulting values and retain rejected/pending states. Duplicates and profile suspension/reinstatement become operator-owned cases with evidence and dependencies. Never invent locations or claim provider reinstatement success before confirmation. Regional and language scope belongs to strategy/observations, not a duplicate business identity.

## Reputation operations

ReviewObservation records provider, location or verified subject, source ID/URL, rating/text where permitted and capture time. Separate machine-interpreted sentiment from source facts. Response drafts attach to exact reviews and use customer authorization before publishing. Requests for reviews require a valid audience/sender policy and must not fabricate reviews or selectively solicit only positive feedback. Removal disputes are evidence-backed human/provider workflows; MOMS cannot promise to delete third-party criticism.

Business and personal reputation subjects require explicit scope and access policy; sensitive case details are restricted. Changes in observed review availability are new observations, not erasure of prior work. Collection rights, retention, request practices and response escalation remain D-022.

## Acceptance

LR-01: Updating one location cannot alter another customer's or location's listings.

LR-02: Observed mismatches propose reviewable changes without replacing approved business facts.

LR-03: Unverified removals, reinstatements and listing updates remain pending/unknown rather than completed.

See [domain model](domain-model.md), [authority work](authority-and-outreach.md) and [service backend](service-delivery-backend.md).
