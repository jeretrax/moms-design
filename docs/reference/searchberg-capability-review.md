# Search Berg Service Review

Reviewed 2026-09-19 from public first-party marketing pages. The user requested backend design to support comparable services. No authenticated product access, private architecture inspection or performance validation was performed.

| Public source | Observed offering | MOMS mapping |
| --- | --- | --- |
| [Homepage](https://www.searchberg.com/) | Broad marketing catalog, managed delivery, client review and periodic activity/results reporting | [Service backend](../design/service-delivery-backend.md) |
| [Paid marketing](https://www.searchberg.com/ppc-marketing/) | Paid media and campaign optimization | [Campaign backend](../design/multichannel-campaign-backend.md) |
| [Social services](https://www.searchberg.com/social-media-management/) | Social presence and related service offerings | [Social backend](../design/social-email-and-community-backend.md) |
| [Email services](https://www.searchberg.com/email-marketing/) | Managed email marketing | [Email backend](../design/social-email-and-community-backend.md) |
| [Local SEO](https://www.searchberg.com/local-seo-services/) | Local presence and citation services | [Local backend](../design/local-presence-and-reputation-backend.md) |
| [Reputation](https://www.searchberg.com/reputation-management-services/) | Business/personal reputation services | [Reputation backend](../design/local-presence-and-reputation-backend.md) |
| [Web development](https://www.searchberg.com/web-design-development-services/) | Business/ecommerce web delivery and related maintenance offerings | [Web backend](../design/web-commerce-and-creative-backend.md) |
| [Amazon marketing](https://www.searchberg.com/amazon-marketing/) | Marketplace listing, storefront, promotion and advertising work | [Commerce backend](../design/web-commerce-and-creative-backend.md) |
| [Video services](https://www.searchberg.com/video-design-services/) | Script, storyboard and production services | [Creative backend](../design/web-commerce-and-creative-backend.md) |

The catalog overlaps existing MOMS design. New documents add service orchestration and missing channel backends; they do not replace current owner documents. Proposed schemas, commands, events, queues, transaction semantics and controls are MOMS engineering inferences, not observed competitor implementations. No competitor pricing, guarantees, contractual terms, capacity figures or turnaround commitments are adopted. Advertised channels may include legacy formats; current API support must be verified before implementation.
