# Publishing Checklist

This checklist is the release gate for the coding-LLM guide. It applies after the reader-facing article has been approved and before any production URL becomes indexable. Complete every applicable row with evidence in the release PR, deployment record, or publishing ticket.

> **Go / no-go rule:** A green build, approved copy, or valid Markdown is not sufficient for release. If any required item is incomplete, keep the page in draft status, retain `noindex`, and exclude the URL from the production sitemap.

## 1. Editorial and factual integrity

| Required check | Owner | Evidence of completion |
|---|---|---|
| The title, description, introduction, summary table, policy section, FAQ, and conclusion make the same task-based recommendation. | Content owner | Final diff or CMS preview reviewed as a whole. |
| Every price, model name, model ID, context limit, capability, availability, and integration statement has been checked against an appropriate primary source. | Subject-matter reviewer | Source URLs and verification date recorded in the article. |
| Promotional or temporary price language includes its relevant period and does not become a permanent default claim. | Subject-matter reviewer | Current provider page reviewed before release. |
| Citation links resolve and support the statements that cite them. | Content owner | Link-check result or manual review record. |
| The article clearly distinguishes vendor descriptions from independently established results. | Content owner | Editorial review complete. |

## 2. Page and SEO implementation

| Required check | Owner | Evidence of completion |
|---|---|---|
| The final canonical URL matches the intended production URL and the page self-canonicalizes. | SEO / implementation owner | Rendered `<link rel="canonical">` inspected. |
| The browser title and meta description match approved copy and have no CMS placeholders. | SEO / implementation owner | Production-like preview inspected. |
| The article page visibly shows a byline or publisher as appropriate, plus a truthful publication or modification date. | Content and implementation owners | CMS preview inspected. |
| Article JSON-LD matches the visible page, including headline, author, date fields, and final image URL. | SEO / implementation owner | Rich Results Test or equivalent validation result. |
| Structured data contains no draft tokens, sample URLs, placeholder dates, or claims not present on the page. | SEO / implementation owner | Final markup inspection. |
| The page is available to permitted crawlers and is not blocked by an unintended robots rule, login wall, or canonical conflict. | SEO / implementation owner | URL inspection or production-like crawl check. |

## 3. Images, accessibility, and social preview

| Required check | Owner | Evidence of completion |
|---|---|---|
| The hero image is present, relevant to the article, sharp at the displayed size, and served from a stable production URL. | Content and implementation owners | Page preview and asset URL checked. |
| Every meaningful image has concise, accurate alternative text; decorative assets are marked or handled appropriately by the CMS. | Content owner | Rendered HTML / accessibility review. |
| Images use responsive delivery or otherwise meet the site’s performance expectations without sacrificing clarity. | Implementation owner | Page-performance and device review. |
| `og:image` and relevant social metadata refer to an existing, crawlable, final asset. | SEO / implementation owner | Social-card preview inspected. |
| The model-routing diagram still matches the article’s written routing policy. | Content owner | Compare `assets/model-routing-framework.mmd`, rendered image, and article section. |

## 4. Links, internationalization, and page behavior

| Required check | Owner | Evidence of completion |
|---|---|---|
| Internal links use correct production paths and external links open the intended destinations. | Content and implementation owners | Link check complete. |
| If localized pages exist, each alternate URL returns HTTP 200, self-canonicalizes, and is represented accurately in hreflang markup. | SEO / implementation owner | Locale and markup verification record. |
| If localized pages do not exist, no hreflang reference points to a draft or nonexistent URL. | SEO / implementation owner | Final head markup inspected. |
| The page is usable at common desktop and mobile widths, including tables, images, and source references. | Implementation owner | Responsive browser check. |
| The page build, type check, lint, and relevant automated tests pass in the target project. | Implementation owner | CI or local build evidence. |

## 5. Release and monitoring

| Required check | Owner | Evidence of completion |
|---|---|---|
| A final production or staging URL returns the expected HTTP status and renders the approved article. | Publisher | URL verification record. |
| The release decision identifies the correct index state: draft / `noindex`, or intentionally indexable. | Publisher | Deployment setting and robots tag checked. |
| Once intentionally indexable, the canonical URL is added to the appropriate sitemap and submitted through the normal site process. | Publisher | Sitemap entry or submission record. |
| A post-release check confirms the live title, canonical, main image, social preview, schema, and key links. | Publisher and SEO / implementation owner | Post-release audit recorded. |
| A next fact-review date or event trigger is assigned. | Content owner | Maintenance record added to the planning system. |

## Release record

Complete this short record in the deployment ticket or final PR comment. It provides a clear audit trail without mixing temporary release notes into reader-facing copy.

| Field | Record |
|---|---|
| Final URL |  |
| Publisher |  |
| Content owner |  |
| Verification date for facts and pricing |  |
| Structured-data validation URL / result |  |
| Social-preview validation result |  |
| Indexing decision |  |
| Sitemap action |  |
| Follow-up review date or trigger |  |

A change to any factual claim, structured-data value, production image URL, or index setting after this record is complete requires a targeted recheck of the affected rows before release.
