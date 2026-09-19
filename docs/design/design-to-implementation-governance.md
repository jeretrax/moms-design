# Design-to-Implementation Governance

Status: source-backed authority model. Sources: H1, H5.

Chat supports exploration and drafting. Work reviews, reconciles and maintains documents. Published `moms-design` is the canonical approved product design. Engineering implements bounded Engineering Work Packages derived from it. Implementation findings return to design.

## Decision status

- Source-backed baseline: directly reconciled from the supplied handoffs.
- Derived constraint: necessary engineering guard to uphold an existing boundary, with no new commercial promise.
- Proposed: suggested architecture, schema, workflow, or implementation approach requiring evaluation.
- Open: material ambiguity awaiting resolution.

Creating this repository does not approve every proposal within it. Source handoffs remain provenance; canonical owner documents resolve duplication. A future user-approved decision updates the relevant owner document, design notes and traceability together. Record decision date, approver, rationale and affected requirements/packages.

## Work package discipline

Each EWP defines objective, source requirements, scope/exclusions, dependencies, contracts, control boundaries, acceptance criteria, validation evidence and escalation conditions. Use the [template](engineering-work-package-template.md). EWP-001 is the only populated initial package and covers public assessment only.

Record the baseline design commit at engineering kickoff. Implementation changes and verification artifacts identify EWP and requirement IDs. Later design commits identify affected work packages; engineering reports deviations and discoveries back to design. Code does not silently become product authority.

## Escalation

If implementation reveals missing behavior that materially changes customer outcomes, data access, pricing, permissions, spend, report meaning, retention, or scope: stop the affected portion, record the issue and options in [design notes](design-notes.md), request the product owner's decision, and resume that portion after the canonical document and EWP are updated. Continue unaffected authorized work where possible.

Ordinary reversible implementation mechanics may be chosen and documented without redefining product behavior. A release must not treat unresolved release blockers as approved defaults.

## Repository maintenance

Keep links and [master index](master-design-index.md) current; retain stable requirement IDs in [traceability](requirements-traceability.md); preserve original sources; record publication truthfully. No license, repository visibility, or production deployment authorization is inferred from creating a design package.
