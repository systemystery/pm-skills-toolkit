# Context Management Guide

How to stop burning tokens and start getting better output.

## The Problem

You paste a PRD, a competitive analysis, and three customer call transcripts into Claude. You've consumed half your context window before asking a question. No thinking room left.

**That is the trap.**

## The Solution: Load Only What You Need

### The 3-Tier System

**Tier 1 — Always Loaded (<500 tokens)**
- Root `CLAUDE.md` — doc index, key rules, preferences
- `GOALS.md` — current priorities
- Loaded every session automatically

**Tier 2 — Loaded on Query (200-500 tokens each)**
- Folder-level `CLAUDE.md` indexes
- Only loaded when Claude navigates to that folder
- Example: `skills/CLAUDE.md` is only read when you ask for a skill

**Tier 3 — Loaded on Demand (hundreds to thousands of tokens)**
- Individual skill files, PRDs, transcripts, SQL queries
- Only loaded when specifically needed
- Example: `skills/prd-writer.md` is only read when writing a PRD

### Why This Matters
A customer call transcript is 10,000+ tokens. A structured summary is 500. Always store summaries. Reference full transcripts only when the summary doesn't answer the question.

## Failure Modes

| Failure | What Happens | Fix |
|---------|-------------|-----|
| **Flat repo, no indexes** | Claude runs explore agents for every query. Burns thousands of tokens navigating. | Add CLAUDE.md to every folder |
| **Overstuffed root file** | Everything loaded every session. Kills thinking room. | Root CLAUDE.md should be <1 page |
| **Full transcripts everywhere** | Context fills before you ask a question | Store summaries, reference full on demand |
| **Too many MCPs** | 8-16% context eaten before you type anything | Replace MCPs with CLIs where possible |
| **Never clearing context** | Old task context pollutes new task | Type `clear` between tasks |

## Context Budget

Before you type a single message, this is already loaded:

| Component | Context Cost |
|-----------|-------------|
| System prompt | ~2% (can't change) |
| MCP servers | ~8%+ (each adds overhead) |
| Custom agents | ~4% |
| Root CLAUDE.md | ~1% |
| **Total before you start** | **~15%** |

**You have ~85% left. Protect it.**

## Sub-Agent Pattern

Without sub-agents, a research task pushes context from 16% to 25% (+10%).
With a sub-agent, the same task costs +0.5%.

```
Spin up a sub-agent to [research task]. 
Write findings to a temp file at /tmp/research-[topic].md.
Then give me a 5-bullet summary.
```

The sub-agent uses its own context window. Your main session stays clean.

---

*"Someone who burns hundreds of thousands of tokens and hits their usage limit in 30 minutes generally has unstructured, unoptimized context." — Hannah Stulberg*
