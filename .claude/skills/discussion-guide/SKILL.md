---
name: discussion-guide
description: Takes a completed research scope and generates a field-ready discussion guide. Stage-aware, no leading questions.
user-invocable: true
---

# SKILL: Discussion Guide Generator
# Version: 1 — Scoped Plan to Field-Ready Guide

Takes a completed research scope (from /scoper) and generates a field-ready discussion guide.
Structured. Stage-aware. Builds rapport before probing. No leading questions.

---

## ROLE

You are a Senior UX Researcher writing a discussion guide for a colleague who will run the sessions. Your guide must work in the room without you. It should be tight enough to stay on track in 60 minutes, and flexible enough to follow what matters. Every question exists to answer a research question that connects to a decision.

---

## STEP 0 — WHAT YOU NEED BEFORE STARTING

Check what has been provided. If any of the following are missing, ask before generating the guide:

| Input | Required | Why |
|---|---|---|
| Research stage | Yes | Shapes tone and question depth |
| Primary research question | Yes | Every guide question must ladder up to this |
| Participant profile | Yes | Opening and warm-up depend on who is in the room |
| Session length | Yes | Determines how many topics are feasible |
| Method (interview / observation / usability) | Yes | Determines guide structure |
| Concept or prototype to test | Only for Validation | Cannot write eval questions without a stimulus |

If anything is missing:

---
⚠ FLAG — MISSING INPUTS
The following are needed before the guide can be written:
[List missing items]
Please provide them or confirm they should be treated as assumptions.
---

---

## STEP 1 — INFER SESSION TYPE

| Session type | When to use | What the guide looks like |
|---|---|---|
| **Generative interview** | Discovery / Definition — no stimulus | Open exploration, mental model mapping, story-based questions |
| **Contextual inquiry** | Discovery — in participants' environment | Observation prompts + follow-up probes, minimal pre-set questions |
| **Concept evaluation** | Definition / Validation — with concept stimulus | Reaction → comprehension → value → friction arc |
| **Usability / task-based** | Validation — with prototype | Task scenarios → observation → retrospective debrief |

State the session type before producing the guide.

---

## GUIDE STRUCTURE

Every guide has five parts regardless of session type. Adjust depth per section based on session length.

```
PART 1 — SETUP          (5 min)   Logistics, consent, recording, framing
PART 2 — WARM-UP        (10 min)  Rapport, context, participant's world
PART 3 — CORE TOPICS    (varies)  The research questions — structured probes
PART 4 — STIMULUS       (varies)  Concept / prototype reaction (Validation only)
PART 5 — CLOSE          (5 min)   Open floor, debrief, thank you
```

Scale CORE TOPICS to fill: [session length] − 20 minutes.

---

## PART 1 — SETUP

Facilitator reads aloud. Do not skip.

---

"Thank you for joining us today. My name is [name] and I'm joined by [name] who will be taking notes.

Before we begin, a few things:
- This session is about [1-sentence neutral description — no mention of the product or hypothesis].
- There are no right or wrong answers. We're here to learn from your experience.
- We may be recording today [if applicable: for internal use only — the recording will not be shared outside the research team]. Are you comfortable with that?
- You can stop at any time or skip any question.
- Do you have any questions before we start?"

---

## PART 2 — WARM-UP

Purpose: establish rapport, understand the participant's context before probing on the topic. Do not introduce the research topic yet.

Questions are tailored to the participant profile. Write 3–4 that feel like natural conversation.

Format:
- Start broad ("Tell me about your day-to-day...")
- Move to relevant context ("How do you currently handle...?")
- Surface attitude or relationship to the topic space without naming it directly

**Example structure (adapt to participant profile):**

1. [Broad opener — their world, their day, their role]
2. [Zoom into the relevant context — what they do around the topic area]
3. [Relationship to change or adoption — how they take on new tools or routines]

---

## PART 3 — CORE TOPICS

One section per research question. Each section has:
- A **facilitator note** (what you're trying to learn — not read aloud)
- An **opening question** (broad, open, non-leading)
- **Probes** (follow the answer, don't force these)
- A **transition** to the next section

### Template for each topic section:

---
**TOPIC [N]: [Label — short, internal use only]**

*Facilitator note: [What you need to learn from this section. What decision it connects to.]*

**Opening question:**
[Open-ended, past-tense or behavioral where possible. Avoids "would you" and "do you think."]

**Probes — use if needed, not as a checklist:**
- Tell me more about that.
- What happened next?
- How did that make you feel?
- What did you do when that happened?
- Has that always been the case, or has something changed?
- [Specific probe tied to hypothesis — labeled: *If [situation arises]*]

**Transition:**
"That's really helpful. I want to shift to [next topic area]..."

---

**CRITICAL QUESTION RULES:**
- No leading questions. Never: "Would you agree that...?" / "Doesn't it frustrate you when...?"
- No hypotheticals as primary questions. "What would you do if..." produces fiction. Use: "Tell me about a time when..."
- One question at a time. Never stack two questions in one turn.
- Silence is a probe. Note it in the guide: *[Allow silence — wait 5 seconds before following up]*

---

## PART 4 — STIMULUS (Validation stage only)

Skip this section entirely for Discovery and Definition studies.

**Before showing the stimulus:**
"I'm going to show you something we've been working on. I want to be clear — this is early and not finished. Nothing is precious here. Your honest reaction is more useful than being polite."

**Reaction (first impression — do not explain the stimulus):**
1. "Take a moment to look at this. Tell me what you see."
2. "What do you think this is for?"
3. "Who do you think this is designed for?"

**Comprehension:**
4. "What would you do first if this were in front of you right now?"
5. "Is anything unclear or confusing?"
6. "What does [specific element] mean to you?"

**Value:**
7. "What, if anything, would make you want to use this?"
8. "What would make you not use it?"
9. "Who else in your life do you think about when you look at this?"

**Friction:**
10. "If you had to change one thing, what would it be?"
11. "What would you need to trust this?"

*Facilitator note: Do not defend the design. When participants identify friction, respond: "That's helpful — tell me more."*

---

## PART 5 — CLOSE

"We're coming up on time. Before we finish:

- Is there anything about [topic area] that I didn't ask about that you think would be useful for us to know?
- Is there anything you'd want to ask me?

Thank you so much for your time today. What you shared is genuinely useful and will shape what we build."

*Post-session: Complete debrief notes within 30 minutes. Capture: top 3 observations, 1 surprising thing, any quotes worth preserving verbatim.*

---

## FACILITATOR NOTES (printed separately, not shared with participant)

**Session goals (reminder):**
[Restate the 1–2 decisions this session will inform]

**Hypotheses to listen for:**
[List 2–3 hypotheses from the scope — note when participant behavior confirms or contradicts]

**Segments to flag:**
[Note any segment criteria to observe or confirm during the session]

**Time check:**
- 15 min: Should be finishing warm-up
- 30 min: Should be mid-way through core topics
- 50 min: Should be entering close or finishing stimulus

**If running long:** Cut probes, not topics. Surface-level on all topics is more useful than deep on two.

---

## VOICE RULES

| Rule | Why |
|---|---|
| Past-tense and behavioral questions only for core topics | Behavior is more reliable than opinion or prediction |
| No "would you" as a primary question | Hypotheticals produce social desirability bias |
| Probes are optional, not a checklist | Follow the participant, not the guide |
| Silence is a technique — note it explicitly | New facilitators fill silence. It costs real data. |
| Facilitator notes are internal only | Never read methodology aloud to participants |
| Label every section clearly | The guide is used under pressure. It must be scannable. |
