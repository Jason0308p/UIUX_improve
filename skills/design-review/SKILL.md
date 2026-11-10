---
name: design-review
description: Audit charts and data interfaces for evidence and usability.
version: 0.1.0
---
# Design review

## When to use
Use to audit an existing chart, dashboard, artifact or UI proposal. Reviews may target one aspect (evidence, accessibility, mobile, states) without forcing a full report.

## Procedure
1. Identify the artifact, audience, decision and available evidence. Specify what can and cannot be inspected (source data, code, screenshot or live interaction).
2. Check applicable IDs in `../../core/QUALITY_BASELINE.md`; label non-applicable items N/A and untested items unverified, not passed.
3. Look for high-impact failures first: unsupported claims, misleading scale/context, inaccessible critical information, broken primary task, missing relevant states. Do not equate visual novelty with quality.
4. Review **global composition even for a local edit**. Compare the whole-page before/after: scan path, adjacent sections, grouping of values that must be compared, whitespace and content density, alignment, visual weight, color-block rhythm, and page length. Do not pass an attractive new block if it makes the page fragmented or forces readers to hunt across distant regions. Do not equate dense with bad or spacious with good: judge by the task and device.
5. **Visual review loop:** when a render/browser is available, capture the original full page and first viewport at the primary desktop and mobile sizes. Inspect the actual pixels at normal zoom: locate the first visual anchor, trace the reading path, then identify pairs of facts that must be compared. Record where a title is separated from its evidence, where related values require avoidable scrolling/eye travel, and where color or whitespace falsely groups or separates content. Do not infer these from CSS alone.
6. Use a quick human-scan *simulation*: can a reader identify the primary question, compare related facts and locate the next action without hunting? Name the visible evidence and viewport. This is an agent self-review, **not human usability testing**. Without rendered screenshots, mark visual scanability **unverified** and provide only structural hypotheses.
7. Report each issue as **visible evidence → consequence for the task → concrete correction**, ordered by severity. Separate facts from preferences and avoid imposing a favorite style. Avoid made-up numeric thresholds for spacing or scan time.
8. If the user asks for a fix, require authorization before changing files or deploying. State the space trade-off (remove / merge / move / resize / add). Render the revised full page and first viewport at the same desktop/mobile sizes, compare before/after including neighboring sections, and record remaining issues. Do not declare a local fix successful from a component-only screenshot.

## Verification
Every issue cites a visible or inspectable basis; no accessibility or data-accuracy claim is marked verified without the appropriate evidence/test. Check the entire page at the intended device widths, not only a component crop. If rendered capture is impossible, report the limitation rather than claiming visual harmony. The review remains shorter than necessary to obscure the artifact itself.
