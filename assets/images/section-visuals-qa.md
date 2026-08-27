# Section visuals QA — replacement screenshots

## Replacement status

The three previous mascot-led illustrations are withdrawn from this pull request. They are replaced by three `1280 × 720` information snapshots in which the article’s factual logic is primary and the supplied mascot is a small fixed upper-right anchor.

| File | Information job | Mascot source and placement | Background result | Factual boundary | Result |
|---|---|---|---|---|---|
| `coding-task-tier-snapshot.png` | Explains predictable, daily production, and high-risk task tiers. | Original `mascot-waving.jpg`, 102 px, upper-right. | Pass: matching continuous `#0D0D15` canvas; no tile, frame, border, or sticker. | Labels are direct summaries of the nearby routing text; no model ranking or price. | Pass |
| `coding-model-evaluation-snapshot.png` | Explains same environment, same task set, and same checks. | Original `mascot-front-welcome.jpg`, 98 px, upper-right. | Pass: matching continuous `#070915` canvas; non-subject source margin cropped; no tile, frame, border, or sticker. | Labels are direct summaries of the nearby evaluation text; no benchmark or measured result. | Pass |
| `unified-coding-workflow-snapshot.png` | Explains shared input, common run, and decision record. | Original `mascot-waving.jpg`, 102 px, upper-right. | Pass: matching continuous `#0D0D15` canvas; no tile, frame, border, or sticker. | Labels are direct summaries of the nearby workflow text; no real product UI or protocol claim. | Pass |

## Required implementation condition

The production CMS must preserve the article image references, alt text, and captions. Do not reuse these section visuals as Open Graph images, and do not add a second logo or mascot overlay in the CMS.
