---
name: ab-test-designer
description: Use when the user asks to design an experiment, A/B test, or validate a hypothesis with data.
tools: []
---

# A/B Test Designer Skill

## Trigger
When the user asks to design an A/B test, experiment, or needs to validate a product hypothesis.

## Instructions

### Phase 1: Hypothesis
Structure every test as: "If we [change], then [metric] will [direction] by [amount] because [reasoning]."

Bad: "Let's test the new onboarding"
Good: "If we reduce onboarding from 5 steps to 3, then Day-7 activation will increase from 35% to 42% because users abandon at step 4 (62% drop-off)"

### Phase 2: Experiment Design

```markdown
# Experiment: [Name]

## Hypothesis
If we [change], then [metric] will [direction] by [amount]
because [reasoning backed by data/research].

## Variants
| Variant | Description | % Traffic |
|---------|------------|-----------|
| Control (A) | Current experience | 50% |
| Treatment (B) | [Specific change] | 50% |

## Metrics
| Type | Metric | Expected Change |
|------|--------|----------------|
| **Primary** | [One metric that decides success] | +X% |
| **Secondary** | [Supporting signal] | +Y% |
| **Guardrail** | [Must not degrade] | No change |

## Audience
- **Who**: [User segment]
- **Eligibility**: [Criteria to enter test]
- **Exclusions**: [Who should NOT see this]
- **Sample size needed**: [Calculate below]

## Statistical Rigor
- **Baseline rate**: [Current conversion/metric value]
- **Minimum detectable effect (MDE)**: [Smallest change worth detecting]
- **Significance level**: 95% (α = 0.05)
- **Power**: 80% (β = 0.20)
- **Estimated sample size**: [Per variant]
- **Estimated duration**: [Days to reach sample size]

## Risks
| Risk | Mitigation |
|------|-----------|
| Novelty effect | Run for minimum 2 full weeks |
| Selection bias | Randomize at user level, not session |
| Interaction with other tests | Check for overlapping experiments |

## Decision Framework
| Result | Action |
|--------|--------|
| Primary ↑, Guardrail stable | Ship treatment |
| Primary ↑, Guardrail ↓ | Investigate trade-off |
| Primary flat | Don't ship, learn why |
| Primary ↓ | Kill experiment, document learnings |

## Success Criteria
This experiment is successful if:
1. Primary metric improves by ≥ [MDE] with 95% confidence
2. Guardrail metrics do not degrade by > [threshold]
3. Results are consistent across [key segments]
```

## Self-Check
- [ ] Hypothesis is falsifiable with a specific predicted magnitude
- [ ] Only ONE primary metric (not three "primaries")
- [ ] Sample size is calculated, not guessed
- [ ] Guardrail metrics are defined
- [ ] Duration accounts for weekly cycles (min 2 weeks)
- [ ] Decision framework is pre-committed (before seeing results)
- [ ] Audience exclusions make sense

## Output Format
Structured markdown. Include the decision framework — pre-committing to actions prevents cherry-picking results.
