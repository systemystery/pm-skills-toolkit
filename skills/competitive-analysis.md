---
name: competitive-analysis
description: Use when the user asks to analyze competitors, do competitive research, compare products, or assess the competitive landscape.
tools: [web-search, firecrawl]
---

# Competitive Analysis Skill

## Trigger
When the user asks for competitive analysis, competitor research, market landscape, or product comparison.

## Instructions

### Phase 1: Define the Arena
Ask the user (or extract from context):
1. **What product/feature are we analyzing?** 
2. **Who are the known competitors?** (Direct + indirect)
3. **What dimensions matter most?** (Pricing, features, UX, market position, tech stack)
4. **Who is the audience for this analysis?** (Board deck vs. team strategy vs. PM decision)

### Phase 2: Research Framework
For each competitor, build this profile:

```markdown
## [Competitor Name]

### Overview
- **Founded**: Year | **HQ**: Location | **Funding**: $X (Series Y)
- **Target customer**: [Segment]
- **Positioning**: [Their one-liner / value prop]
- **Estimated scale**: [Users, revenue, team size if available]

### Product Analysis
| Dimension | Their Approach | Strength/Weakness |
|-----------|---------------|-------------------|
| Core feature | ... | ✅/⚠️/❌ |
| Pricing | ... | ✅/⚠️/❌ |
| UX/Design | ... | ✅/⚠️/❌ |
| Integrations | ... | ✅/⚠️/❌ |
| AI/ML capabilities | ... | ✅/⚠️/❌ |

### Recent Moves
- [Date]: [What they shipped/announced]
- [Date]: [What they shipped/announced]

### What They Do Better
- ...

### Where They Fall Short
- ...
```

### Phase 3: Comparative Matrix
Build a feature-by-feature comparison:

```markdown
## Feature Comparison Matrix

| Feature | Us | Competitor A | Competitor B | Competitor C |
|---------|---:|:----------:|:----------:|:----------:|
| Feature 1 | ✅ | ✅ | ❌ | ⚠️ |
| Feature 2 | ❌ | ✅ | ✅ | ✅ |
| Pricing (per seat) | $X | $Y | $Z | $W |
```

### Phase 4: Strategic Insights
Don't just list features — derive insights:

1. **Where we win**: Our clear advantages
2. **Where we lose**: Honest gaps to address
3. **Emerging threats**: What competitors are building next
4. **Opportunity gaps**: What NO ONE is doing well
5. **Recommended actions**: 3-5 specific moves, prioritized

### Phase 5: Tailor the Output
- **For a board deck**: Lead with market position and strategic implications
- **For the team**: Lead with feature gaps and actionable recommendations
- **For a PM decision**: Lead with differentiation opportunities

## Self-Check
Before presenting:
- [ ] At least 3 competitors analyzed (direct + indirect)
- [ ] Every claim has a source or is clearly marked as estimate
- [ ] Includes both strengths AND weaknesses of competitors (not just threats)
- [ ] Feature matrix uses consistent rating system
- [ ] Strategic insights go beyond feature comparison
- [ ] Recommendations are specific and actionable (not "improve our product")
- [ ] Recent moves are from the last 6 months
- [ ] Output is tailored to the stated audience

## Output Format
Structured markdown with tables, emoji ratings (✅/⚠️/❌), and a clear "So What?" section at the end with prioritized recommendations.
