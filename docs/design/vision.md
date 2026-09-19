# Vision

Status: source-backed design baseline. Sources: H1, H2, H5 in the [source register](../reference/handoffs/README.md).

MOMS is a customer-facing managed marketing service powered internally by AI, deterministic automation, data sources, and human approvals. A business describes the customers and work it wants; MOMS translates that intent into research, opportunities, recommendations, work, and measurement.

The customer should be able to answer: Where are we now? What should we do? What will it cost? What benefit do we expect? When can we measure it? What happened afterward?

The operating loop is observe → understand → recommend → approve → execute → measure → learn. The service's value is the ability to move from evidence to useful action and reassess it, rather than only displaying metrics.

## Principles

- Business goals precede keyword lists and channel choices.
- Recommendations explain evidence, benefit, effort, cost, uncertainty, and a useful measurement window.
- Authorization governs execution; AI cannot grant itself authority.
- Results are observed and compared to a recorded hypothesis, not retrospectively substituted for the original forecast.
- Organic rankings and dates are never guaranteed; activation is different from business results.
- Legitimate participation and useful content take precedence over deceptive personas, spam, and manufactured links.
- Data and model providers are replaceable implementation dependencies.

See [product definition](product-definition.md), [MVP scope](mvp-scope.md), and [benefit model](benefit-and-time-model.md).
