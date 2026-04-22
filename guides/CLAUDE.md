# Guides Directory Index

This folder contains best-practice guides for getting the most out of the PM Skills Toolkit and AI tools in general.

## Files

| File | What It Covers | When to Read |
|------|---------------|-------------|
| `prompting-guide.md` | Three tiers of prompting (basic → proposal → full plan), power prompts, ask-user-questions tool, sub-agent delegation, context monitoring | When you want better AI output quality |
| `context-management.md` | 3-tier token loading system, failure modes that burn context, sub-agent pattern, context budgeting | When Claude feels slow, forgetful, or you're hitting usage limits |

## Key Concepts
- **Lightweight alignment**: Add "give me a proposal first" to any prompt — 30 seconds saves 30 minutes
- **Sub-agents**: Delegate research to separate instances — uses 0.5% context instead of 10%
- **CLI over MCP**: CLIs have zero context overhead; MCPs eat context just by existing
