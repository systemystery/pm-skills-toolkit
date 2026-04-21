---
name: task-prioritizer
description: Use when the user has too many tasks, feels overwhelmed, needs to prioritize work, or asks what to focus on. Also triggers on keywords like "100 things", "overwhelmed", "what should I work on", "prioritize", "LNO", "leverage".
tools: []
---

# Task Prioritizer Skill (LNO Framework)

Based on Shreyas Doshi's LNO Framework + Radical Delegation Matrix.

## Trigger
When the user:
- Has too many tasks and doesn't know what to focus on
- Asks "what should I work on?"
- Says they're overwhelmed or have "100 things on their plate"
- Asks to prioritize a task list
- Mentions LNO, leverage, or Shreyas Doshi

## Instructions

### Phase 1: Gather the Task Dump
Ask the user to list EVERYTHING on their plate. Use the ask-user-questions tool if available. Prompt:

```
List every task, meeting, project, and to-do currently on your plate.
Don't filter. Don't organize. Just dump it all.
Include things you think are "small" — those are often the hidden time drains.
```

If the user provides a partial list, ask:
- "What meetings do you have this week that require prep?"
- "What do you owe anyone? (follow-ups, reviews, documents)"
- "What's been sitting on your list for 2+ weeks that you keep avoiding?"

### Phase 2: Classify Each Task Using LNO

For each task, ask two questions:
1. **What's the return multiplier?** If I spend X hours on this, do I get 10X value (Leverage), 1X value (Neutral), or <1X value (Overhead)?
2. **What happens if I do a mediocre job?** If the answer is "nothing much" — it's probably Neutral or Overhead.

#### LNO Classification Guide

| Category | Return | Your Best Effort Matters? | Example |
|----------|--------|--------------------------|---------|
| **🔴 Leverage (L)** | 10x-100x | YES — quality here = disproportionate impact | Product strategy doc, key stakeholder alignment, critical PRD, hiring decision, major customer escalation |
| **🟡 Neutral (N)** | ~1x | Somewhat — good is fine, great doesn't add much | Sprint planning, routine 1:1 prep, standard status updates, most meetings, regular bug triage |
| **⚪ Overhead (O)** | <1x | NO — just get it done | Expense reports, formatting slides, routing approvals, updating wikis, most email replies, calendar management |

#### The Key Insight
> **Most PMs treat 80% of their tasks as Leverage. In reality, only 10-20% are Leverage. The rest are Neutral or Overhead eating your best hours.**

### Phase 3: Build the LNO Matrix

Present the classification to the user:

```markdown
# Your LNO Analysis — [Date]

## 🔴 LEVERAGE (Do these with your best energy)
These tasks have 10x-100x return. Perfectionism is ENCOURAGED here.

| # | Task | Why It's Leverage | Recommended Time | When |
|---|------|------------------|-----------------|------|
| 1 | [Task] | [Impact explanation] | [Hours] | [Best energy block] |
| 2 | [Task] | [Impact explanation] | [Hours] | [Best energy block] |

**⏰ Total Leverage time: [X] hours this week**
**🎯 Rule: Spend 60-70% of your deep work time here**

---

## 🟡 NEUTRAL (Do these well enough, then move on)
These tasks have ~1x return. Good is fine. Great adds nothing.

| # | Task | Time Box | Shortcuts |
|---|------|----------|-----------|
| 1 | [Task] | [Max X min] | [How to do this faster] |
| 2 | [Task] | [Max X min] | [How to do this faster] |

**⏰ Total Neutral time: [X] hours this week**
**🎯 Rule: Time-box these. Set a timer. When it rings, ship it.**

---

## ⚪ OVERHEAD (Minimize, delegate, or automate)
These tasks have <1x return. Actively try to spend LESS time here.

| # | Task | Can You... | Action |
|---|------|-----------|--------|
| 1 | [Task] | Delegate? Automate? Skip? | [Specific action] |
| 2 | [Task] | Delegate? Automate? Skip? | [Specific action] |

**⏰ Total Overhead time: [X] hours this week**
**🎯 Rule: If it takes <5 min, batch it. If someone else can do it, delegate.**

---

## 📊 Your Time Allocation

| Category | Tasks | Hours | % of Week | Ideal % |
|----------|-------|-------|-----------|---------|
| 🔴 Leverage | [N] | [X] | [Y]% | 60-70% |
| 🟡 Neutral | [N] | [X] | [Y]% | 20-30% |
| ⚪ Overhead | [N] | [X] | [Y]% | <10% |
```

### Phase 4: Apply the Delegation Matrix
For Leverage and Neutral tasks, check replaceability:

| | Only You Can Do It | Others Could Do It |
|---|---|---|
| **🔴 Leverage** | ✅ **YOUR #1 PRIORITY** — block 2-4 hour chunks | 🤝 Delegate with close oversight + clear brief |
| **🟡 Neutral** | ⚡ Do it, but time-box aggressively | 🤝 Delegate fully — check output once |
| **⚪ Overhead** | 🤖 Automate or batch into one session | 🗑️ Delegate and forget, or eliminate entirely |

### Phase 5: Create the Action Plan

```markdown
## This Week's Focus Plan

### Monday-Tuesday: Leverage Block
- [ ] [Leverage Task 1] — 2 hours, deep work, no meetings
- [ ] [Leverage Task 2] — 1.5 hours, deep work

### Overhead Batch (30 min, Wednesday morning)
- [ ] [Overhead 1] — 5 min
- [ ] [Overhead 2] — 10 min
- [ ] [Overhead 3] — 5 min

### Delegated This Week
| Task | Delegated To | Due | Check-in |
|------|-------------|-----|----------|
| [Task] | @name | [Date] | [When to review] |

### Eliminated This Week
| Task | Why It's Safe to Skip | Risk If We Don't |
|------|----------------------|-----------------|
| [Task] | [Reason] | [Low/None] |

### The Uncomfortable Question
> **What am I NOT doing because I'm spending time on [biggest overhead task]?**
> The opportunity cost of [overhead task] is [leverage task you're not doing].
```

### Phase 6: Weekly Audit Prompt
Suggest the user runs this every Monday:

```
Look at my calendar and task list for this week.
Classify every item as Leverage, Neutral, or Overhead.
Am I spending 60%+ of my deep work time on Leverage tasks?
What can I delegate, automate, or eliminate?
```

## Self-Check
Before presenting:
- [ ] Every task is classified as L, N, or O with clear reasoning
- [ ] Leverage tasks are limited (10-20% of total tasks, not 50%+)
- [ ] User was challenged if they classified too many things as Leverage
- [ ] Overhead tasks have specific "minimize" actions (delegate/automate/eliminate)
- [ ] Time allocation adds up and shows current vs. ideal split
- [ ] The "uncomfortable question" about opportunity cost is included
- [ ] Action plan has specific time blocks, not just a priority list
- [ ] Delegation matrix is applied (who else can do this?)

## Output Format
Structured markdown with the LNO matrix, emoji-coded categories (🔴🟡⚪), time allocation table, delegation recommendations, and a concrete weekly action plan. Always end with the opportunity cost question — it's the most powerful reframe.

## Why This Skill Matters
> "The biggest problem isn't that PMs can't prioritize. It's that they treat everything as a Leverage task. When everything is a priority, nothing is." — Inspired by Shreyas Doshi
