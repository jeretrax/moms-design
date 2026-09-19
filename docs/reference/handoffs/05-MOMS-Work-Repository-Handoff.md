# Handoff to Work - Create and Reconcile MOMS Design Repository

## Objective

Create and initialize the canonical design repository `moms-design` for
**MOMS - Marketing Operations Management System** using the accompanying
handoff documents as source material.

## Instructions

1.  Review all MOMS handoff files together.
2.  Create the initial canonical design document structure.
3.  Reconcile duplicate concepts rather than copying the handoffs
    verbatim into multiple canonical documents.
4.  Create `REPO_START_HERE.md` as the entry point.
5.  Create and maintain `docs/design/master-design-index.md`.
6.  Capture unresolved decisions in `docs/design/design-notes.md`.
7.  Define the first Engineering Work Package around the first vertical
    slice only:
    -   customer/domain intake
    -   ordinary-language business goals
    -   public website assessment
    -   search-intent/keyword discovery
    -   relevant search/competitor observations
    -   prioritized Marketing Work Items
    -   customer-facing SEO/site optimization report
    -   persisted baseline
8.  Do not include Google Ads write operations in the first Engineering
    Work Package.
9.  Preserve Google Ads read/recommend and later controlled execution as
    approved product design.
10. Define deterministic controls for spend, permissions, approvals, and
    audit logging.
11. Treat AI as an internal implementation mechanism. Customer-facing
    design should describe the managed marketing service and its
    outcomes.
12. Cross-reference related documents.
13. Do not silently invent material product behavior. Put ambiguities
    into design notes.
14. Commit and push the resulting canonical design to `moms-design`.
15. Report:
    -   files created
    -   files modified
    -   open design questions
    -   first Engineering Work Package boundary
    -   commit hash

## Canonical Product Statement

MOMS accepts a company's public domain and ordinary-language business
objectives, determines how the company currently appears online,
discovers opportunities to acquire the desired business, converts those
opportunities into prioritized marketing work, obtains approvals where
necessary, executes authorized work, and measures the resulting benefit.

The first product proof is not "an AI chatbot for marketing."

The first product proof is:

**Give MOMS a business, a domain, a geography, and the type of customers
the business wants. MOMS returns a defensible, prioritized marketing
plan showing what to do, why to do it, what it may cost, what benefit is
expected, and when the result should be measured.**

## Governance

Use the same design-governance principle established for ITOMS:

**design conversation -\> Work reconciliation -\> canonical design repo
-\> bounded Engineering Work Package -\> implementation -\>
implementation findings back to design**

Material ambiguity discovered during implementation must return to
design rather than being silently resolved in code.
