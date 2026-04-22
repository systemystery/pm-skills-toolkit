---
name: task-prioritizer
description: Use when the user has too many tasks, feels overwhelmed, needs to prioritize work, or asks what to focus on. Also triggers on keywords like "100 things", "overwhelmed", "what should I work on", "prioritize", "4A", "amplify", "automate", "abandon".
tools: []
---

# Task Prioritizer Skill (4A Framework)

Extends Shreyas Doshi's LNO Framework for the AI era.

**The core question LNO never asked: "Should AI do this instead of me?"**

## Trigger
When the user:
- Has too many tasks and doesn't know what to focus on
- Asks "what should I work on?"
- Says they're overwhelmed or have "100 things on their plate"
- Asks to prioritize a task list
- Mentions prioritization, LNO, 4A, leverage

## The 4A Framework

Every task gets TWO questions:
1. **Is this a brainer or a no-brainer?** (Does it need my judgment, context, relationships — or is it routine?)
2. **What's the impact?** (If I do this excellently vs. adequately, does the outcome change 10x?)

That gives you four categories:

| | 🧠 BRAINER (needs your judgment) | 🤖 NO-BRAINER (routine/mechanical) |
|---|---|---|
| **HIGH IMPACT** | 🔴 **AMPLIFY** — You drive, AI thinks with you | ⚡ **ACCELERATE** — AI drafts, you review closely |
| **LOW IMPACT** | ⚡ **ACCELERATE** — AI drafts, you glance | 🤖 **AUTOMATE** — AI handles entirely |
| **NO IMPACT** | ❌ **ABANDON** — Stop doing it | ❌ **ABANDON** — Definitely stop doing it |

### 🔴 AMPLIFY (Brainer + High Impact)
**What**: Work where YOUR judgment + AI's capability = 10x results.
**How**: Use AI as a thinking partner. Share full context. Ask it to challenge your assumptions. Iterate together.
**Your role**: You drive. AI co-pilots.
**Time**: Give these your best energy blocks. Perfectionism welcome.

Examples:
- Product strategy → AI researches, you decide
- Critical stakeholder negotiation → AI preps talking points, you read the room
- Complex PRD → AI drafts structure, you bring domain judgment
- Prioritization decisions → AI provides data, you make the call

**Prompt pattern**: "Here's my full context: [everything]. Help me think through this. Challenge my assumptions. What am I missing?"

### ⚡ ACCELERATE (Medium judgment needed OR high impact routine)
**What**: Work that needs to get done well, but AI can do 80% of the lifting.
**How**: AI creates the first draft. You review, adjust, ship.
**Your role**: Editor, not author. Quality check, not creation.
**Time**: Time-box aggressively. 30 min max per task.

Examples:
- Sprint planning → AI generates from backlog, you adjust
- Weekly status update → AI drafts from project data, you add context
- OKR first drafts → AI proposes from strategy, you refine
- Meeting prep → AI pulls stakeholder context, you decide what to raise

**Prompt pattern**: "Draft this for me based on [context]. I'll review and adjust."

### 🤖 AUTOMATE (No-brainer + Low impact)
**What**: Routine tasks that AI can handle entirely. No judgment needed.
**How**: Set it up once. Let AI run it. Don't look at the output.
**Your role**: None. Seriously — stop touching these.
**Time**: Zero ongoing time. One-time setup only.

Examples:
- Meeting note summaries → Granola/Otter auto-summarizes
- Scheduling emails → AI sends based on calendar
- Wiki/doc updates → AI updates from merged PRs
- Routine status reports → AI pulls from tools and posts to Slack
- Formatting slides → AI formats, you never look

**Prompt pattern**: "Do this automatically every [time]. Don't ask me. Just do it."

### ❌ ABANDON (No impact — regardless of brainer status)
**What**: Work that shouldn't exist. Not "do a bad job" — STOP DOING IT.
**How**: Delete it. Decline the meeting. Remove yourself from the thread.
**Your role**: Courageous eliminator.
**Time**: Negative time — every abandoned task GIVES you time back.

Examples:
- The recurring meeting nobody gets value from → Cancel it
- The report nobody reads → Stop writing it
- The approval chain that exists "because it always has" → Challenge it
- The Slack thread where your input isn't needed → Leave it
- The dashboard nobody checks → Let it rot

**The test**: "If I stopped doing this, would anyone notice within 2 weeks?" If no → ABANDON.

## Instructions

### Phase 1: Gather the Task Dump
Ask the user to list EVERYTHING on their plate:

```
List every task, meeting, project, and to-do currently on your plate.
Don't filter. Don't organize. Just dump it all.
Include things you think are "small" — those are often the hidden time drains.
```

If incomplete, probe:
- "What meetings require prep this week?"
- "What do you owe anyone? (follow-ups, reviews, docs)"
- "What's been on your list for 2+ weeks that you keep avoiding?"

