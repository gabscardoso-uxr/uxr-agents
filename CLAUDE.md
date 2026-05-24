## Scoper Skill Workflow
- Always confirm research stage (Discovery/Validation/etc.) with the user BEFORE generating a scope — do not assume Discovery.
- Always execute Step 0 of the skill file before producing output.
- For this repo (uxr-agents): keep both `intake.html` and `scope.html` in `preview/` so the example output stays in the demo location. Skill's path-resolution cascade is otherwise: explicit `path=` argument → CLAUDE.md override (this rule) → git repo root `<root>/scopes/<study-slug>/` → fallback `~/uxr/scopes/<study-slug>/`.
- Step 0 writes `intake.html` (visual pre-flight card: persistent "AI's guess" pill with confidence label on the inferred stage, clickable stage buttons where green = the user's confirmed decision, "Copy all my answers" button compiling stage + checklist + context-probe textareas into one paste-back) and echoes the pre-flight block in chat. Wait for the user to confirm stage before proceeding.
- After stage confirmation and desk research, write the full scope to `scope.html`.
- Pin `color-scheme: light` in generated HTML CSS so dark-mode previews render correctly.
- `scope.html` uses 5 color-coded role sections (PM `#FF6636` / Designer `#D85C4F` / Content `#B8956A` / Developer `#3D3D3D` / Research `#6B3D2E`) with checkable actions + status pills (localStorage-persisted) and a Team Alignment section for the Figma session (goals, success metrics, **guardrails as constraints — cost/system-limits/evaluation/principles/frameworks/data — not "won't do" promises**, risks).
- Voice rule: never write "this, not that" framings (negating one claim to assert another). Make the positive claim directly.

## Git & PR Conventions
- Check for `gh` CLI availability before promising to open a PR; if unavailable, provide the compare URL immediately instead of attempting and failing.
- Before pushing, verify git credentials/PAT are configured; surface auth requirements upfront.
- Don't open a PR if the branch is already merged — check merge status first.

## Skills Authoring Rules
- All skill files (.claude/skills/**/SKILL.md) must have valid YAML frontmatter with name and description.
- Do not reference unreleased or unverified Claude Code commands (e.g., /plugin marketplace) — verify against current docs before suggesting.
