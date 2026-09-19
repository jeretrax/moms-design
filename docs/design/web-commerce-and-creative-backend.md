# Web, Commerce and Creative Delivery Backend

Status: user-requested capability expansion; R-031/R-032/R-033. References: [Search Berg website services](https://www.searchberg.com/web-design-development-services/), [Amazon marketing](https://www.searchberg.com/amazon-marketing/) and [video production](https://www.searchberg.com/video-design-services/).

Comparable service scope covers business/storefront websites, ongoing maintenance, marketplace listing work and media production. MOMS coordinates these as managed engagements with specialist delivery and verified external execution, not an automatic promise to generate any arbitrary application.

## Website, landing page and maintenance delivery

WebsiteProject links requirements, approved design/artifact revisions, source repository, preview/staging/production targets, assigned implementers and acceptance conditions. Application-development and CRM-implementation engagements can use the same project structure with their own bounded engineering specifications. Track deployment artifacts, preconditions, backup/rollback references and verification separately from ordinary content publication.

Release actions require explicit target authority, approved revision, staging evidence and change window where configured. Detect changed remote state before replacing it. Hosting is a managed-provider relationship with renewal, health, backup and incident records; it is not a new hosting platform commitment. DNS, certificate, runtime configuration and production deployment changes are distinct controlled actions. Landing-page experiments require a measurement plan and separate release approval.

## Ecommerce and marketplaces

ProductReference binds customer-owned catalog identity to store/marketplace identifiers, locale and source-of-truth system. ListingRevision holds proposed text/media/metadata changes and supporting claims. Ingest feeds into staging, validate identifiers and required fields, then submit approved changes with per-item results. Do not treat partial batch success as total success. Catalog price/inventory are externally mastered unless a separately approved integration changes that authority.

Marketplace account/brand verification, listing optimization, storefront creative, promotions and paid campaigns are related tasks with separate permissions. Promotion/price changes require specific commercial authority. Orders and refunds feed measurement through minimal required references; MOMS is not replacing fulfillment or the store ledger. Marketplace advertising uses the campaign backend rather than a separate spending system.

## Creative production

CreativeBrief links goal, channels, dimensions/duration, brand profile, source assets and desired deliverables. Script/storyboard/design revisions progress through review into render/transcode jobs and final accepted artifacts. Support graphics, infographics, video, audio and channel variants. Store source and derived assets separately with checksum, rights/usage provenance, accessibility metadata, approver and artifact lineage. Scan uploads and isolate processing workers. Generated visuals are not authoritative charts or factual evidence.

Creative production can be human, vendor or bounded AI work. Rendering success does not mean customer acceptance or publication. Podcast/video search and distribution work can reuse these records plus content metadata and channel adapters; no channel-specific support is implied without validation.

## Acceptance

WC-01: Production release requires target/version-matched authority and retains a verified outcome or explicit failure plus recovery path.

WC-02: Marketplace feed retries do not duplicate listings or change unapproved prices/inventory; partial failures remain visible.

WC-03: A final media asset traces to source rights and approved revisions; a rejected artifact cannot publish through a downstream channel.

See [CMS workflow](content-production-and-publishing.md), [campaign backend](multichannel-campaign-backend.md) and D-023.
