---
name: launch-checklist
description: Use when the user asks about launching a feature, release readiness, go-to-market preparation, or launch planning.
tools: []
---

# Launch Checklist Skill

## Trigger
When the user asks about feature launches, release readiness, GTM prep, or needs a launch checklist.

## Instructions

### Phase 1: Launch Classification
Determine the launch type first — this drives the checklist scope:

| Launch Type | Who Knows | Checklist Depth | Example |
|-------------|-----------|-----------------|---------|
| **Silent** | Internal only | Light | Bug fix, backend migration |
| **Soft launch** | Select users | Medium | Beta feature, 5% rollout |
| **Full launch** | All users | Full | New feature, pricing change |
| **Major launch** | Public + press | Maximum | New product line, rebrand |

Ask the user if not clear: "Is this a silent ship, soft launch, full launch, or major launch?"

### Phase 2: Generate the Checklist

```markdown
# Launch Checklist: [Feature Name]
**Launch type**: [Silent/Soft/Full/Major]
**Target date**: [Date]
**Launch owner**: @name
**Status**: 🔴 Not Ready / 🟡 In Progress / 🟢 Ready

---

## T-14 Days: Pre-Launch

### Product Readiness
- [ ] All P0 requirements complete and tested
- [ ] All P1 requirements complete or explicitly descoped (with stakeholder sign-off)
- [ ] Edge cases documented and handled
- [ ] Error states and empty states designed and built
- [ ] Loading states implemented
- [ ] Rollback plan documented and tested

### Quality
- [ ] QA sign-off received
- [ ] Performance benchmarks met (page load < Xs, API response < Yms)
- [ ] Accessibility audit passed (WCAG 2.1 AA minimum)
- [ ] Cross-browser testing complete (Chrome, Safari, Firefox, Edge)
- [ ] Mobile responsive testing complete
- [ ] Security review passed (if applicable)
- [ ] Load testing passed (if applicable)

### Data & Analytics
- [ ] All tracking events implemented
- [ ] Events verified in staging (not just "deployed")
- [ ] Dashboard created with launch metrics
- [ ] Baseline metrics captured (BEFORE launch)
- [ ] A/B test configured (if gradual rollout)
- [ ] Alerting set up for key metrics (anomaly detection)

### Compliance & Regulatory (for regulated industries)
- [ ] Legal review completed
- [ ] Privacy impact assessment done
- [ ] Data processing agreements updated
- [ ] User consent flows updated (if new data collection)
- [ ] Audit trail logging enabled
- [ ] Regulatory documentation updated

---

## T-7 Days: Stakeholder Readiness

### Internal Communication
- [ ] Engineering team briefed on rollout plan
- [ ] Customer support team trained on new feature
- [ ] Support documentation / FAQ created
- [ ] Sales team briefed (if customer-facing)
- [ ] Leadership notified of launch timeline
- [ ] On-call rotation confirmed for launch week

### Documentation
- [ ] Help center article written and reviewed
- [ ] In-app tooltips / onboarding configured
- [ ] Changelog entry drafted
- [ ] Internal wiki updated
- [ ] API documentation updated (if applicable)

### External Communication (Full/Major launches only)
- [ ] Launch email drafted and reviewed
- [ ] Blog post drafted and reviewed
- [ ] Social media posts scheduled
- [ ] Press outreach sent (Major launches only)
- [ ] Partner notifications sent (if applicable)

---

## T-1 Day: Final Checks

### Go/No-Go
- [ ] All "T-14" items complete
- [ ] All "T-7" items complete
- [ ] Feature flag configured for rollout %
- [ ] Rollback procedure verified
- [ ] War room / monitoring channel created
- [ ] Launch owner available for full launch window

### Final Metrics Snapshot
| Metric | Pre-Launch Baseline | Target | Alert Threshold |
|--------|-------------------|--------|-----------------|
| [Primary] | X | Y | Below Z |
| [Secondary] | X | Y | Below Z |
| [Guardrail] | X | Must stay above Y | Below Z |

---

## Launch Day (T-0)

### Execution
- [ ] Feature flag enabled to [X]% of users
- [ ] Monitoring dashboard open and watched
- [ ] Support team on standby
- [ ] First 30 minutes: check error rates, latency, conversion
- [ ] First 2 hours: check user behavior matches expectations
- [ ] Internal announcement sent
- [ ] External announcement sent (if applicable)

### Escalation Path
| Issue Severity | Action | Who to Contact |
|---------------|--------|---------------|
| P0 (broken) | Immediate rollback | @eng-lead |
| P1 (degraded) | Assess within 30 min | @pm + @eng-lead |
| P2 (minor) | Track, fix in next sprint | @pm |

---

## T+1 to T+7: Post-Launch

### Day 1 Review
- [ ] Error rates normal?
- [ ] Key metrics trending as expected?
- [ ] Any unexpected user behavior?
- [ ] Support ticket volume normal?
- [ ] Proceed to next rollout stage? Y/N

### Day 7 Review
- [ ] Metrics vs. targets:
  | Metric | Target | Actual | Status |
  |--------|--------|--------|--------|
  | ... | ... | ... | ✅/⚠️/❌ |
- [ ] Top user feedback themes
- [ ] Bugs discovered (severity + status)
- [ ] Decision: Full rollout / Hold / Rollback

### Retrospective
- [ ] What went well?
- [ ] What went wrong?
- [ ] What would we do differently?
- [ ] Action items for next launch

---

## T+30: Launch Impact Report
- [ ] Final metrics report published
- [ ] Learnings documented in project folder
- [ ] Team retro completed
- [ ] Case study drafted (if significant impact)
- [ ] Repo updated with new metrics, queries, schemas
```

## Self-Check
Before presenting:
- [ ] Launch type correctly classified
- [ ] Compliance section included for regulated industries
- [ ] Rollback plan is not just "mentioned" — it's specific
- [ ] Metrics have baselines AND targets AND alert thresholds
- [ ] Escalation path has specific people, not generic roles
- [ ] Post-launch includes a 30-day impact report (most people skip this)
- [ ] Checklist items are checkable (binary yes/no), not vague
- [ ] Support team prep is included (most PM launches forget this)

## Output Format
Markdown checklist with clear time-based phases. Tables for metrics and escalation. Every item should be actionable by one person.
