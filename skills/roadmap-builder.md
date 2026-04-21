---
name: roadmap-builder
description: Use when the user asks to create a roadmap, plan a quarter, prioritize features, or align on product direction.
tools: []
---

# Roadmap Builder Skill

## Trigger
When the user asks to build a roadmap, plan quarterly work, prioritize initiatives, or create a product direction document.

## Instructions

### Phase 1: Inputs
Gather:
1. **Time horizon**: Quarter / Half / Year
2. **Strategic pillars**: Top 3-5 company or team priorities
3. **Candidate initiatives**: All ideas, requests, and backlog items
4. **Constraints**: Headcount, budget, dependencies, tech debt

### Phase 2: Prioritization (RICE Framework)

Score every candidate initiative:

| Initiative | Reach | Impact | Confidence | Effort | RICE Score |
|-----------|-------|--------|-----------|--------|------------|
| [Name] | [Users/qtr] | [0.25-3] | [50-100%] | [person-weeks] | R×I×C/E |

**Scoring guide:**
- **Reach**: How many users affected per quarter
- **Impact**: 3=massive, 2=high, 1=medium, 0.5=low, 0.25=minimal
- **Confidence**: 100%=data-backed, 80%=strong signal, 50%=gut feel
- **Effort**: Person-weeks of work (all roles combined)

Sort by RICE score descending. Top items go into the roadmap.

### Phase 3: Build the Roadmap

```markdown
# Product Roadmap: [Q/Year]

## Strategic Context
**Company mission**: [One line]
**This period's theme**: [The overarching narrative]
**Key bets**: [2-3 strategic bets we're making]

## Roadmap Summary

### Now (This Sprint / This Month)
| Initiative | Goal | Owner | Status |
|-----------|------|-------|--------|
| [Name] | [Outcome metric target] | @name | 🟢/🟡/🔴 |

### Next (Next Month / Next 6 Weeks)
| Initiative | Goal | Owner | Confidence |
|-----------|------|-------|-----------|
| [Name] | [Outcome metric target] | @name | High/Med |

### Later (This Quarter / Rest of Half)
| Initiative | Goal | Dependency |
|-----------|------|-----------|
| [Name] | [Outcome metric target] | [What needs to be true] |

### Not Doing (Explicitly Deprioritized)
| Initiative | Why Not | Revisit When |
|-----------|---------|-------------|
| [Name] | [Reason] | [Condition to reconsider] |

## Dependencies Map
| Our Initiative | Depends On | Team | Status | Risk |
|---------------|-----------|------|--------|------|
| [Name] | [What we need] | @team | Confirmed/TBD | Low/Med/High |

## Resource Allocation
| Pillar | % of Eng | Initiatives |
|--------|---------|-------------|
| Growth | 40% | [List] |
| Platform/Infra | 25% | [List] |
| Quality/Debt | 20% | [List] |
| Exploration | 15% | [List] |

## Risks to the Plan
| Risk | Impact | Likelihood | Mitigation |
|------|--------|-----------|------------|
| [Risk] | High | Med | [Plan B] |

## How We'll Track Progress
- **Weekly**: Sprint review against roadmap milestones
- **Monthly**: Metrics review (are shipped things working?)
- **Quarterly**: Full roadmap review + reprioritization
```

### Phase 4: Tailor for Audience
- **For leadership**: Focus on themes, outcomes, strategic alignment
- **For engineering**: Focus on Now/Next, dependencies, technical risks
- **For the team**: Full detail including prioritization rationale

## Self-Check
- [ ] Roadmap uses Now/Next/Later (NOT dates for uncertain items)
- [ ] Every initiative has an outcome goal, not just a ship date
- [ ] "Not Doing" section exists (what you say no to defines strategy)
- [ ] RICE scores show the prioritization reasoning
- [ ] Dependencies are mapped with owners and status
- [ ] Resource allocation adds up to ~100%
- [ ] Tech debt / quality has dedicated allocation (not zero)
- [ ] Risks have mitigations

## Output Format
Structured markdown with Now/Next/Later sections. Tables for initiatives. Include the "Not Doing" section — it's the most strategically important part.
