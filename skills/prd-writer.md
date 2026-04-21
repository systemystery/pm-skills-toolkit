---
name: prd-writer
description: Use when the user asks to write, create, or draft a PRD, product requirements document, spec, or feature specification.
tools: []
---

# PRD Writer Skill

## Trigger
When the user asks to write a PRD, product spec, feature spec, or requirements document.

## Instructions

### Phase 1: Requirements Gathering
Before writing anything, gather context. Ask the user:

1. **What problem are we solving?** (Not what feature are we building)
2. **Who experiences this problem?** (Specific user segment, not "users")
3. **How do we know this is a real problem?** (Data, user quotes, support tickets)
4. **What does success look like?** (Specific metric + target + timeframe)
5. **What are the constraints?** (Timeline, tech debt, dependencies, compliance)

If the user provides a brief, extract answers to these questions from their input. If any are missing, ask before proceeding.

### Phase 2: Problem Validation
Before solutioning, validate the problem statement:
- Is it specific enough to measure?
- Is it scoped to one user segment?
- Does it have evidence (not just opinion)?
- Can we articulate what happens if we do nothing?

### Phase 3: Write the PRD
Follow this exact structure:

```markdown
# [Feature Name] — PRD

## Problem Statement
**Who**: [Specific user segment with size estimate]
**What**: [The problem in one sentence]
**Evidence**: [Data points, user quotes, or ticket volume]
**Cost of inaction**: [What happens if we don't solve this]

## Success Metrics
| Metric | Current | Target | Timeframe |
|--------|---------|--------|-----------|
| Primary metric | X | Y | Z weeks |
| Secondary metric | X | Y | Z weeks |
| Guardrail metric | X | Must not drop below Y | Ongoing |

## Solution Overview
[2-3 sentence summary of the approach]

## User Stories
- As a [user type], I want to [action] so that [outcome]
- As a [user type], I want to [action] so that [outcome]

## Detailed Requirements

### Must Have (P0)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|
| 1 | ... | ... |

### Should Have (P1)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|

### Nice to Have (P2)
| # | Requirement | Acceptance Criteria |
|---|------------|-------------------|

## Technical Considerations
- **Dependencies**: [Systems, APIs, teams involved]
- **Data requirements**: [New events, schema changes]
- **Performance**: [Latency, throughput expectations]
- **Security/Compliance**: [Any regulatory requirements]

## Design Requirements
- [Link to mockups or describe key interactions]
- [Accessibility requirements]
- [Mobile/responsive considerations]

## Go-to-Market
- **Launch type**: [Silent / Beta / Full launch]
- **Rollout plan**: [% rollout stages]
- **Documentation**: [Help center, changelog, training]
- **Communication**: [Internal teams to notify]

## Risks & Mitigations
| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| ... | High/Med/Low | High/Med/Low | ... |

## Timeline
| Phase | Dates | Deliverable |
|-------|-------|-------------|
| Design | ... | Mockups approved |
| Build | ... | Feature complete |
| QA | ... | Bug-free release |
| Launch | ... | Feature live to X% |

## Open Questions
- [ ] Question 1 — Owner: @name, Due: date
- [ ] Question 2 — Owner: @name, Due: date

## Appendix
- Related docs
- Competitive screenshots
- Raw data
```

### Phase 4: Self-Improvement
After the first draft, iterate:
1. Read the PRD as if you're an engineer — are the requirements clear enough to build from?
2. Read it as a designer — are the user needs clear?
3. Read it as a stakeholder — is the business case compelling?

## Self-Check
Before presenting the PRD:
- [ ] Problem statement is specific and evidence-backed
- [ ] Success metrics have current baseline AND target AND timeframe
- [ ] At least one guardrail metric is defined
- [ ] Requirements are prioritized (P0/P1/P2)
- [ ] Every requirement has acceptance criteria
- [ ] Risks section has at least 3 entries
- [ ] Open questions have owners and due dates
- [ ] No vague language ("improve", "better", "faster") without numbers
- [ ] Timeline is realistic given the scope

## Output Format
A complete markdown document following the structure above. Bold key decisions. Use tables for structured data. End with clear next steps.
