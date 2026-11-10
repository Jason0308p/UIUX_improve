---
name: data-viz-analysis
description: Assess data adequacy and choose honest visual representations.
version: 0.1.0
---
# Data visualization analysis

## When to use
Choose this skill for a data-to-chart request, chart choice, interpretation of metrics, or an unsupported analytical claim. Do not use it for an interface-only visual redesign with no data question.

## Procedure
1. State the audience's question or decision, available fields, time range, units and comparison basis. Ask only for missing information that changes the conclusion.
2. Assess support: **supported / partially supported / unsupported**. If unsupported, specify the missing data and stop before claiming an insight. Existing chart requests are suggestions, not proof of suitability.
3. Compare chart, table, single value and prose against the analytical task. Select the simplest sufficient form; if choosing a chart, explain the encoding and baseline.
4. Separate observed facts from interpretation and hypotheses. Mark synthetic inputs as demonstration data.
5. Check relevant IDs in `../../core/QUALITY_BASELINE.md` (especially Q1–Q4); report any unresolved risk.

## Verification
The stated claim must be reproducible from the provided inputs; the selected form must answer the stated question without hiding essential context. If no data is provided, deliver a data-gap assessment, not a fabricated chart.
