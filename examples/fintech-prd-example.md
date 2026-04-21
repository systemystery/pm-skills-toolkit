# FinTech PRD Example: AI-Powered Investment Commentary Tool

> This is a real-world example of a PRD built using the `/skills/prd-writer.md` skill. It demonstrates how to write a PRD for a FinTech product with compliance considerations.

---

# AI-Powered Investment Commentary Tool — PRD

## Problem Statement
**Who**: 47 investment directors across 12 portfolio teams who write quarterly client commentaries
**What**: Each director spends 6-8 hours per quarter writing personalized commentaries for their client portfolios, resulting in 380+ hours of senior talent time spent on repetitive writing
**Evidence**: Internal time tracking shows commentary writing is the #2 time sink after client meetings. 73% of directors rated it "the task I most want to automate" in Q3 survey. Three directors have missed deadlines in the last two quarters.
**Cost of inaction**: $285K/quarter in senior talent time. Missed deadlines risk client dissatisfaction. Quality varies significantly across directors — some clients get excellent commentaries, others get boilerplate.

## Success Metrics
| Metric | Current Baseline | Target | Timeframe |
|--------|-----------------|--------|-----------|
| **Time to draft commentary** | 6-8 hours | < 1 hour | 8 weeks post-launch |
| Commentary quality score (peer review) | 3.2/5.0 | ≥ 4.0/5.0 | 12 weeks post-launch |
| On-time delivery rate | 82% | 98% | 8 weeks post-launch |
| Guardrail: Client satisfaction (NPS) | +42 | Must stay ≥ +38 | Ongoing |
| Guardrail: Compliance incidents | 0 | Must stay at 0 | Ongoing |

## Solution Overview
An AI-powered tool that generates draft investment commentaries from portfolio performance data, market research, and the director's historical writing style. Directors review and edit AI drafts rather than writing from scratch. All outputs pass through compliance checks before delivery.

## User Stories
- As an **investment director**, I want to generate a first draft of my quarterly commentary from my portfolio data so that I spend my time refining insights rather than writing boilerplate
- As a **compliance officer**, I want every AI-generated commentary to be flagged for review so that no unapproved content reaches clients
- As a **client**, I want my commentary to reflect my specific portfolio performance and market context so that I trust my advisor understands my investments

## Detailed Requirements

### Must Have (P0)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Ingest portfolio performance data from existing systems | Connects to Portfolio Analytics API; refreshes daily |
| 2 | Generate draft commentary matching director's writing style | Director rates style match ≥ 4/5 in blind test |
| 3 | Include market context and attribution analysis | References correct benchmarks and sector performance |
| 4 | Compliance review workflow | Draft flagged for compliance; cannot be sent without approval |
| 5 | Audit trail for all AI-generated content | Every draft version stored with timestamp and editor |

### Should Have (P1)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Director can adjust tone (conservative/balanced/optimistic) | Three tone presets that produce noticeably different outputs |
| 2 | Batch generation for multiple client portfolios | Can generate 20+ drafts in one session |
| 3 | Track edits to improve model over time | System learns from director corrections |

### Nice to Have (P2)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Client-specific historical context | References past commentaries and client preferences |
| 2 | Multi-language support | Supports English and Mandarin initially |

## Technical Considerations
- **Dependencies**: Portfolio Analytics API (owned by Data team), Market Data Feed (vendor), LLM provider (vendor selection needed)
- **Data requirements**: 3 years of historical commentaries per director for style training; daily portfolio performance feed
- **Performance**: Draft generation < 30 seconds; batch of 20 < 5 minutes
- **Security/Compliance**: SOC 2 Type II required for LLM vendor; no client PII in prompts; all data stays in-region (US/EU); model outputs must be deterministic enough for compliance review

## Risks & Mitigations
| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| AI hallucinates performance numbers | Medium | Critical | All numerical claims validated against source data before display |
| Directors don't trust AI output | High | High | Start with "draft assistant" positioning, not "replacement"; pilot with 3 enthusiastic directors |
| Compliance rejects AI-generated content | Medium | High | Involve compliance team from Day 1; build review workflow they approve |
| LLM vendor data privacy concerns | Low | Critical | On-premise or private cloud deployment; no data leaves our infrastructure |
| Writing style doesn't match | Medium | Medium | Fine-tune on each director's historical commentaries; allow style correction feedback loop |

## Timeline
| Phase | Dates | Deliverable |
|-------|-------|-------------|
| Design + Compliance Review | Weeks 1-3 | Approved workflow design; compliance sign-off |
| Build: Data pipeline + LLM integration | Weeks 4-8 | Working prototype with sample commentaries |
| Pilot: 3 directors | Weeks 9-12 | Quality scores, time savings data, compliance feedback |
| Iterate + Scale | Weeks 13-16 | Full rollout to all 47 directors |

## Open Questions
- [ ] Which LLM vendor passes our security review? — Owner: @cto, Due: Week 2
- [ ] Can we use historical commentaries for training under existing data policies? — Owner: @legal, Due: Week 1
- [ ] What's the compliance team's capacity for reviewing AI drafts? — Owner: @compliance-lead, Due: Week 2

---

*This PRD was generated using the [PRD Writer Skill](/skills/prd-writer.md) from the PM Skills Toolkit.*
