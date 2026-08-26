# Content Workflow and Governance

This document governs how the coding-LLM guide moves from a maintained editorial draft to a production content page. It is designed to prevent a common failure mode: treating an approved Markdown file as if it were already a validated, indexable web page.

## Roles and ownership

The roles below may be performed by one person in a small team, but the responsibilities should remain distinct during review.

| Role | Primary responsibility | Must approve or verify |
|---|---|---|
| Content owner | Maintains reader value, structure, editorial scope, and final copy. | Reader-facing accuracy, clarity, recommendation framing, and references. |
| Subject-matter reviewer | Challenges technical and comparative claims. | Model capabilities, pricing units, workflow recommendations, caveats, and date-sensitive wording. |
| SEO / implementation owner | Translates approved copy into a production page. | Canonical URL, metadata, internal links, social preview, Article JSON-LD, image delivery, and index controls. |
| Publisher | Makes the release decision after all other gates are complete. | Live-page behavior, production status, sitemap inclusion, and monitoring handoff. |

## Content lifecycle

| Status | What is true | Permitted work | Not permitted |
|---|---|---|---|
| Draft | The article is under development or contains unverified changes. | Editorial edits, source collection, visual exploration, internal review. | Indexing, sitemap inclusion, production promotion, or claims of final publication readiness. |
| Content-approved | Reader-facing copy has passed editorial and factual review. | CMS implementation and technical QA preparation. | Assuming schema, links, social cards, or rendering are correct without testing. |
| Implementation-ready | The final CMS/page configuration is known and required metadata values are available. | Page build, preview, structured-data validation, performance and link testing. | Production release before all applicable checklist items pass. |
| Release-approved | Content, page implementation, and final QA are complete. | Production publish and controlled removal of draft safeguards. | Introducing unreviewed content or asset changes. |
| Published | The page is live and crawlable by design. | Monitoring, periodic refreshes, corrections, and controlled updates. | Letting prices, model identifiers, or availability claims age without review. |

## Source-of-truth map

| Question | Source of truth |
|---|---|
| What will a reader see? | `BestLLMforCodingin2026_ChoosebyTaskandCost.md` |
| How should the page be implemented? | `seo/coding-models-publication-handoff.md` |
| How should the guide be changed and reviewed? | `CONTRIBUTING.md` |
| Is a release safe to perform? | `docs/PUBLISHING_CHECKLIST.md` |
| How are visual assets maintained? | `assets/`, with source files retained beside rendered assets where applicable |
| How should a PR be described? | `.github/pull_request_template.md` |

## Factual-refresh policy

The article’s subject matter changes quickly. Start a factual-refresh review whenever a provider changes a model name, model version, list price, context limit, supported tool interface, availability, promotional term, or documentation position that the article cites. Also refresh after a material change to the ApiFlux model catalog, integration workflow, displayed pricing, or supported protocol statement.

A factual refresh is complete only when the changed statement is verified against the relevant primary source, the source URL remains usable, the article’s verification language still matches reality, and the reviewer determines whether the title, summary table, recommendation, FAQ, and publication metadata need to change together. Avoid a partial refresh that updates a single price while leaving an inconsistent verdict elsewhere in the article.

## Change categories and review depth

| Change | Minimum review | Additional release impact |
|---|---|---|
| Grammar, formatting, or clarity without changed meaning | Content owner review | None beyond standard Markdown and link checks. |
| New or modified external link | Content owner review | Confirm destination, anchor text, and whether the linked claim is still supported. |
| Price, model capability, model ID, context, or availability | Subject-matter review with primary source | Refresh dates and all related comparative statements; consider a new social preview if the message changes. |
| Recommendation or model-tier routing | Subject-matter and content-owner review | Update the route diagram source and rendered image if the policy changes. |
| Hero image or social metadata | Content and implementation-owner review | Validate the actual social card, alternative text, final image URL, and page performance. |
| Canonical, schema, robots, sitemap, hreflang, or publication status | Implementation-owner and publisher review | Run live-environment checks before release or index-state changes. |

## Change-control rules

Keep a pull request focused on one logical outcome. Do not mix a factual model refresh with unrelated formatting cleanup, image experiments, or template reorganizations unless the relationship is explicitly explained. Keep reviewer comments traceable by naming the affected section or file. If a claim cannot be verified with a credible source, soften or remove it rather than retaining an unsupported assertion.

When a change affects the article’s core promise, update all surfaces that make that promise: the H1 and description where relevant, the first summary, comparison table, FAQ answer, visual assets, social copy, and structured-data values. This protects readers from a page whose title, body, image, and metadata describe different things.

## Periodic maintenance cadence

Use an event-driven review for provider or product changes, then schedule a broader content review at an interval that matches the pace of the market. A monthly scan is appropriate while the guide is actively competing for fresh model-comparison queries; a quarterly review may be enough if the page is stable and its claims are narrowly scoped. Each review should record whether the page remains current, needs a factual refresh, or should be reclassified as a dated historical snapshot.
