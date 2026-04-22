# FinTech PRD Example: AI-Powered Document Generation Tool

> This is a real-world example of a PRD built using the `/skills/prd-writer.md` skill. It demonstrates how to write a PRD for a FinTech product with compliance considerations.

---

# AI-Powered Document Generation Tool — PRD

## Problem Statement
**Who**: ~50 senior analysts across 10+ teams who write quarterly client reports
**What**: Each analyst spends 6-8 hours per quarter writing personalized reports for their client portfolios, resulting in 400+ hours of senior talent time spent on repetitive writing
**Evidence**: Internal time tracking shows report writing is the #2 time sink after client meetings. 73% of analysts rated it "the task I most want to automate" in the last internal survey. Multiple analysts have missed deadlines in the last two quarters.
**Cost of inaction**: Significant cost in senior talent time per quarter. Missed deadlines risk client dissatisfaction. Quality varies significantly across analysts — some clients get excellent reports, others get boilerplate.

## Success Metrics
| Metric | Current Baseline | Target | Timeframe |
|--------|-----------------|--------|-----------|
| **Time to draft report** | 6-8 hours | < 1 hour | 8 weeks post-launch |
| Report quality score (peer review) | 3.2/5.0 | ≥ 4.0/5.0 | 12 weeks post-launch |
| On-time delivery rate | 82% | 98% | 8 weeks post-launch |
| Guardrail: Client satisfaction (NPS) | +42 | Must stay ≥ +38 | Ongoing |
| Guardrail: Compliance incidents | 0 | Must stay at 0 | Ongoing |

## Solution Overview
An AI-powered tool that generates draft client reports from structured data, market research, and the analyst's historical writing style. Analysts review and edit AI drafts rather than writing from scratch. All outputs pass through compliance checks before delivery.

## User Stories
- As a **senior analyst**, I want to generate a first draft of my quarterly report from my data so that I spend my time refining insights rather than writing boilerplate
- As a **compliance officer**, I want every AI-generated report to be flagged for review so that no unapproved content reaches clients
- As a **client**, I want my report to reflect my specific situation and relevant context so that I trust my advisor understands my needs

## Detailed Requirements

### Must Have (P0)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Ingest structured data from existing internal systems | Connects to internal data API; refreshes daily |
| 2 | Generate draft report matching analyst's writing style | Analyst rates style match ≥ 4/5 in blind test |
| 3 | Include relevant context and data analysis | References correct benchmarks and key metrics |
| 4 | Compliance review workflow | Draft flagged for compliance; cannot be sent without approval |
| 5 | Audit trail for all AI-generated content | Every draft version stored with timestamp and editor |

### Should Have (P1)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Analyst can adjust tone (conservative/balanced/confident) | Three tone presets that produce noticeably different outputs |
| 2 | Batch generation for multiple client reports | Can generate 20+ drafts in one session |
| 3 | Track edits to improve model over time | System learns from analyst corrections |

### Nice to Have (P2)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | Client-specific historical context | References past reports and client preferences |
| 2 | Multi-language support | Supports English and one additional language initially |

## Technical Considerations
- **Dependencies**: Internal data API (owned by Data team), external data feeds (vendor), LLM provider (vendor selection needed)
- **Data requirements**: Historical reports per analyst for style training; regular data feed
- **Performance**: Draft generation < 30 seconds; batch of 20 < 5 minutes
- **Security/Compliance**: SOC 2 Type II required for LLM vendor; no client PII in prompts; all data stays in-region; model outputs must be deterministic enough for compliance review

## Risks & Mitigations
| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| AI hallucinates data points | Medium | Critical | All numerical claims validated against source data before display |
| Analysts don't trust AI output | High | High | Start with "draft assistant" positioning, not "replacement"; pilot with 3 enthusiastic analysts |
| Compliance rejects AI-generated content | Medium | High | Involve compliance team from Day 1; build review workflow they approve |
| LLM vendor data privacy concerns | Low | Critical | On-premise or private cloud deployment; no data leaves our infrastructure |
| Writing style doesn't match | Medium | Medium | Fine-tune on each analyst's historical reports; allow style correction feedback loop |

## Timeline
| Phase | Dates | Deliverable |
|-------|-------|-------------|
| Design + Compliance Review | Weeks 1-3 | Approved workflow design; compliance sign-off |
| Build: Data pipeline + LLM integration | Weeks 4-8 | Working prototype with sample reports |
| Pilot: 3 analysts | Weeks 9-12 | Quality scores, time savings data, compliance feedback |
| Iterate + Scale | Weeks 13-16 | Full rollout to all analysts |

## Open Questions
- [ ] Which LLM vendor passes our security review? — Owner: @cto, Due: Week 2
- [ ] Can we use historical reports for training under existing data policies? — Owner: @legal, Due: Week 1
- [ ] What's the compliance team's capacity for reviewing AI drafts? — Owner: @compliance-lead, Due: Week 2

---

*This PRD was generated using the [PRD Writer Skill](/skills/prd-writer.md) from the PM Skills Toolkit.*
