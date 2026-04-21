---
name: pm-daily-system
description: Use at the start of every work day, or when the user says they're overwhelmed, lost, stuck, or don't know what to work on. This is the master workflow that chains all other skills.
tools: []
---

# PM Daily System — The Master Workflow

## Why This Exists
You have 100 tasks. You have 10 skills. You have AI.
But without a **system**, you're still reacting to whatever screams loudest.

This workflow is the operating system. Run it once at the start of your day.
Everything else flows from it.

## Trigger
- Start of work day
- "I'm overwhelmed"
- "What should I work on?"
- "I have too many things"
- Monday morning (automatic weekly version)

## The Daily Loop (15 minutes)

### Step 1: Brain Dump (3 min)
```
List everything on my plate right now. Check:
- My calendar for today and tomorrow
- My task board / Linear / Jira
- My Slack unreads and DMs
- Any pending follow-ups I owe people
- Things I keep pushing to "later"

Give me the complete, unfiltered list.
```

### Step 2: LNO Classify (5 min)
```
Using /skills/task-prioritizer.md, classify every task:
🔴 Leverage — 10x return, my best work matters
🟡 Neutral — 1x return, good enough is fine
⚪ Overhead — <1x return, minimize or delegate

Show me the breakdown and my time allocation.
Challenge me if I'm marking too many things as Leverage.
```

### Step 3: Today's Focus (3 min)
```
Based on the LNO classification:
1. Pick my ONE Leverage task for today (deep work, 2+ hour block)
2. List my Neutral tasks (time-boxed, max 30 min each)
3. Batch my Overhead tasks (one 30-min block)
4. What should I SKIP or DELEGATE today?

Block my calendar accordingly.
```

### Step 4: Meeting Prep (2 min)
```
For each meeting today:
- Is this meeting Leverage, Neutral, or Overhead?
- If Leverage: What do I need to prepare? (check /knowledge/people/)
- If Neutral: What's my one-sentence goal for this meeting?
- If Overhead: Can I skip, shorten, or send a delegate?
```

### Step 5: End-of-Day Checkpoint (2 min, run at EOD)
```
What did I accomplish today?
- Did I complete my Leverage task? Y/N
- If no, what blocked me? (Add to CLAUDE.md as a rule)
- What moves to tomorrow?
- Any new tasks from today's meetings? (Classify immediately)
```

## The Weekly Version (Monday, 30 min)

Run Steps 1-4 above, PLUS:

### Step 6: Weekly LNO Audit
```
Look at everything I spent time on last week.
Using /skills/task-prioritizer.md, calculate:
- What % of my time was on Leverage tasks?
- What % was on Overhead I could have eliminated?
- What Leverage task did I NOT do because of Overhead?

Show me the time allocation vs. ideal (60/30/10).
```

### Step 7: Skill Chain
Based on what's on your plate this week, the system auto-suggests which skills to run:

| If Your Week Includes... | Run This Skill |
|--------------------------|---------------|
| Writing a PRD | `/skills/prd-writer.md` |
| Preparing OKRs | `/skills/okr-generator.md` |
| Customer calls to synthesize | `/skills/user-interview-synthesizer.md` |
| Feature launching | `/skills/launch-checklist.md` |
| Stakeholder update needed | `/skills/stakeholder-brief.md` |
| Sprint planning ceremony | `/skills/sprint-planning.md` |
| Experiment to design | `/skills/ab-test-designer.md` |
| Quarterly planning | Chain: `/workflows/quarterly-planning.md` |
| Competitor questions | `/skills/competitive-analysis.md` |
| New metrics needed | `/skills/metrics-dashboard.md` |
| Roadmap review | `/skills/roadmap-builder.md` |

### Step 8: Weekly Report Auto-Draft
```
Using /skills/stakeholder-brief.md, draft my weekly update.
Tailor it for [my manager / my team].
Pull from what I accomplished this week.
```

## The Automation Layer

### Hook: Auto-Detect Overwhelm
Create a hook at `.claude/hooks/overwhelm-detector.sh`:
When the user's message contains phrases like "too many tasks", "overwhelmed",
"don't know what to work on", "everything is urgent", "100 things" —
automatically suggest running this workflow.

### Hook: Monday Morning Trigger
Create a hook that on the first prompt every Monday, suggests:
"It's Monday. Want to run your weekly LNO audit?"

### Hook: Meeting Classifier
Before any meeting prep, automatically ask:
"Is this meeting Leverage, Neutral, or Overhead?"
This one question changes how much prep time you invest.

## The Compounding Effect

Week 1: You classify tasks. It feels manual.
Week 4: You notice patterns. "Status meetings are always Overhead."
Week 8: You've eliminated 3 recurring Overhead meetings. Freed 4 hours/week.
Week 12: Your CLAUDE.md has rules like "Never spend >15 min on status updates."
Week 20: The AI already knows your LNO patterns. Classification is instant.

**That's the difference between "using AI" and "having a system."**
The system compounds. One-off prompts don't.

## Self-Check
- [ ] Daily loop takes ≤15 minutes (if longer, you're over-engineering)
- [ ] Only ONE Leverage task per day (focus, not multitasking)
- [ ] Overhead batch is ≤30 minutes (if more, you need to delegate/eliminate)
- [ ] Weekly audit compares actual vs. ideal time allocation
- [ ] Meeting classification is applied (most PMs skip this)
- [ ] End-of-day checkpoint feeds back into tomorrow's plan
