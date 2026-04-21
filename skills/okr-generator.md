---
name: okr-generator
description: Use when the user asks to create OKRs, set objectives, define key results, or do quarterly/annual goal setting.
tools: []
---

# OKR Generator Skill

## Trigger
When the user asks to create OKRs, set goals, define objectives, or plan quarterly/annual targets.

## Instructions

### Phase 1: Context Gathering
Before generating OKRs, understand:
1. **What level?** (Company / Team / Individual)
2. **What time period?** (Quarter / Half / Annual)
3. **What's the strategy?** (Top-level priorities or company objectives to ladder into)
4. **What happened last period?** (Previous OKRs, what hit, what missed, why)
5. **What constraints exist?** (Headcount, budget, dependencies)

### Phase 2: Objective Design
Good objectives follow these rules:
- **Qualitative, not quantitative** (Numbers go in Key Results)
- **Inspirational but achievable** (Stretchy, not delusional)
- **Time-bound by the period** (Not "eventually")
- **Ladders up** to company/team objective
- **3-5 objectives max** per team per quarter

Bad: "Increase revenue by 20%"
Good: "Become the go-to solution for enterprise onboarding"

### Phase 3: Key Results Design
Each objective gets 2-4 key results. Every KR must be:

| Criteria | Test |
|----------|------|
| **Measurable** | Can I put a number on it? |
| **Has a baseline** | Do I know where we are today? |
| **Has a target** | Is the target specific? |
| **Time-bound** | Does it have a deadline? |
| **Outcome, not output** | Does it measure impact, not activity? |

Bad: "Ship the new onboarding flow" (output)
Good: "Increase Day-7 retention from 35% to 50%" (outcome)

### Phase 4: Add Leading Indicators & Guardrails

```markdown
## Objective: [Inspirational statement]

### Key Results
| # | Key Result | Baseline | Target | Confidence | Owner |
|---|-----------|----------|--------|------------|-------|
| KR1 | [Outcome metric] | X | Y | 70% | @name |
| KR2 | [Outcome metric] | X | Y | 50% | @name |
| KR3 | [Outcome metric] | X | Y | 60% | @name |

### Leading Indicators
_Early signals that predict KR success (check weekly):_
| Indicator | Current | Healthy Range | Alert If |
|-----------|---------|--------------|----------|
| ... | X | Y-Z | Below W |

### Guardrail Metrics
_Things that must NOT break while pursuing these KRs:_
| Metric | Current | Must Stay Above |
|--------|---------|----------------|
| ... | X | Y |

### Key Initiatives
_The bets we're making to hit these KRs:_
| Initiative | Expected Impact | Effort | Status |
|-----------|----------------|--------|--------|
| ... | Drives KR1 by ~X% | M weeks | Not started |

### Risks to Achieving
| Risk | Likelihood | Mitigation |
|------|-----------|------------|
| ... | Med | ... |

### Dependencies
- [Team/system] — What we need from them by when
```

### Phase 5: Scoring Framework
Include a grading rubric:

| Score | Meaning | Interpretation |
|-------|---------|----------------|
| 0.0-0.3 | Failed to make progress | Wrong bet or poor execution |
| 0.4-0.6 | Made progress | Typical "stretch" result |
| 0.7-1.0 | Delivered | Either great execution or target wasn't stretchy enough |

**Ideal average score: 0.6-0.7.** If you're hitting 1.0 on everything, your targets aren't ambitious enough.

## Self-Check
Before presenting:
- [ ] 3-5 objectives maximum
- [ ] Each objective is qualitative and inspirational
- [ ] Each KR has baseline, target, and timeframe
- [ ] KRs measure outcomes, not outputs
- [ ] Confidence levels are realistic (50-70% for stretch goals)
- [ ] At least one guardrail metric per objective
- [ ] Leading indicators are identified for weekly check-ins
- [ ] Every KR has an owner
- [ ] OKRs ladder up to the next level's objectives
- [ ] No vanity metrics (page views alone, signup count without activation)

## Output Format
Structured markdown with tables. Group by objective. Include the scoring framework at the end. Bold the objectives. Each section should stand alone (printable for team meetings).
