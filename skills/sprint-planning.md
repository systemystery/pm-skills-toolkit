---
name: sprint-planning
description: Use when the user asks to plan a sprint, create sprint goals, or break down stories.
tools: []
---

# Sprint Planning Skill

## Trigger
When the user asks to plan a sprint, break down work, estimate effort, or prepare for sprint planning.

## Instructions

### Phase 1: Sprint Context
Gather:
1. **Sprint duration**: 1 or 2 weeks
2. **Team capacity**: Engineers, designers, QA
3. **Carry-over**: Unfinished work from last sprint
4. **OKR alignment**: Which OKR does this serve?
5. **Known risks**: Dependencies, PTO, on-call

### Phase 2: Sprint Goal
One sentence. Not a ticket list.

**Formula**: "By end of sprint, [user segment] can [capability] which moves [metric] toward [target]."

### Phase 3: Story Breakdown
For each story, include:
- User story format (As a / I want / So that)
- Acceptance criteria (Given/When/Then)
- Estimate (story points)
- Priority (P0/P1/P2)
- Dependencies
- Design link

### Phase 4: Capacity Check

| Category | Points |
|----------|--------|
| Total capacity | X |
| Carry-over | Y |
| Bug budget (15%) | Z |
| Interrupt buffer (10%) | W |
| **Available** | **X-Y-Z-W** |

Health: ✅ P0+P1 < Available | ⚠️ P0+P1 = Available | 🚫 P0+P1 > Available → cut scope

### Phase 5: Risk & Definition of Done
Include risks with mitigations and explicit DoD (code reviewed, tested, deployed to staging, analytics firing).

## Self-Check
- [ ] Sprint goal is ONE outcome-oriented sentence
- [ ] Every story has acceptance criteria
- [ ] Capacity math includes buffers
- [ ] P0 items alone fit within capacity
- [ ] Dependencies called out
- [ ] No 13+ point stories (too large)

## Output Format
Structured markdown. User story format. Tables for capacity. Emoji health indicator.
