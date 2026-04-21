<div align="center">

# 🧰 PM Skills Toolkit

### Drop-in AI skills for product managers — works with Claude Code, Cursor, Windsurf, and any AI coding tool.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Compatible-blueviolet)](https://claude.ai)
[![Cursor](https://img.shields.io/badge/Cursor-Compatible-orange)](https://cursor.com)

**Stop writing PRDs from scratch. Stop reinventing sprint plans. Start compounding.**

[Quick Start](#-quick-start) · [Skills](#-skills) · [Templates](#-templates) · [Workflows](#-workflows) · [Contributing](#-contributing)

</div>

---

## 🤔 Why This Exists

Most PMs use AI like a chatbot — type a prompt, get a mediocre response, spend an hour fixing it.

The top 1% use **skills** — reusable instruction sets that turn AI into a domain expert for specific PM tasks. Every skill in this repo is:

- **Battle-tested** across real FinTech, SaaS, and marketplace products
- **Multi-tool compatible** — works in Claude Code, Cursor, Windsurf, or any AI IDE
- **Opinionated** — not generic templates, but specific methodologies that actually work
- **Compounding** — each skill builds on shared knowledge and improves over time

> *"The difference between a PM who uses AI and a PM who is 10x more effective with AI is the quality of their skills."*

---

## ⚡ Quick Start

### Option 1: Clone the whole toolkit

```bash
git clone https://github.com/systemystery/pm-skills-toolkit.git
cd pm-skills-toolkit
```

### Option 2: Copy individual skills

Browse the `/skills` folder and copy any `.md` file into your own `.claude/skills/` or project directory.

### Option 3: Use with your AI tool

**Claude Code:**

```bash
# Copy skills to your project
cp -r skills/ your-project/.claude/skills/
```

**Cursor:** The `.cursorrules` file at the root automatically loads the toolkit context.

**Windsurf:** The `.windsurfrules` file at the root automatically loads the toolkit context.

---

## 🛠 Skills

Each skill is a standalone markdown file with clear trigger conditions, instructions, and self-checking steps.

| Skill | What It Does | When to Use |
|-------|-------------|-------------|
| [PRD Writer](skills/prd-writer.md) | Generates a structured PRD from a problem statement | Starting any new feature |
| [Competitive Analysis](skills/competitive-analysis.md) | Deep competitor research with framework | Strategy planning, board decks |
| [User Interview Synthesizer](skills/user-interview-synthesizer.md) | Extracts insights from call transcripts | After customer calls |
| [OKR Generator](skills/okr-generator.md) | Creates measurable OKRs from strategy | Quarterly planning |
| [Launch Checklist](skills/launch-checklist.md) | Pre/post launch verification | Before any release |
| [Stakeholder Brief](skills/stakeholder-brief.md) | Tailored communication per audience | Cross-functional updates |
| [Metrics Dashboard Spec](skills/metrics-dashboard.md) | Defines KPIs and dashboard structure | New feature instrumentation |
| [Sprint Planning](skills/sprint-planning.md) | Generates sprint plans from backlog | Sprint ceremonies |
| [A/B Test Designer](skills/ab-test-designer.md) | Experiment design with stats rigor | Growth experiments |
| [Roadmap Builder](skills/roadmap-builder.md) | Visual roadmap from priorities | Stakeholder alignment |

---

## 📋 Templates

Ready-to-fill templates for common PM deliverables:

- [`prd-template.md`](templates/prd-template.md) — Problem-first PRD structure
- [`okr-template.md`](templates/okr-template.md) — OKR with leading/lagging indicators
- [`launch-email-template.md`](templates/launch-email-template.md) — Internal launch announcement
- [`retro-template.md`](templates/retro-template.md) — Sprint retrospective with action items
- [`one-pager-template.md`](templates/one-pager-template.md) — Executive one-pager for quick alignment

---

## 🔄 Workflows

Multi-step processes that chain skills together:

- [`daily-standup.md`](workflows/daily-standup.md) — Morning context load + priorities
- [`weekly-synthesis.md`](workflows/weekly-synthesis.md) — Cross-project status rollup
- [`quarterly-planning.md`](workflows/quarterly-planning.md) — Strategy → OKRs → Roadmap pipeline

---

## 📂 Repo Structure

```
pm-skills-toolkit/
├── README.md                    ← You are here
├── CLAUDE.md                    ← Claude Code configuration
├── .cursorrules                 ← Cursor configuration
├── .windsurfrules               ← Windsurf configuration
├── LICENSE                      ← MIT License
├── skills/
│   ├── prd-writer.md
│   ├── competitive-analysis.md
│   ├── user-interview-synthesizer.md
│   ├── okr-generator.md
│   ├── launch-checklist.md
│   ├── stakeholder-brief.md
│   ├── metrics-dashboard.md
│   ├── sprint-planning.md
│   ├── ab-test-designer.md
│   └── roadmap-builder.md
├── templates/
│   ├── prd-template.md
│   ├── okr-template.md
│   ├── launch-email-template.md
│   ├── retro-template.md
│   └── one-pager-template.md
├── workflows/
│   ├── daily-standup.md
│   ├── weekly-synthesis.md
│   └── quarterly-planning.md
└── examples/
    ├── fintech-prd-example.md
    └── saas-okr-example.md
```

---

## 🏗 How Skills Work

Each skill follows the same structure:

```markdown
---
name: skill-name
description: When this skill should be triggered
tools: [optional tools needed]
---

# Skill Name

## Trigger
When the user asks to [specific action]...

## Instructions
1. Step-by-step process
2. With specific methodology
3. Not generic advice

## Self-Check
Before presenting output:
- [ ] Verify against these criteria
- [ ] Double-check these assumptions
- [ ] Ensure this quality bar

## Output Format
[Exact structure of the deliverable]
```

The **self-check** section is what separates great skills from mediocre ones. It forces the AI to validate its own work before showing you — like having a junior PM who proofreads before hitting send.

---

## 🧠 Philosophy

This toolkit is built on three principles from operating PM OS systems in production:

1. **Skills > Prompts.** A prompt is used once. A skill compounds forever.
2. **Opinionated > Generic.** "Write a PRD" produces garbage. "Write a PRD using the problem-first framework with these specific sections" produces work you'd actually ship.
3. **Self-checking > Trust.** Every skill validates its own output. The builder-validator pattern catches 80% of issues before you even see the result.

---

## 🤝 Contributing

Found a skill that could be better? Built one for your team? PRs are welcome.

1. Fork this repo
2. Add your skill to `/skills` following the skill structure above
3. Add an example to `/examples` if applicable
4. Submit a PR with a description of what the skill does and why it's useful

---

## 📚 Inspired By

- [Carl Vellotti's Product OS](https://github.com/carlvellotti/carls-product-os) — Pioneer of the personal PM OS
- [Hannah Stulberg's Team OS](https://github.com/in-the-weeds-hannah-stulberg/team-os-example-repo) — Scaling AI across product teams
- [Aakash Gupta's PM OS](https://www.news.aakashg.com/p/pm-os) — The most comprehensive PM setup guide

---

## 📄 License

MIT — use it, fork it, make it yours.

---

<div align="center">

**Built by [Nimish Singhal](https://productnarrative.github.io) · [Product Narrative](https://productnarrative.substack.com/)**

*If this saves you even one hour, star the repo ⭐*

</div>
