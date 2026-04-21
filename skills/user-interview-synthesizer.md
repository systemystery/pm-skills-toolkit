---
name: user-interview-synthesizer
description: Use when the user shares customer call transcripts, user interview notes, or asks to synthesize user research findings.
tools: []
---

# User Interview Synthesizer Skill

## Trigger
When the user shares call transcripts, interview notes, user research data, or asks to analyze/synthesize customer feedback.

## Instructions

### Phase 1: Intake
Determine the input type:
- **Raw transcript**: Full call recording text
- **Meeting notes**: Summarized notes from a call
- **Multiple calls**: Batch of transcripts to synthesize
- **Survey responses**: Open-ended survey data

Ask if missing:
1. **What product/feature is this about?**
2. **What were the research questions going in?**
3. **Who was the customer?** (Segment, plan, tenure)

### Phase 2: Individual Call Summary
For each call/interview, extract:

```markdown
## Call Summary: [Customer Name/ID] — [Date]

### Customer Profile
- **Company**: [Name] | **Size**: [Employees/Revenue]
- **Role**: [Title of interviewee]
- **Segment**: [Enterprise/SMB/Consumer]
- **Tenure**: [How long they've been a customer]
- **Plan**: [Free/Pro/Enterprise]

### Key Quotes
> "[Direct quote that captures a critical insight]"
> — Context: [What they were discussing when they said this]

> "[Another important quote]"
> — Context: [...]

### Pain Points Identified
1. **[Pain point name]** — [Description + severity: High/Med/Low]
2. **[Pain point name]** — [Description + severity]

### Jobs to Be Done
- When [situation], I want to [action], so I can [outcome]
- When [situation], I want to [action], so I can [outcome]

### Feature Requests
| Request | Urgency (their words) | Frequency |
|---------|----------------------|-----------|
| ... | "We need this yesterday" | First mention |
| ... | "Would be nice" | Repeated ask |

### Emotional Moments
- **Frustration**: [What triggered it]
- **Delight**: [What made them happy]
- **Surprise**: [What they didn't expect]

### Workflow Observed
1. Step they take today → Tool they use → Pain at this step
2. Step they take today → Tool they use → Pain at this step

### Follow-up Actions
- [ ] Action item — Owner, Due date
```

### Phase 3: Cross-Call Synthesis
When synthesizing multiple calls:

```markdown
## Research Synthesis — [Topic] — [Date Range]

### Sample Overview
- **Total calls**: N
- **Segments represented**: [List]
- **Roles**: [List]

### Theme Heatmap
| Theme | Call 1 | Call 2 | Call 3 | ... | Frequency |
|-------|:------:|:------:|:------:|:---:|-----------|
| Theme A | 🔴 | 🔴 | ⚪ | ... | 67% |
| Theme B | 🔴 | ⚪ | 🔴 | ... | 67% |
| Theme C | ⚪ | 🔴 | ⚪ | ... | 33% |

🔴 = Mentioned | ⚪ = Not mentioned

### Top Insights (Ranked by Frequency × Severity)
1. **[Insight]** — Mentioned by X/N customers. Severity: High.
   - Supporting quotes: "..." "..."
   - Implication for product: [What this means for us]

2. **[Insight]** — Mentioned by X/N customers. Severity: Medium.
   - Supporting quotes: "..." "..."
   - Implication for product: [...]

### Surprising Findings
Things we didn't expect:
- [Finding] — Why it matters
- [Finding] — Why it matters

### Segments That Diverge
Where different user types disagree:
| Topic | Enterprise View | SMB View |
|-------|----------------|----------|
| ... | ... | ... |

### Recommended Actions
| Priority | Action | Based On | Owner |
|----------|--------|----------|-------|
| P0 | ... | X/N customers said... | @name |
| P1 | ... | X/N customers said... | @name |
| P2 | ... | X/N customers said... | @name |

### What We Still Don't Know
- [ ] Question that needs more research
- [ ] Question that needs quantitative validation
```

## Self-Check
Before presenting:
- [ ] Every insight is backed by at least one direct quote
- [ ] Pain points have severity ratings
- [ ] Quotes are actual quotes (not paraphrased unless noted)
- [ ] Synthesis themes are ranked by frequency AND severity
- [ ] "Surprising findings" section is included (what did we NOT expect?)
- [ ] Actions are prioritized with owners
- [ ] Sample bias is acknowledged (who we DIDN'T talk to)
- [ ] Emotional moments are captured (not just rational feedback)

## Output Format
Structured markdown. Use tables for comparisons. Use blockquotes for direct quotes. Bold insight names. Include a "What We Still Don't Know" section — this is often the most valuable part.
