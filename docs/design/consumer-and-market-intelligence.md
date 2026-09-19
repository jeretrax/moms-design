# Consumer and Market Intelligence

Status: user-requested capability design, 2026-09-19; R-035/R-036/R-037. References: [consumer research](https://www.brandwatch.com/products/consumer-research/), [search intelligence](https://www.brandwatch.com/suite/search-intelligence/) and [analyst services](https://www.brandwatch.com/suite/insights/).

Add saved research queries across available public/licensed social, web, news and authorized first-party sources. Support keyword/Boolean filters where providers allow, topic and sentiment classification, text/image brand signals, cohort analysis, historical comparison and human-reviewed summaries. Demand research compares traditional, social and shopping search signals with existing sampled AI visibility. Analysts can investigate emerging issues, curate briefings and route opportunities into marketing work.

## MOMS evidence contract

ResearchQueryRevision records customer, question, terms/exclusions, brands/products, geography/language, sources, periods and collection budget. Natural-language query assistance produces a reviewable structured query. Query revisions never rewrite historical result sets. Observation identity uses provider/account/source-item scope; repeated results reference the same source item with capture/revision lineage. Syndicated/reposted items have relationship links, not an assumed identical audience.

SourceCapability records collection rights, export/redistribution restrictions, available history, freshness, coverage and authorized customer scope. Backfill occurs only within available licensed history and quota. No assumed archive size, global network coverage or real-time SLA is imported. A lack of accessible data is unknown, not silence in the market. Private conversations remain access-scoped; a unified store is not permission to expose them to general analysts.

ClassificationRevision references observation, taxonomy/model version, label, confidence and human correction. Sentiment and inferred topics are interpretations. Image-derived brand detections retain confidence and source evidence; they cannot identify a person by assumption. ResearchCohort is a scoped analytical filter, not a mailing list or inferred identity graph. Authorized first-party imports retain provenance, purpose and retention; no automatic marketing consent results.

## Demand and visibility boundary

SearchDemandSeries records provider methodology, term/topic, locale, unit, period and observed/estimated status. Strategy consumes the series; AI visibility owns prompt testing and citation measurement. Do not sum query volume, social mentions and AI samples into an unexplained visibility score. Correlation across these signals can suggest a work item; it does not prove causation or identify individual searchers.

## Findings, alerts and briefings

InsightFinding links evidence, question, method, uncertainty, analyst review and suggested next action. AlertRuleRevision defines a condition, comparable baseline/window, minimum coverage, severity and cooldown/deduplication policy. Evaluate on bounded jobs; persist AlertOccurrence, acknowledge state and evidence. Low coverage or ingestion outages produce data-quality issues rather than brand-crisis claims. Thresholds remain D-028.

Findings can link to existing Marketing Work Items and [EngagementCases](engagement-inbox-and-cases.md). Cases coordinate human assessment; no negative-sentiment label authorizes deletion, public response or campaign shutdown. Analyst Briefing is a report type with review status and citations, rendered/delivered by [agency reporting](agency-portal-and-reporting.md). Repeated alerts share a case according to configured deduplication; delivery retries use the existing notification ledger.

## Acceptance

CI-01: Query replay and cross-capability ingestion preserve source identity without double-counting identical provider items.

CI-02: Every chart/summary exposes query revision, source coverage, time window and observation/classification lineage.

CI-03: Correcting a classifier creates a new interpretation and retains prior report reproducibility within retention/access rights.

CI-04: Provider outages do not trigger a false decrease/increase in brand sentiment or demand.

CI-05: An issue alert creates or links bounded review work; it cannot send an external response or alter advertising without authority.

See [ownership](capability-ownership-and-reconciliation.md), [runtime](service-delivery-backend.md) and D-026/D-028 in [decisions](design-notes.md).
