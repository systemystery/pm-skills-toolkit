---
name: metrics-dashboard
description: Use when the user asks to define metrics, create a dashboard spec, set up KPIs, or instrument a feature.
tools: []
---

# Metrics Dashboard Spec Skill

## Trigger
When the user asks to define metrics, create KPIs, spec a dashboard, instrument a feature, or set up analytics tracking.

## Instructions

### Phase 1: Understand What to Measure
Ask the user:
1. **What feature or product area?**
2. **What's the goal?** (Growth, retention, monetization, quality)
3. **Who will read this dashboard?** (PM, exec, eng, data team)
4. **What decisions will this dashboard drive?**

### Phase 2: Metrics Framework
Apply the HEART framework (Google) + business metrics:

```markdown
# Metrics Spec: [Feature/Product Area]

## North Star Metric
**Metric**: [The ONE metric that best captures value delivered]
**Definition**: [Precise calculation]
**Current**: [Baseline value]
**Target**: [Goal + timeframe]
**Why this metric**: [Why it captures real value, not vanity]

## HEART Metrics

### Happiness (User Satisfaction)
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| NPS / CSAT | [How calculated] | [Survey / in-app] | [Weekly/Monthly] |
| Task satisfaction | [Rating after completing key flow] | [In-app] | [Real-time] |

### Engagement (Usage Depth)
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| DAU/MAU ratio | Active users daily / monthly | [Analytics tool] | Daily |
| Feature adoption | % of eligible users who used feature | [Events] | Weekly |
| Session depth | Actions per session | [Events] | Daily |

### Adoption (New User Uptake)
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| Activation rate | % of signups completing [key action] | [Events] | Daily |
| Time to first value | Minutes from signup to [aha moment] | [Events] | Daily |
| Feature discovery | % of users who find the feature | [Events] | Weekly |

### Retention (Users Coming Back)
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| D1 / D7 / D30 retention | % returning after 1/7/30 days | [Analytics] | Daily |
| Churn rate | % of users who stop using in [period] | [Analytics] | Weekly |
| Resurrection rate | % of churned users who return | [Analytics] | Monthly |

### Task Success (Completion & Efficiency)
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| Task completion rate | % who complete the intended flow | [Events] | Daily |
| Error rate | % of attempts that fail | [Events] | Real-time |
| Time on task | Median time to complete [flow] | [Events] | Daily |

## Business Metrics
| Metric | Definition | Source | Frequency |
|--------|-----------|--------|-----------|
| Revenue impact | ARR attributable to feature | [Billing] | Monthly |
| Conversion rate | % of [stage] → [next stage] | [Events] | Daily |
| Support ticket volume | Tickets related to feature | [Support tool] | Weekly |

## Guardrail Metrics
_Metrics that must NOT degrade:_
| Metric | Current | Alert If Below | Why It Matters |
|--------|---------|---------------|----------------|
| Page load time | Xms | Yms | Performance degrades conversion |
| Error rate | X% | Y% | Reliability = trust |
| Existing feature usage | X | Y | New feature shouldn't cannibalize |
```

### Phase 3: Tracking Plan
Specify the events to instrument:

```markdown
## Tracking Plan

### Events to Implement
| Event Name | Trigger | Properties | Priority |
|-----------|---------|------------|----------|
| `feature_viewed` | User sees the feature | `user_id, source, variant` | P0 |
| `feature_action_started` | User begins the flow | `user_id, entry_point` | P0 |
| `feature_action_completed` | User finishes the flow | `user_id, duration_ms, success` | P0 |
| `feature_error` | Flow fails | `user_id, error_type, step` | P0 |
| `feature_feedback` | User rates experience | `user_id, rating, comment` | P1 |

### Event Naming Convention
- Format: `[object]_[action]` (snake_case)
- Always include: `user_id`, `timestamp`, `session_id`
- Use consistent property names across events
```

### Phase 4: Dashboard Layout
Describe the visual layout:

```markdown
## Dashboard Layout

### Row 1: Health at a Glance
| North Star Metric | Trend (7d) | vs. Target |

### Row 2: Funnel
| Stage 1 → Stage 2 → Stage 3 → Stage 4 |
| (with conversion rates between each) |

### Row 3: Engagement
| DAU/MAU | Feature Adoption | Session Depth |

### Row 4: Quality
| Error Rate | Page Load | Support Tickets |

### Filters
- Date range (default: last 7 days)
- User segment (all / new / returning)
- Platform (web / mobile / API)
- Plan (free / pro / enterprise)
```

## Self-Check
Before presenting:
- [ ] North star metric is defined and is an OUTCOME, not an output
- [ ] Metrics cover all 5 HEART dimensions
- [ ] Every metric has a precise definition (not "engagement" without specifics)
- [ ] Guardrail metrics are included (what must NOT break)
- [ ] Tracking plan has event names, triggers, and properties
- [ ] Event naming follows a consistent convention
- [ ] Dashboard answers "what decisions will this drive?" — not just "what can we measure?"
- [ ] Metrics distinguish between leading (predictive) and lagging (outcome) indicators
- [ ] No vanity metrics without context (raw counts without rates/ratios)
- [ ] Data source is specified for every metric (not assumed)

## Output Format
Structured markdown with tables. Separate sections for metrics definitions, tracking plan, and dashboard layout. Include the "Why this metric" rationale — this is what separates thoughtful instrumentation from checkbox analytics.
