# MVP Scope and Delivery Sequence

Status: source-backed design baseline. Sources: H1, H3, H5.

The MVP vision has three functions. The first engineering milestone is a narrower complete vertical slice, not all three functions at once.

| Milestone | Deliverable | Execution boundary |
| --- | --- | --- |
| M1: Public assessment | Intake, crawl, intent/keyword candidates, current search/competitor observations, prioritized work, readable report, persisted baseline | Public research and internal recommendations only |
| M2: Google Ads Phase A | Authorized account read, performance and pacing analysis, keyword/CPC/budget recommendations | No Google Ads mutations |
| M3: Ongoing measurement | Compare recorded forecasts and baselines to later observations; reassess priorities | Read and analyze; execution authority remains separate |
| Subsequent gated package: Ads Phase B | Recommend, approve, execute, verify, measure | Only specifically approved or standing-authorized changes |

M1 includes an expected benefit and measurement window on recommendations. M3 adds ongoing actual-versus-expected comparison; its later placement does not defer M1 forecast fields.

M1 may identify paid-search opportunities from public or available licensed data. It does not require a connected Ads account, fabricated CPC figures, or Ads write permission.

## M1 included

Create customer; capture domain, business description, ordinary-language goals, desired customers, priority products/services, and geography; inspect the public site; discover search intents and topic families; inspect relevant competition; create and prioritize Marketing Work Items; generate a report; persist assessment and baseline.

## M1 excluded

Ads account integration, external mutation, campaign activation, autonomous publication, ongoing monitoring schedules, subscription checkout, a complete content-production system, social posting, and broad platform expansion. Future capabilities remain in approved product scope but need their own packages.

The [first EWP](../engineering/EWP-001-public-domain-assessment.md) owns the implementation boundary and acceptance criteria. [Design notes](design-notes.md) list unresolved release and provider decisions.

## Post-assessment capability expansion

See [agency growth expansion](agency-growth-expansion.md) for R-018 through R-025 and delivery dependencies. The original M1/M2/M3 sequence remains intact. New acceptance criteria belong to future bounded work packages, not EWP-001. Drafting, publishing, outreach, report delivery and commerce each have separate gates.

## Backend expansion boundary

[R-026 through R-034](managed-marketing-backend-expansion.md) add future managed-service backends. EWP-001 remains unchanged. Introduce shared orchestration and read adapters before separately gated channel writes. New owner-document acceptance criteria require future bounded EWPs; they are not a requirement to build every service before delivering M1.

## Intelligence expansion

R-035 through R-041 add future intelligence/engagement requirements and consolidate existing capability ownership. [Ownership and rollout](capability-ownership-and-reconciliation.md) define dependencies. M1/EWP-001 remain unchanged; research data coverage, case roles and creator payment support require explicit decisions before release.
