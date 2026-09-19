# Measurement, Conversion and CRM Backend

Status: MOMS backend design inferred to support the requested managed services; R-034. This is a proposed implementation contract extending [benefit measurement](benefit-and-time-model.md), not a claim about a competitor's internal attribution technology.

## Collection contract

ConversionDefinition versions what qualifies as an event, lead, qualified lead or sale. TrackingPlan links goals, page/app/account targets, consent requirements, tag changes and test evidence. Installing tags or altering conversion configuration requires website/account change authority. Validate configured collection before describing conversion results as available.

MeasurementEvent records customer, event ID, external source/account, observed/received time, event type, campaign/UTM/click references where available, consent context, value/currency if relevant and quality flags. Deduplicate by stable provider/account/event identity. Keep raw source evidence access controlled; normalized measures must preserve original units and event windows. Late or corrected events produce revised reporting snapshots.

## CRM boundary

CRMConnection maps authorized external contact/lead/opportunity IDs to minimal internal references. Import outcome changes through an authenticated adapter or reviewed file; define source ownership and conflict behavior before enabling two-way sync. Keep person identity separate from campaign membership and sending permissions. Form submissions and permitted call events may create lead references; recordings/transcripts have separate permission and retention rules.

AttributionSnapshot records rule/model version, eligible touchpoints, lookback definition, time window and limitations. A single event can be reported by several providers; do not sum all vendor-reported conversions as unique customers. Preserve provider claims separately from deduplicated internal results. Unknown attribution stays unknown. Revenue/return metrics account for source definitions, currency and refunds; projections remain separate from realized amounts.

## Acceptance

ME-01: Duplicate callbacks and multi-provider reporting do not create duplicate canonical conversions when identity can be resolved; unresolved duplicates are disclosed.

ME-02: A report identifies metric definition, attribution version, data freshness and missing tracking.

ME-03: CRM sync cannot grant marketing consent or overwrite externally mastered data without configured authority.

See [service backend](service-delivery-backend.md), [provider contracts](integrations-and-provider-interfaces.md) and D-009/D-025.
