# Agent handoff — UIUX_improve

Read `docs/PROJECT_BRIEF.md`, `docs/ARCHITECTURE.md`, and `docs/DECISIONS.md` before making project decisions. For a specific task, load only the relevant `skills/*/SKILL.md`, then consult `core/QUALITY_BASELINE.md`. Never treat a previous chat as the source of truth.

## Boundaries
- This repository is a distinct Git repository nested under `n8n_project`. Confirm `git rev-parse --show-toplevel` resolves to `UIUX_project` before Git commands. Never modify the parent repository or its remote.
- Do not invent data or present hypotheses as facts. If the evidence is insufficient, identify the gap and stop rather than fabricating a chart or insight.
- Core quality requirements are maintained only in `core/QUALITY_BASELINE.md`; skills reference IDs rather than copying rules. Style, chart types, and layouts are not universal requirements.
- Before external writes, installs, commits, pushes, or deployment, check the user's authorization and scope. Local project edits are authorized for the initial scaffold; publishing is not yet authorized.
- Record confirmed product decisions in `docs/DECISIONS.md`, with date, rationale and alternatives. Do not mark proposals as approved.

## Routing
- Data adequacy, analysis, chart/table choice: `skills/data-viz-analysis/SKILL.md`
- Dashboard decision flow and information architecture: `skills/dashboard-architecture/SKILL.md`
- Substantively different UI/UX concepts and prototypes: `skills/uiux-exploration/SKILL.md`
- Audit an existing design or chart: `skills/design-review/SKILL.md`

If several skills apply, load each relevant skill; do not invent a mandatory full pipeline. Prompt improvement is a reusable template/reference concern until independent demand justifies a separate skill. Platform-specific adapters belong in `adapters/` and must not redefine the baseline.
