# Contributing to the Coding-LLM Guide

This repository is maintained as an editorial content package. Contributions are welcome when they make the guide more accurate, clearer, easier to implement, or more useful to readers. Every change must preserve the distinction between **reader-facing article copy** and **implementation-only publishing instructions**.

## Choose the right change type

| Change type | Typical files | Required review focus |
|---|---|---|
| Editorial improvement | Article Markdown, README, workflow documents | Accuracy of meaning, clarity, scope, and useful structure. |
| Factual refresh | Article Markdown and source citations | Primary-source verification, access date, model ID, units, pricing assumptions, and wording that matches the source. |
| SEO implementation update | `seo/` handoff, publication checklist | Consistency with visible page copy, canonical URL, dates, schema, social metadata, and indexing controls. |
| Visual-asset update | `assets/images/`, `assets/*.mmd`, alt text references | Relevance to nearby content, accessibility text, responsive-use implications, file naming, and source-file preservation. |
| Release preparation | Multiple files | Completion of every required release check; approval does not replace live-page QA. |

## Contribution workflow

Start from the current review branch or create a focused branch from the appropriate base. Make only changes necessary for one editorial outcome, then explain that outcome in the pull request. The preferred sequence is shown below.

| Step | Required action | Completion signal |
|---|---|---|
| 1. Classify | Identify whether the change is editorial, factual, technical SEO, visual, or release-related. | The PR scope is unambiguous. |
| 2. Edit | Update the smallest relevant set of files. Keep reader copy separate from internal implementation notes. | The diff has no unrelated reformatting or speculative product claims. |
| 3. Verify | Check citations, link targets, dates, terminology, image references, and affected checklist items. | Every changed claim or asset has an auditable basis. |
| 4. Review locally | Run `git diff --check` and inspect the final diff. | There are no whitespace errors, accidental files, or unreviewed asset changes. |
| 5. Open or update a PR | Use the repository PR template and explain reader impact, implementation impact, and remaining release work. | A reviewer can make a decision without reconstructing the context. |

## Editorial standards

### Preserve the article’s decision framework

The guide should remain a task-based evaluation framework. It should not drift into an unqualified “best model” ranking, provider marketing copy, or a price-only comparison. Recommendations must remain conditional on the reader’s workload, verifier, reliability target, latency requirements, and total accepted-task cost.

### Treat time-sensitive claims as factual edits

Model names, context limits, pricing, availability, vendor capability claims, and compatibility statements change quickly. Use the provider’s own documentation as the default source. Record or update the article’s verification date when substantive facts change, use precise units, and state any assumptions that affect a comparison. Do not infer unlisted pricing, features, benchmark outcomes, or availability.

### Keep citation and link quality high

Every factual paragraph that relies on a source should point readers to a direct, stable source URL. Preserve existing reference-style citations unless there is a clear editorial reason to change them. Replace broken links, remove obsolete links, and check that a cited source actually supports the adjacent statement before merging.

### Write for a technical decision maker

Lead with a short direct answer, then provide the reasoning and decision criteria. Use descriptive headings, short paragraphs, and tables only where comparison improves comprehension. Define a success criterion before presenting an evaluation method. Avoid vague superlatives, unverifiable competitive claims, keyword stuffing, and repeated calls to action.

## Visual-asset standards

Images are part of the page’s semantic content, not decoration. Use meaningful filenames, place each image near the section it supports, and provide concise alt text that describes the decision-relevant information. Do not use text baked into an image when the same information needs to be accessible, translatable, or updated frequently.

For structured diagrams, maintain the editable source beside the rendered output. The model-routing image is generated from `assets/model-routing-framework.mmd`; update and review both the source and rendered PNG together. When replacing a social or hero image, update the corresponding image URL and preview checks in `seo/coding-models-publication-handoff.md`.

## Pull-request expectations

A PR should state the reader-facing impact in plain language and identify any publishing work that still remains. Use `.github/pull_request_template.md` as the review record. Do not mark a page ready to publish merely because copy is approved; production implementation, rendered metadata, structured data, images, links, and indexing controls require their own validation.

Before requesting review, run:

```bash
git diff --check
git status --short
git diff --cached --check  # when changes are staged
```

> **Publication safeguard:** Never remove a draft or `noindex` safeguard unless the corresponding release checklist is complete and the final page implementation has been verified in the intended production environment.
