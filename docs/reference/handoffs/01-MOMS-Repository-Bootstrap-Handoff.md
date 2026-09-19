# MOMS Repository Bootstrap Handoff

## Purpose

Create a new canonical design repository named `moms-design` for
**MOMS - Marketing Operations Management System**.

MOMS is a customer-facing managed marketing service powered by AI and
automation. Customers should experience it as a marketing service, not
as a collection of AI agents. The system should accept business
objectives in ordinary language, translate those objectives into
marketing opportunities, recommend and eventually execute approved work,
measure results, and continuously improve the plan.

## Canonical Design Authority

Once created, the `moms-design` repository becomes the canonical design
authority for MOMS.

Use the same general governance pattern as the ITOMS design process:

-   Chat: design conversation, exploration, and specification drafting.
-   Work: design review, reconciliation, document creation, and
    repository maintenance.
-   `moms-design`: canonical approved product design.
-   Engineering implementation: derived from approved design through
    bounded Engineering Work Packages.
-   Implementation must not silently redefine product behavior.
-   Material design gaps discovered during implementation must be
    escalated back into design.

## Initial Repository Structure

Create at minimum:

-   `REPO_START_HERE.md`
-   `README.md`
-   `docs/design/master-design-index.md`
-   `docs/design/vision.md`
-   `docs/design/product-definition.md`
-   `docs/design/mvp-scope.md`
-   `docs/design/customer-experience.md`
-   `docs/design/agent-operating-model.md`
-   `docs/design/marketing-work-item.md`
-   `docs/design/seo-site-assessment.md`
-   `docs/design/google-ads-management.md`
-   `docs/design/benefit-and-time-model.md`
-   `docs/design/autonomy-approvals-and-spend-controls.md`
-   `docs/design/subscription-model.md`
-   `docs/design/domain-model.md`
-   `docs/design/design-to-implementation-governance.md`
-   `docs/design/engineering-work-package-template.md`
-   `docs/design/design-notes.md`

## Initial Product Boundary

The first implementation milestone is a complete vertical slice:

**Public domain + business objectives -\> research -\> SEO/site
assessment -\> prioritized Marketing Work List -\> customer-facing
report**

The second implementation capability is Google Ads integration.

The third is ongoing measurement of expected versus actual benefit.

Do not broaden the first engineering milestone into a complete digital
marketing platform before the first vertical slice works end to end.

## Required Review

Reconcile this bootstrap handoff with the separate MOMS Product Design
Handoff and MVP Functional Specification. Capture unresolved questions
in `docs/design/design-notes.md`.

Do not invent material product behavior where the handoff is ambiguous.
Record the ambiguity and escalate it for design resolution.
