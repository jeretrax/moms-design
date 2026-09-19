# AI Search Visibility

Status: user-requested capability expansion, 2026-09-19. Requirement R-019. Reference: [Adaptify AI visibility](https://adaptify.ai/features/ai-visibility).

Track customer and competitor appearances in sampled AI answers. Generate business-relevant questions, accept manually supplied or imported prompts, group follow-up questions, inspect mentions and cited URLs, and turn missing coverage into content work. Provide list and relationship views and compare later observations after authorized changes. Target coverage includes ChatGPT, Claude, Gemini, Perplexity and Copilot where a valid collection method is available; support is subject to integration verification.

## MOMS measurement contract

Each observation records prompt/version, customer, platform and collection surface, model/version where available, geography/language, capture time, retrieval settings where known, response evidence, citations, errors and interpretation confidence. A model API response is not proof of the consumer search experience. Label the tested surface explicitly. Generated questions are hypotheses about customer interest, not observed query-volume data.

A failed run is unknown, not an absent mention. Visibility summaries show successful sample denominators, failed samples and observation dates. Separate brand mention, linked citation, recommendation and interpreted sentiment. Changes to prompts, models or collection surfaces limit comparisons; retain those boundaries. Retest previously successful prompts as well as gaps to detect regressions. Cadence, samples and score design remain D-014.

## Acceptance

AI-01: A reviewer can reproduce the context of each reported mention/citation from retained evidence.

AI-02: Failed samples cannot lower visibility as if they were successful negative observations.

AI-03: A gap creates or links a work item and later measurement, without bypassing content approval.

See [benefit model](benefit-and-time-model.md) and [provider contracts](integrations-and-provider-interfaces.md).
