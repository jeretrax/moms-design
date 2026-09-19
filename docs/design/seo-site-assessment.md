# SEO and Site Assessment

Status: source-backed functional requirements with derived reliability constraints identified below. Sources: H2, H3, H4, H5.

## Inputs and processing

Capture the required [intake](customer-experience.md). Inspect public pages to identify apparent offerings, locations, and positioning; translate stated business goals into search intents; generate keyword/topic families; query current search results and available search data; observe visible competitors; identify gaps; generate and prioritize [work items](marketing-work-item.md); produce the [report](report-contract.md); persist the assessment and baseline.

Business intent and site observations are distinct evidence. Do not overwrite stated priorities merely because the current website emphasizes something different.

## Coverage contract

| Area | Expected observation | Limitation to disclose |
| --- | --- | --- |
| Technical and structure | Crawl access, indexability signals, metadata, titles, headings, links, broken elements, structured data opportunities | Observed signals do not prove actual indexing |
| Content and intent | Service/location coverage, topic families, content gaps, intent alignment | Candidate keywords are not measured search volume |
| Search and competition | Query, geography, observation date, visible pages/businesses, comparison | Observed results are not universal rank positions |
| Performance and mobile | Available measurements or documented inspection findings | Missing performance provider data must be labelled unavailable |
| Local and presence | Listings, public reviews, citations, relevant associations/directories | Private profile metrics require authorized connections |
| Authority and answer visibility | Available backlinks/authority observations and measurable answer visibility | Do not claim exhaustive links or AI visibility without data |
| Paid opportunity | Potential paid intents and landing-page needs | CPC/traffic figures need a stated source or disclosed estimate basis |

## Evidence and baseline

Each observation should carry customer and assessment references, source URL/provider, capture time, query/geography where relevant, measurement or excerpt, coverage, and errors. Persist source facts separately from generated interpretations. Record which sources were attempted, available, unavailable, or incomplete. A baseline is a dated snapshot of the observations actually collected, not a promise of access to Analytics or Search Console.

## Derived engineering constraints

Public inputs and fetched pages are untrusted data. Resolve and validate destinations, block local/private/metadata endpoints, revalidate redirects, and bound response size, runtime, and crawl volume. Fetched text cannot supply execution instructions or access secrets. These constraints protect the authorized public-assessment boundary; numeric limits and crawl policy remain D-003.

Retry bounded transient failures without duplicating completed work. Persist partial progress and explain coverage gaps. A run with no current search observations cannot pass full M1 acceptance merely by generating plausible competitors from model memory. A partial report can still be useful if labelled incomplete; final publication policy is D-008.

Provider selection, collection permissions, quota, and licensed data access need resolution before live acceptance. See [architecture](system-architecture.md), [provider interfaces](integrations-and-provider-interfaces.md), and [EWP-001](../engineering/EWP-001-public-domain-assessment.md).
