---
name: stakeholder-brief
description: Use when the user asks to write a message, email, update, or brief for a specific stakeholder, executive, or team.
tools: []
---

# Stakeholder Brief Skill

## Trigger
When the user asks to draft a message, update, email, Slack message, or brief tailored to a specific audience (executive, engineering, design, sales, support, board).

## Instructions

### Phase 1: Audience Analysis
Before writing anything, determine:
1. **Who is the audience?** (Specific person or group)
2. **What do they care about?** (Their incentives and concerns)
3. **What action do you need from them?** (Approve, review, be informed, unblock)
4. **What's their context level?** (Deep in the project vs. hearing about it for the first time)
5. **What format do they prefer?** (Check knowledge/people/ files if available)

### Phase 2: Audience Profiles
Use these default profiles if no people files exist:

| Audience | They Care About | They Don't Want | Format |
|----------|----------------|-----------------|--------|
| **CEO/C-Suite** | Revenue impact, strategic alignment, risk | Details, technical specs | 3 bullets + 1 ask |
| **VP/Director** | Team velocity, cross-team dependencies, timelines | Individual task status | Summary + key decisions |
| **Engineering Lead** | Technical feasibility, scope clarity, edge cases | Marketing language, vague requirements | Specific, technical, structured |
| **Design Lead** | User impact, research backing, interaction details | Decisions made without user data | Visual references, user quotes |
| **Sales/CS** | Customer impact, talking points, timeline | Internal process details | FAQ format, customer-facing language |
| **Board** | Market position, growth metrics, strategic bets | Operational details | Narrative + 3 key metrics |
| **Legal/Compliance** | Regulatory risk, data handling, liability | Feature excitement | Risk assessment, precedent |

### Phase 3: Draft Using the Right Framework

**For Executives (CEO, VP, Board):**
```markdown
## [Topic] — [Status: On Track / At Risk / Blocked]

**TL;DR**: [One sentence summary + the ask]

**Context** (2-3 sentences max):
[Why this matters right now]

**Key Update**:
- ✅ [What's going well]
- ⚠️ [What needs attention]
- 🚫 [What's blocked + what you need]

**The Ask**: [Specific action, specific timeline]
```

**For Engineering:**
```markdown
## [Feature/Project] — PM Update

**What changed since last sync**:
- [Decision made + rationale]
- [Scope change + why]

**Open questions for eng**:
1. [Specific technical question]
2. [Feasibility check]

**Updated requirements** (if any):
| # | Requirement | Change | Reason |
|---|------------|--------|--------|
| ... | ... | Added/Modified/Removed | ... |

**Timeline impact**: [None / Shifted by X days / TBD pending answer to Q1]
```

**For Design:**
```markdown
## [Feature] — Design Brief

**User Problem**: [Evidence-backed problem statement]

**Key User Quotes**:
> "[Quote from research]"

**Requirements that affect design**:
- [Constraint 1 — why it exists]
- [Constraint 2 — why it exists]

**What I need from you**:
- [ ] [Specific deliverable] by [date]

**Reference**: [Links to mockups, competitors, inspiration]
```

**For Sales/Customer Success:**
```markdown
## [Feature] — What You Need to Know

**What's launching**: [Customer-friendly one-liner]
**When**: [Date + rollout plan]
**Who gets it**: [Plans/tiers/segments]

**Talking Points**:
- "We built this because [customer problem]"
- "This means you can now [benefit]"
- "The key difference from [competitor] is [differentiator]"

**FAQ**:
| Question | Answer |
|----------|--------|
| "When can my customer get this?" | [Answer] |
| "Does this change pricing?" | [Answer] |
| "What if they have [edge case]?" | [Answer] |

**Not ready to discuss** (internal only):
- [Things still in flux]
```

### Phase 4: Tone Calibration
Adjust tone based on the situation:

| Situation | Tone | Example |
|-----------|------|---------|
| Good news | Confident, celebrating | "We shipped ahead of schedule" |
| Bad news | Direct, solution-oriented | "We're behind by 2 weeks. Here's the plan." |
| Ask for resources | Data-backed, business case | "This unblocks $Xk ARR at risk" |
| Escalation | Factual, no blame | "Here's where we are and what we need" |

## Self-Check
Before presenting:
- [ ] Audience is explicitly identified
- [ ] Format matches what that audience wants (not what you want to say)
- [ ] There's a clear, specific ask (not "let me know what you think")
- [ ] Context level matches their familiarity (no over-explaining to experts, no jargon for executives)
- [ ] Tone matches the situation
- [ ] Length is appropriate (executives get bullets, engineers get detail)
- [ ] If sharing bad news: the mitigation plan is included, not just the problem
- [ ] If asking for a decision: the options and your recommendation are clear

## Output Format
Markdown formatted for the specific audience. Use the framework templates above as the structure. Keep executive comms under 200 words. Keep engineering comms as detailed as needed.
