# Agency Portal and Reporting

Status: user-requested capability expansion, 2026-09-19. Requirements R-023/R-024. Reference: [Adaptify reporting](https://adaptify.ai/features/white-label-reporting).

Provide agency-branded customer portals, custom domains, logos/colors, PDF reports, recurring summaries and configurable notifications. Customers can review drafts, provide feedback, approve authorized work and inspect results. Reporting combines delivered content, technical work, links, search performance and AI visibility. Configure visible sections and delivery schedules per customer, with agency-controlled sender and reply routing.

## MOMS portfolio and access design

Add an agency portfolio view with explicit customer context, pending decisions, failed jobs, disconnected integrations, usage and upcoming work. Cross-customer aggregation is restricted to authorized agency staff; client views query only permitted records. Branding and hidden navigation are not access controls. Custom-domain routing must validate tenant ownership rather than trusting an arbitrary hostname.

Reuse canonical reports, measurements and approvals. Scheduled deliveries record recipient, authorized scope, report revision and outcome, and recheck recipient permission before sending. Retrying a job must not send duplicate summaries. Email summaries use verified results and distinguish recommendations from completed work.

Portal authentication and revocable scoped sharing are D-017; do not adopt an unrestricted bearer link as approval identity. A shareable report does not confer spending or publication authority. Retention and deletion inherit D-005. No messages are sent by this design task.

## Acceptance

AR-01: Switching agency/customer context never exposes another customer's report or approval.

AR-02: Branded PDF, portal and summary reconcile to the same report revision and evidence.

AR-03: Revoked access prevents new deliveries and portal retrieval; every approval identifies the authorized actor and content version.

See [customer experience](customer-experience.md) and [report contract](report-contract.md).
