# Assessment pilot feedback for runtime implementation

Status: implementation guidance derived from the user-authorized public assessment pilot, 2026-10-23. No deployment, provider or numeric operating policy selected. Customer-specific evidence belongs in private assessment records.

Applies to [EWP-001](EWP-001-public-domain-assessment.md); no expansion into writes or recurring jobs.

## Required behavior and verification cases
- AC-02/AC-08: discover navigation, sitemap and search-only pages; preserve discovery method and coverage. Fixture: a legacy page outside the current menu is found and checked.
- AC-02/AC-11: retain per-source retrieval method, observation time, source crawl time when available, URL, status and supporting content. Do not represent search snippets as current live state.
- AC-04/AC-09: compare identity/contact facts across pages and external references; flag conflicts for confirmation, never infer ownership or merge identities automatically.
- AC-08: represent each canonical audit category/check as assessed or incomplete; unknown is not pass or absence.
- AC-04/AC-08: HTML tracking detection, rendered tracking detection and authorized account verification are separate checks. No HTML identifier alone cannot prove analytics absent.
- AC-04: identify unverified offerings, prices, testimonials and time-sensitive availability; recommend owner confirmation rather than inventing corrections.
- AC-07: preserve original baseline, source evidence and report revisions; subsequent observations create comparisons rather than replacing history.
- AC-04/AC-10: use existing Marketing Work Items and separate preparation/recommendation from authorized execution. No form submission, external message or change during read-only assessment.
- AC-09/AC-11: isolate customer records and keep private pilot evidence out of the public design repo.

## Delivery status
A manual public assessment produced these requirements. The independently running runtime is not implemented or deployed by this document. Future engineering must provide executable acceptance evidence for each case. Existing provider, hosting and production gates remain applicable.
