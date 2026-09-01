# Research Notes — 2026-08-27

## Public PR baseline

The public pull request is accessible at `https://github.com/tom61-bl/best-llm-for-coding-2026/pull/1`. At review time it contained three commits, twelve changed files, no automated checks, no reviewers, no labels, and no discussion. The PR description clearly identifies the content, visual, SEO, documentation, and draft-indexing scope. The repository is public; therefore, all draft content and implementation documents are externally visible.

## OpenAI source verification

Source reviewed: [OpenAI API — Models](https://developers.openai.com/api/docs/models).

The official catalog identifies GPT-5.6 Sol as the starting option for complex reasoning and coding, GPT-5.6 Terra as the model balancing intelligence and cost, and GPT-5.6 Luna as the model for cost-sensitive, high-volume workloads. The catalog reports a 1.05M context window for Sol, Terra, and Luna. At the time reviewed, Sol was listed at $4 input / $20 output per MTok, Terra at $2 / $12, and Luna at $0.20 / $1.20. Therefore, the article’s OpenAI pricing values ($5 / $30 for Sol and $1 / $6 for Luna) are stale and must be refreshed before the content is presented as current.

## Initial SEO implication

The current reader-facing slug `/coding-models` is concise and brand-aligned, but it does not include the article’s most specific primary query. The best decision depends on whether that URL already has backlinks, traffic, or an established information architecture. For a new, unlaunched page, `/best-llm-for-coding` is more query-descriptive while remaining short, stable, and future-proof. A year should not appear in the slug because the guide is intended to be updated rather than replaced annually. If `/coding-models` is already live or indexed, preserve it and use the article title, on-page H1, metadata, internal linking, and canonical configuration to express topical relevance; do not change a live canonical path without redirect and migration planning.

## Anthropic source verification

Source reviewed: [Claude Platform Docs — Models overview](https://platform.claude.com/docs/en/models/overview).

The official overview positions Claude Opus 5 for complex agentic coding and enterprise work, and Claude Sonnet 5 as the best combination of speed and intelligence. It lists a 1M-token context window for both. At review time, listed public API pricing was $5 input / $25 output per MTok for Opus 5 and $2 / $10 for Sonnet 5. Therefore, the article’s Opus 5 price remains aligned with the provider documentation, while the article’s Sonnet 5 normal list-price statement of $3 / $15 does not match the currently displayed public API price and must be refreshed. The provider also lists a higher-capability Claude Fable 5 tier; a near-production article should either explain why it is excluded from the shortlist or include it in the evaluation framework.

## Gemini source verification

Source reviewed: [Google AI for Developers — Gemini models](https://ai.google.dev/gemini-api/docs/models).

Google identifies Gemini 3.7 Flash as its latest and most capable Flash model for complex coding, agentic workflows, and reliable multi-step execution. Gemini 3.6 Flash is positioned as the previous-generation Flash model, balancing speed and multimodal capabilities across general agentic and everyday tasks. This means the article’s description of Gemini 3.6 Flash as the speed-focused candidate is directionally compatible, but a current-comparison article should acknowledge Gemini 3.7 Flash or make a documented reasoned exclusion. The reviewed page did not provide the exact 3.6 Flash token-pricing figures in the extracted content, so those values require verification on the current pricing page before an article update.

## Content-quality implication

A near-production update should not merely alter individual table cells. It should reconcile the primary shortlist, pricing table, summary, verdict paragraphs, practical selection policy, FAQ, routing diagram, metadata date, and citation record in one editorial refresh. The article should make the distinction between direct-provider list prices and ApiFlux displayed / billed prices explicit, then link to the current ApiFlux Models page as an implementation check rather than presenting an unverified static gateway price.

## DeepSeek source verification

Source reviewed: [DeepSeek API Docs — Models & Pricing](https://api-docs.deepseek.com/quick_start/pricing/).

The provider documents DeepSeek V4 Pro as `DeepSeek-V4-Pro-0813` with a 1M-token context length, JSON output, tool calls, Responses API support, Anthropic API support, chat-prefix completion, and non-thinking / thinking modes. Its displayed peak pricing is $1.32 for cache-miss input and $3.96 for output per MTok, while off-peak prices are half those amounts. The current article’s $0.435 cache-miss / $0.87 output figures therefore do not match the reviewed official pricing. A corrected table must distinguish peak and off-peak rates instead of presenting a single number without conditions.

## ApiFlux model-directory verification

Source reviewed: [ApiFlux Models](https://apiflux.ai/models).

The public directory is accessible and describes prices as per one million tokens, including reviewed cache rates where applicable. It states that ApiFlux prices are shown in USD per one million tokens and visually presents the platform as charging 15% below makers’ official list price. The directory lists the relevant current model family entries, including Gemini 3.7 Flash, Claude Opus 5, GPT-5.6 Sol, GPT-5.6 Luna, GPT-5.6 Terra, Claude Sonnet 5, and Claude Fable 5. This supports linking readers to the directory for live availability, but its price cards remain dynamic product information and should not be represented as a fixed, evergreen static price snapshot in the article.

## URL and internal-link implications

For a new content page, the recommended canonical path is `/best-llm-for-coding`. It directly expresses the primary query, remains human-readable, and avoids including a volatile year. The existing `/coding-models` path should become a future-proof topic-hub route or redirect to the canonical article route if it has not yet been indexed. This recommendation is conditional on the page not being live: if it already receives traffic, links, or has an existing canonical history, retain the current URL and make any migration only with a permanent 301 redirect, updated canonicals, internal-link updates, sitemap revision, and post-migration monitoring.

## Official URL-structure guidance

Source reviewed: [Google Search Central — URL structure best practices](https://developers.google.com/search/docs/crawling-indexing/url-structure).

Google recommends descriptive URLs, hyphens between words, and logical paths intelligible to people. It also warns that unnecessarily complex URLs can cause crawl inefficiency. This supports a short, descriptive, hyphenated canonical slug; it does not support adding every keyword variant or a changing year to the path.

## ApiFlux blog information architecture

Source reviewed: [ApiFlux Blog](https://apiflux.ai/blog).

The public blog uses the `/blog/<descriptive-slug>` pattern. Its existing article appears at `/blog/qwen3-8-release-window-prep`, while the blog index is `/blog`. To align this content with the existing structure, the strongest new-page recommendation is therefore `https://apiflux.ai/blog/best-llm-for-coding`, not a root-level `/coding-models` route. The slug is descriptive, hyphenated, query-aligned, concise, and not date-bound. The site can retain `/coding-models` in the future as a model-directory or comparison-hub route, but it should not canonicalize the same article at both URLs. If the root path was never deployed, there is no migration cost; otherwise a permanent redirect and internal-link update are required.

## Recommended final URL decision

Use the canonical URL `https://apiflux.ai/blog/best-llm-for-coding` for this new article, subject to confirming the page has not already gone live at `/coding-models`. Use `Best LLMs for Coding in 2026: Choose by Task & Cost | ApiFlux` as the on-page H1 and current editorial title. This separates the stable content identity from the annually refreshed title. It also follows the website’s existing blog architecture rather than introducing an isolated URL convention.

## Gemini pricing verification

Source reviewed: [Google AI for Developers — Gemini Developer API pricing](https://ai.google.dev/gemini-api/docs/pricing).

At review time, both Gemini 3.7 Flash and Gemini 3.6 Flash were displayed at $0.75 input / $3.75 output per MTok through December 31, 2026, with listed increases beginning January 1, 2027. The page lists paid-tier context caching at $0.075 per MTok through December 31, 2026, plus $0.50 per MTok per hour for storage. Gemini 3.7 Flash is described as the most capable Flash model for agentic workflows and multimodal reasoning; Gemini 3.6 Flash is described as a speed-focused Flash model with search and grounding strengths. The article’s original $1.50 / $7.50 Gemini 3.6 pricing therefore requires correction and should include the time-bound price condition.

## Helpful-content quality guidance

Source reviewed: [Google Search Central — Creating helpful, reliable, people-first content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content).

Google’s guidance emphasizes helpful, reliable information created for people rather than ranking manipulation. It prompts reviewers to assess originality, substantial coverage, analysis beyond a source rewrite, descriptive non-sensational titles, transparent sourcing, author or site background, subject-matter review, and the absence of easily verifiable factual errors. It also cautions against changing dates without meaningful content changes. Therefore, this article should add a transparent editorial methodology, a named or organizational byline with an About-page link, a last-verified disclosure tied to a substantive factual refresh, and an explicit note that the recommendations are an evaluation shortlist rather than benchmark claims.

## Visual asset validation

The dedicated social asset was verified at 1200 × 630 pixels. Its central AI-routing hub, coding workspace, and analytics panel remain safely visible within the social-preview crop, and it contains no critical text that could become stale or inaccessible. The updated routing diagram was rendered successfully from its Mermaid source and visually confirms the latest article policy: Claude Opus 5 / GPT-5.6 Sol for frontier work; Claude Sonnet 5 / GPT-5.6 Terra for balanced work; Gemini 3.7 Flash / GPT-5.6 Luna / DeepSeek V4 Pro for fast or cost-focused work; and Claude Fable 5 only as a deliberate highest-capability evaluation after escalation.
