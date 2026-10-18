# Sandy Getting Started: Step 1 — Company Identity and Online Presence Discovery
Status: user-confirmed functional workflow, 2026-10-17. Design only; not implemented.

## Purpose
Start with company name and optional address, domains, Facebook, Instagram, other social profiles and known URLs. A website is not required. Discover, catalog and correlate publicly accessible references before conducting deeper audits.

## Workflow
1. Intake company name (minimum), plus known identifying anchors.
2. Search public directories, sites, social profiles/posts, parent/sister/affiliate websites, brands, divisions, locations and other references. Include digital-risk intelligence references where lawfully available.
3. Record immutable discovery provenance: source URL/provider, observation timestamp, captured identifiers, evidence, inferred identity/relationship, source reliability and confidence. Distinguish absence of evidence from verified absence.
4. Propose identity/resource relationships for human confirmation. Reviewer may confirm, reject, merge true duplicates, separate entities, reassign, request more investigation, and add editable relationship type, notes and plain-language description.
5. Save confirmed, annotated identity map and resource catalog; keep original evidence and decision history, and retain unresolved cases in a review queue.

An online presence item may reference multiple companies or identities. Links are referential and do not establish ownership, administrative access, or permission to change a resource. Confirming that a security claim refers to a company does not verify the claim itself.

## Digital risk discovery
Catalog legitimate reports of domain/email breach exposure, ransomware claims, website compromise, phishing/impersonation, leaked information and criminal-forum/dark-web references. Record source, date, evidence summary, affected identity, confidence and verification status; avoid storing stolen credentials or leaked documents. Review identity association at the same confirmation checkpoint.

## Monitoring
Manual discovery scans are available. Continuous discovery scans default to every seven days, with configurable interval. Revisit known resources and search for new references; maintain coverage and change history. Provider access, rate limits and escalation behavior require separate implementation decisions.

## Completion
Initial scan coverage and limitations documented; proposed identities reviewed or deferred; confirmed relationships saved; outstanding questions tracked. Output: Company Identity and Online Presence Registry.

## Integration
Use existing [MOMS Domain Model](../domain-model.md) Customer/Business Profile, Web Property, Assessment, Evidence/Observation and Job/Audit Event concepts. Do not introduce competing canonical entity definitions; physical schema and organizational ontology alignment remain design work. See [Step 2](getting-started-step-2.md).
