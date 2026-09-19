# MOMS MVP Functional Specification

## MVP Objective

Deliver a usable subscription marketing service around three concrete
functions.

## Function 1 - Domain SEO and Site Optimization Assessment

### Inputs

Required:

-   Public-facing domain
-   Business description
-   Desired customers/business
-   Priority products/services
-   Target geography

Optional:

-   Current marketing priorities
-   Known competitors
-   Existing Google properties
-   Existing ad account
-   Customer budget

### Processing

The service should:

1.  Crawl and inspect the public website.
2.  Identify the company's apparent products, services, locations, and
    positioning.
3.  Translate business goals into search intents.
4.  Generate candidate keyword/topic families.
5.  Query current search results and available search data.
6.  Identify businesses/pages currently visible for relevant searches.
7.  Compare the customer's web presence with visible competitors.
8.  Identify technical, content, local, authority, and structural gaps.
9.  Generate prioritized Marketing Work Items.
10. Produce a customer-facing SEO/Site Optimization Report.

### Output

The report should include:

-   Executive summary
-   Current-state visibility summary
-   Business goals understood by MOMS
-   Search opportunities
-   Competitor observations
-   Immediate opportunities
-   Organic SEO opportunities
-   Site optimization findings
-   Local/presence opportunities
-   Paid-search opportunities
-   Prioritized Marketing Work List
-   Proposed benefit for each major action
-   Estimated effort/cost where practical
-   Expected measurement window
-   Recommended next decisions

### Marketing Work Item

Each work item should support:

-   ID
-   Customer
-   Goal
-   Category
-   Title
-   Description
-   Evidence
-   Recommended action
-   Proposed benefit
-   Expected measurement window
-   Estimated cost
-   Estimated effort
-   Priority
-   Confidence
-   Dependencies
-   Execution capability
-   Approval requirement
-   Status
-   Measurement method
-   Baseline
-   Result
-   Created date
-   Last evaluated date

Execution capability should distinguish:

-   Informational only
-   Human task
-   Agent can draft
-   Agent can execute with approval
-   Agent can execute within standing authorization

## Function 2 - Google Ads Management

### Phase A - Read and Recommend

Connect to a customer's Google Ads account with appropriate
authorization.

Read and analyze:

-   Campaigns
-   Ad groups
-   Keywords
-   Search terms where available
-   Ads
-   Spend
-   Budgets
-   CPC
-   Clicks
-   Impressions
-   Conversions where configured
-   Conversion cost
-   Geographic targeting
-   Negative keywords
-   Landing pages
-   Performance history

Generate:

-   Candidate keywords
-   Keyword groupings
-   Negative keyword recommendations
-   Budget recommendations
-   CPC observations/estimates
-   Campaign recommendations
-   Landing-page recommendations
-   Waste/anomaly findings
-   Spend pacing
-   Proposed changes

### Phase B - Controlled Execution

Support an approval workflow:

**recommendation -\> customer/internal approval -\> authorized change
-\> verification -\> measurement**

No agent action may exceed:

-   Customer-defined total ad budget
-   Account-level spending policy
-   Campaign-specific limits
-   Authorized action types
-   Required approval thresholds

The system must maintain an audit record of proposed and executed
changes.

### Customer Presentation

Avoid requiring the customer to interpret an advertising console.

Present questions such as:

-   What are we spending?
-   What are we getting?
-   What are people searching for?
-   Where are we wasting money?
-   What could we target next?
-   What would an additional budget likely purchase?
-   What changes need approval?

## Function 3 - Benefit and Measurement Timeline

MOMS should attach an expected measurement model to recommendations.

Suggested initial classes:

### Immediate / Activation

Examples: - Paid search visibility after campaign activation -
Correcting broken or missing basic site elements - Fixing obvious
listing errors

This means the activity can become active quickly, not that business
results are guaranteed immediately.

### Near-Term Measurement

Examples: - Paid campaign optimization - landing-page testing -
conversion improvements - local listing improvements - review-generation
activity

### Longer-Term Measurement

Examples: - Organic ranking work - authority development - content
portfolio growth - competitive search visibility improvements

The system must record the forecast/hypothesis and later compare it with
actual observed results.

## First Vertical Slice

The first implementation target is:

1.  Create customer.
2.  Enter domain.
3.  Enter ordinary-language business objective.
4.  Enter target geography.
5.  Run public assessment.
6.  Generate search-intent and keyword candidates.
7.  inspect relevant search competition.
8.  generate Marketing Work Items.
9.  prioritize them.
10. produce a readable customer report.
11. save assessment and baseline for future comparison.

Google Ads write access is not required for this first vertical slice.

## Success Criterion

A non-marketing customer should be able to read the resulting report and
understand what MOMS recommends doing next without needing to understand
SEO tools.
