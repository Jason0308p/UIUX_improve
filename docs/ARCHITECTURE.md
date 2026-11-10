# Architecture

## Source of truth and loading
`AGENTS.md` is the **project-local** handoff, not Hermes global configuration. `README.md` serves humans. `docs/PROJECT_BRIEF.md` owns product intent; `docs/DECISIONS.md` separates approved decisions from proposals. `core/QUALITY_BASELINE.md` owns shared rules. Each `skills/<name>/SKILL.md` owns only its task-specific process. Never duplicate baseline prose across skills; reference its IDs.

```
UIUX_project/
├── AGENTS.md                  project-only cross-agent handoff
├── README.md                  human entry
├── docs/                      brief, architecture, decision record
├── core/QUALITY_BASELINE.md   single source for common quality boundaries
├── skills/                    four independently usable skills
│   ├── data-viz-analysis/SKILL.md
│   ├── dashboard-architecture/SKILL.md
│   ├── uiux-exploration/SKILL.md
│   └── design-review/SKILL.md
├── prompts/                   future copy/paste task prompts; not a skill router
├── profiles/                  future optional preferences, not overrides of evidence rules
├── adapters/                  future platform installation instructions only
└── evals/cases/               future reproducible input/expected-behavior cases
```

The last four directories are reserved for later phases; empty directories do not become Git-tracked content. Do not introduce a hub skill that merely redirects to the four real skills.

## Operating flow
Select only needed skills → state decision and known evidence → identify missing inputs → choose representation and structure → produce only authorized output → review relevant quality rules. A narrow chart-choice task need not run a dashboard/UI pipeline. If data cannot support the requested conclusion, report the gap before producing a misleading artifact.

## Cross-agent strategy
Lowest common denominator is plain Markdown with concise frontmatter. Claude/Hermes may discover individual skill files via their own mechanisms; Codex/OpenCode may load them via project instructions; chat-only models may receive a pasted skill plus the baseline. Platform adapters will document tested install paths and fallback behavior when added; do not claim validated compatibility before testing on each platform. A model switch is handled by reading repo files, not by relying on chat memory.

## Conflict order
Evidence and shared baseline > explicit task permissions and constraints > project/user preferences > skill defaults. Preferences can choose visual forms but cannot authorize unsupported facts. No file in this repo grants permission to publish, push, or deploy on its own.

## Next work, not yet implemented
Prompt templates (minimal/full and task-specific), optional profile schema, reproducible evaluation cases and before/after examples, licensing and contribution policy, tested platform adapters, and release process. Confirm each tranche before publishing.
