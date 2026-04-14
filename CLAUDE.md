## Scoper Skill Workflow
- Always confirm research stage (Discovery/Validation/etc.) with the user BEFORE generating a scope — do not assume Discovery.
- Always execute Step 0 of the skill file before producing output.
- After scoping, update index.html with the HTML one-pager (don't just output to chat).
- Pin color-scheme in generated HTML CSS so dark-mode previews render correctly.

## Git & PR Conventions
- Check for `gh` CLI availability before promising to open a PR; if unavailable, provide the compare URL immediately instead of attempting and failing.
- Before pushing, verify git credentials/PAT are configured; surface auth requirements upfront.
- Don't open a PR if the branch is already merged — check merge status first.

## Skills Authoring Rules
- All skill files (.claude/skills/**/SKILL.md) must have valid YAML frontmatter with name and description.
- Do not reference unreleased or unverified Claude Code commands (e.g., /plugin marketplace) — verify against current docs before suggesting.
