# Shared quality baseline (draft)

These are proposed cross-skill checks, not a claim that every scenario requires a full audit. A rule's conditions and exceptions matter. Change this file—not four copies—when the user approves refinements.

- **Q1 Evidence:** Never invent observed values, sources, or causal claims. Clearly label synthetic demo data; do not present it as real evidence.
- **Q2 Representation:** Do not use scales, selective ranges, ordering, visual area, or dual axes to imply a conclusion the data cannot support. A narrowed axis is not universally forbidden; justify and label it where used.
- **Q3 Context:** Where interpretation depends on it, expose period, metric definition, units, denominator, comparison basis and freshness. Report what's unavailable instead of guessing.
- **Q4 Epistemic status:** Distinguish observations from interpretation, hypotheses, unknowns and proposed actions when providing analysis.
- **Q5 Accessibility:** Critical differences must not rely on color alone. Check contrast and keyboard/screen-reader behavior when an interactive artifact exists; do not claim compliance without testing.
- **Q6 States:** For reusable data interfaces, account for loading, empty, partial, error and stale states. A one-off static chart need not implement an application state machine.
- **Q7 Context of use:** For interface tasks, identify the primary device and confirm that the central user task is feasible there. Do not force a desktop layout onto mobile.
- **Q8 Authority:** Respect explicit approval gates for writes, installs, commits, pushes and deployment. Reading, planning and writing a draft are distinct permissions.

Visual style, color palette, card layout, chart library, density and technology are preferences, not universal baseline rules. Cases where a check does not apply should be marked N/A rather than failed. Automated validation of all eight checks has **not** been implemented.
