# Prompting Guide: How to Get 10x Better Output

Based on techniques from Carl Vellotti and Hannah Stulberg's AI operating systems.

## The Three Tiers of Prompting

### Tier 1: Basic Prompt (Quick tasks)
Just type your request. Fine for lookups and simple tasks.
```
What's the difference between OKRs and KPIs?
```
**When to use**: Simple questions, quick lookups, no ambiguity.

### Tier 2: Lightweight Alignment (Most tasks)
Add **"give me a proposal first"** to any prompt. Claude proposes an approach before executing. You course-correct in 30 seconds instead of fixing a bad output for 30 minutes.
```
Write a competitive analysis for [product]. Give me a proposal first — 
outline your approach, what sources you'll check, and the structure 
before you start writing.
```
**When to use**: Anything with even slight ambiguity. This is your default mode.

### Tier 3: Full Plan Mode (Complex work)
For strategy docs, PRDs, or anything multi-section. Press **Shift+Tab twice** in Claude Code to enter plan mode. Claude cannot execute until you approve the plan.
```
I need a quarterly product strategy doc. Enter plan mode:
1. Read /knowledge/company/ for context
2. Check /knowledge/research/ for latest user insights
3. Propose a section-by-section outline
4. I'll review and adjust before you write anything
```
**When to use**: Strategy docs, complex PRDs, anything you'll present to stakeholders.

---

## Power Prompts

### Push Your Thinking
After building a plan, use this to catch blind spots:
```
Use your ask-user-question tool to push me on my thinking. 
Help me consider other angles. Challenge my assumptions. 
Take as long as you need.
```

### The Ask-User-Questions Tool
Instead of letting Claude make assumptions, force it to ask:
```
Before starting, use your ask-user-questions tool to grill me on 
all possible requirements for this feature. Don't assume anything.
```

### Self-Check Any Output
After Claude generates anything, tell it to verify:
```
Double-check your output against the skill instructions. 
What did you miss? What assumptions did you make?
```

### Sub-Agent Delegation
Keep your main context clean by delegating research:
```
Spin up a sub-agent to research [topic]. Have it write findings 
to a temp file. Then summarize the key points back to me.
```
**Why**: Without sub-agents, research uses ~10% of your context window. With sub-agents, it uses ~0.5%.

---

## Context Management Tips

### Monitor Your Context
```
/status line
```
Shows a color-coded context meter. Green (<50%), Orange (50-80%), Red (>80%).

### Clear Between Tasks
Type `clear` when switching tasks. Leftover context pollutes results.

### Rollback Bad Prompts
Press **Escape twice** to undo a bad prompt. Everything after it is erased from context.

### CLI Over MCP
MCPs eat context just by existing. CLIs have zero context overhead.
- **GitHub CLI** (`gh`) — PRs, issues, repos
- **Vercel CLI** — deployments, logs
- **Firecrawl CLI** — web scraping

**Rule**: For every MCP you use, ask "does a CLI for this exist?" If yes, switch.

---

## The Decision Matrix

| Task Type | Prompting Tier | Time Investment |
|-----------|---------------|-----------------|
| Quick lookup | Tier 1 (basic) | 0 min planning |
| Routine doc with some ambiguity | Tier 2 (proposal first) | 30 sec alignment |
| Complex doc, multiple sections | Tier 3 (full plan) | 15-30 min planning |
| Multi-phase research project | Tier 3 + sub-agents | Hours across a day |
| Recurring process | Saved plan file | Start at 80% done |

---

## Save Your Plans
Native plan files in Claude Code get wiped every 24-72 hours. If you spent time on a plan, save it to your repo. Next time, you start at 80% done. Your team can reuse it.

```
Save this plan to /workflows/plans/[name]-plan.md so I can reuse it.
```

---

*"Most people under-plan. That is why the output doesn't match what they wanted. The plan is not overhead. The plan is the work." — Hannah Stulberg*