### Phase 2: Classify Each Task

For each task, ask two questions:

**Question 1 — Brainer or No-Brainer?**
- Does this need my specific judgment, relationships, or domain context?
- Would the output be meaningfully worse if someone else (or AI) did it?
- If YES → Brainer. If NO → No-brainer.

**Question 2 — What's the impact multiplier?**
- If I do this excellently vs. adequately, does the outcome change significantly?
- Does this affect our users, revenue, strategy, or team direction?
- HIGH impact → the quality of my effort matters 10x
- LOW impact → good enough is truly good enough
- NO impact → why are we doing this?

### Phase 3: Present the 4A Matrix

```markdown
# Your 4A Analysis — [Date]

## 🔴 AMPLIFY (Brainer + High Impact) — You + AI as thinking partner
These tasks need YOUR judgment, amplified by AI.

| # | Task | Why It's a Brainer | AI's Role | Time Block |
|---|------|-------------------|-----------|------------|
| 1 | [Task] | [What judgment is needed] | [How AI helps] | [Best energy block] |

**⏰ Total: [X] hours · 🎯 Rule: 60% of deep work time here**

---

## ⚡ ACCELERATE (AI drafts, you review)
AI does the heavy lifting. You steer.

| # | Task | AI Does | You Do | Time Box |
|---|------|---------|--------|----------|
| 1 | [Task] | [AI's 80%] | [Your 20% review] | Max [X] min |

**⏰ Total: [X] hours · 🎯 Rule: Time-box. When timer rings, ship it.**

---

## 🤖 AUTOMATE (AI handles entirely)
Set up once. Never touch again.

| # | Task | Automation | Setup Time | Ongoing Time |
|---|------|-----------|------------|-------------|
| 1 | [Task] | [How to automate] | [One-time] | Zero |

**⏰ Ongoing time: ZERO · 🎯 Rule: If you're still manually doing these, you're wasting leverage.**

---

## ❌ ABANDON (Stop doing these)
Tasks that shouldn't exist. Kill them.

| # | Task | Why It's Safe to Kill | Who Notices? | Action |
|---|------|----------------------|-------------|--------|
| 1 | [Task] | [Reason] | [Nobody / Maybe X] | [Cancel / Decline / Unsubscribe] |

**⏰ Time recovered: [X] hours/week · 🎯 Rule: Every abandoned task gives you time for an AMPLIFY task.**

---

## 📊 Your Time Allocation

| Category | Tasks | Hours/Week | Current % | Ideal % |
|----------|-------|-----------|-----------|---------|
| 🔴 Amplify | [N] | [X] | [Y]% | 50-60% |
| ⚡ Accelerate | [N] | [X] | [Y]% | 20-30% |
| 🤖 Automate | [N] | [X] | [Y]% | <5% (setup only) |
| ❌ Abandon | [N] | [X] | [Y]% | 0% (eliminated) |

## 💡 The Opportunity Cost Question
> What AMPLIFY task am I NOT doing because I'm manually doing [biggest Automate/Abandon task]?
```

### Phase 4: Challenge the User
Push back if:
- Too many tasks in AMPLIFY (most PMs overcategorize — if >30% of tasks are "brainer + high impact," they're wrong)
- Nothing in ABANDON (every PM has tasks that shouldn't exist — they're just afraid to kill them)
- Automate tasks they're still doing manually ("Why are you still writing meeting summaries by hand?")

### Phase 5: Weekly Audit Prompt
```
Look at my calendar and task list for this week.
Classify every item using the 4A Framework:
🔴 Amplify — Am I using AI as a thinking partner on these?
⚡ Accelerate — Is AI drafting these for me?
🤖 Automate — Why am I still doing these manually?
❌ Abandon — What can I stop doing entirely?

Show me my time allocation vs. ideal (60/25/5/0).
```

## Self-Check
Before presenting:
- [ ] Every task classified into exactly one of the 4 A's
- [ ] AMPLIFY tasks are limited (max 20-30% of total tasks)
- [ ] User was challenged if nothing is in ABANDON
- [ ] AUTOMATE tasks have specific automation strategies, not just "automate this"
- [ ] Each AMPLIFY task specifies HOW AI helps (not just "use AI")
- [ ] Each ACCELERATE task has a time box
- [ ] Time allocation table shows current vs. ideal split
- [ ] The opportunity cost question is included
- [ ] At least one ABANDON recommendation (every PM has something to kill)

## Output Format
Structured markdown with the 4A matrix, emoji-coded categories, time allocation table, and the opportunity cost question at the end.

## Credits
The 4A Framework extends Shreyas Doshi's LNO Framework for the AI era. LNO asks "how much effort?" The 4A Framework asks "who should do the effort — you, AI, or nobody?"
