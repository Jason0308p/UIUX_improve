---
name: dashboard-architecture
description: Structure dashboards around audience decisions and evidence.
version: 0.1.0
---
# Dashboard architecture

## When to use
Use for planning or restructuring a dashboard/report, prioritizing many metrics, or designing navigation between summary and detail. Do not use for a single chart when no broader information flow is required.

## Procedure
1. Define decision, audience, frequency, device and the next action the interface should enable.
2. Inventory available metrics and their limitations. If evidence is insufficient, note the gap; consult `../data-viz-analysis/SKILL.md` for a dedicated data assessment only when needed.
3. Draft an information hierarchy: primary question, summary, evidence, drilldown and action. Not all dashboards need cards, a KPI row or a top-to-bottom layout.
4. Set a **scan path and space budget** for the primary device: which facts must be seen together, which can be grouped, and which can move to a detail view? Avoid both excessive spreading (related data too far apart) and indiscriminate compression. A fixed viewport height is a task constraint only when the user requires it, not a universal rule.
5. For a local change, sketch the whole page before editing. State what will be removed, merged, moved or resized to make space; adding a block without accounting for displaced content is not a complete design. Explain what remains stable and why. If the user's workflow expects an approval gate, show this impact map before changing code.
6. Sketch the mobile task independently rather than merely shrinking desktop. Account for relevant data states and review Q1–Q8 in `../../core/QUALITY_BASELINE.md` as applicable.

## Verification
At normal viewing size on the primary device, a target user should locate the main question, compare related values without unnecessary back-and-forth scanning, and find the evidence and next step. Inspect the entire page before and after a local edit: hierarchy, alignment, grouping, density, section transitions and total length. Check the changed region plus its neighbors, not just the new component. Distinguish unverified assumptions from tested behavior.
