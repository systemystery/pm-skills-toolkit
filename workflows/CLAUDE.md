# Workflows Directory Index

This folder contains multi-step processes that chain skills together. Workflows tell you WHEN to use WHICH skill.

## Files

| File | What It Does | Frequency |
|------|-------------|-----------|
| `pm-daily-system.md` | **The master workflow.** 15-minute daily loop: brain dump → 4A classify → focus → meeting prep → EOD check. Chains all other skills automatically. | Daily (every morning) |
| `daily-standup.md` | Morning context load: check calendar, project status, prep for meetings, set today's 3 priorities | Daily |
| `weekly-synthesis.md` | Cross-project status rollup: what shipped, what's blocked, stakeholder update draft, next week priorities | Weekly (Friday or Monday) |
| `quarterly-planning.md` | Full planning cycle: score last quarter's OKRs → gather strategy inputs → generate new OKRs → build roadmap → stakeholder deck | Quarterly (2-3 weeks before new quarter) |

## Recommended Flow
1. **Start here**: `pm-daily-system.md` — run this every morning
2. **End of week**: `weekly-synthesis.md` — synthesize and plan ahead
3. **End of quarter**: `quarterly-planning.md` — the full planning cycle
4. `daily-standup.md` is a lighter alternative to the full daily system

## How Workflows Chain Skills
Workflows reference skills from `/skills/`. For example, `pm-daily-system.md` automatically suggests:
- `task-prioritizer.md` for daily LNO/4A classification
- `stakeholder-brief.md` for weekly updates
- `okr-generator.md` during quarterly planning
