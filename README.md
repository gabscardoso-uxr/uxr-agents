# UXR Agents

A set of Claude Code skills for UX researchers. Each skill takes a specific research input and produces a structured, decision-ready output — without fabricating signals or skipping steps.

---

## Install

These skills run inside [Claude Code](https://claude.com/claude-code). You'll need it installed first.

**Option 1 — use the repo as your working directory (simplest):**

```bash
git clone https://github.com/gabscardoso-uxr/uxr-agents.git
cd uxr-agents
claude
```

The skills in `.claude/skills/` are available automatically when Claude Code runs from this directory.

**Option 2 — install into your user-level Claude config (skills available everywhere):**

```bash
git clone https://github.com/gabscardoso-uxr/uxr-agents.git
cp -r uxr-agents/.claude/skills/* ~/.claude/skills/
```

After either setup, `/scoper`, `/screener`, `/discussion-guide`, and `/synthesis` are available as slash commands in any Claude Code session.

To stay up to date, `git pull` in the cloned repo (Option 1) or re-copy the skills directory (Option 2).

---

## Example: running `/scoper`

You're a researcher whose PM just dropped this in Slack: *"Trial-to-paid conversion is down 12% this quarter. Can you figure out why?"*

In Claude Code:

```
/scoper trial-to-paid conversion is down 12% this quarter, PM wants to know why
```

**What the skill does, step by step:**

1. **Pre-flight gate.** Before generating anything, the skill checks the brief for a workable problem, infers the research stage (Discovery, in this case), and outputs a checklist asking you to confirm the stage and add any context (existing data, prior conversations, senior bets). It will not produce a scope until you confirm.

2. **Desk research.** Once you confirm, it runs 4–6 parallel web searches for industry signal on the problem space (in this case: SaaS trial conversion benchmarks, common churn causes at the trial-to-paid stage, recent vendor case studies). Findings get synthesized into the Research Plan section by theme — not by source.

3. **Chat output.** You see "The short version" (one strategic sentence + the recommended path) and the research questions.

4. **HTML deliverable.** The full scope is written to `scope.html` in your working directory — a one-pager with collapsible sections for the PM, Designer, Developers, and Research lead. Every section opens with the action that role needs to take. Open it in a browser to share.

5. **Refinement menu.** The skill lists the four sections you can iterate on in chat before sharing the HTML.

The skill won't fabricate signals. If the brief is missing pieces — no metric definition, no segment data, no prior conversations — it flags those gaps in the scope rather than inventing plausible content.

---

## Skills

### `/scoper` — Research Scoper
**Input:** A research brief (problem, goals, research questions)
**Output:** A scoped research plan — one document, four readers (Exec, PM, Designer, Developers)

What it does:
- Confirms the research stage (Discovery / Definition / Validation) before producing anything
- Flags when multiple RQs are at different stages and need to be separated
- Adapts the engineering section for hardware + software products
- Refuses to fabricate signals — names gaps explicitly

Use when: a team brings you a brief and needs a research plan before anyone starts recruiting or designing.

---

### `/discussion-guide` — Discussion Guide Generator
**Input:** A completed research scope (from `/scoper`) + session details (length, method, participant profile)
**Output:** A field-ready discussion guide with facilitator notes

What it does:
- Structures the guide around the primary research question, not the question list
- Adapts format to session type (generative interview / contextual inquiry / concept eval / usability)
- Writes behavioral, non-leading questions
- Includes a stimulus section for Validation-stage sessions
- Adds facilitator-only notes: hypotheses to listen for, time checks, segment flags

Use when: you have a scope and need to brief a facilitator or run sessions yourself.

---

### `/synthesis` — Research Synthesis
**Input:** Raw session notes, transcripts, or observation logs + the research questions the study was designed to answer
**Output:** Structured findings in the scoper format — findings, hypothesis review, segments, open questions, recommended next step

What it does:
- Flags data quality issues before synthesizing (low N, sparse notes, segment mismatch)
- Produces findings as active statements with named evidence, not summaries
- Calibrates confidence explicitly (High / Medium / Low)
- Reviews every hypothesis the team held going in — confirms, contradicts, or complicates
- Surfaces open questions and whether they block the current decision

Use when: sessions are complete and the team needs to move from data to direction.

---

### `/screener` — Participant Screener Generator
**Input:** Target participant profile + number of participants needed + session logistics
**Output:** A field-ready participant screener with recruiter quota instructions

What it does:
- Builds explicit criteria before writing any questions
- Writes questions that don't reveal the qualifying answer
- Uses behavioral questions over attitudinal ones
- Separates participant-facing copy from recruiter instructions
- Includes quota logic, screening ratio, and red flags for inattentive respondents

Use when: you have a research plan and need to brief a recruiting agency or post to a panel tool.

---

## Workflow

These skills are designed to chain:

```
Brief → /scoper → /screener      (recruit the right people)
                → /discussion-guide  (run the sessions)
                      ↓
               /synthesis          (turn data into direction)
```

Each skill checks its inputs before producing output. If something is missing, it asks — it does not fabricate.

---

## Design Principles

- **Stage-aware:** Every output is shaped by where the team is in the product development process.
- **No fabrication:** If signals are missing, skills name the gap and ask. They do not invent data to fill it.
- **Decision-connected:** Every finding, question, and recommendation must connect to a decision the team needs to make. Outputs that don't connect to a decision are cut.
- **Four readers:** Research outputs serve executives, PMs, designers, and engineers differently. Each skill produces output structured for all four.
