# Daily Standup Workflow

## When to Use
Every morning, or at the start of your work session.

## Steps

### Step 1: Load Context
Tell your AI tool:
```
Read /tasks/current.md and my calendar for today. 
What are my priorities and what meetings do I have?
```

### Step 2: Check Project Status
```
For each project in /projects/, give me a one-line status:
- Project name: [On track / At risk / Blocked] — [Why]
```

### Step 3: Prep for Meetings
```
I have a meeting with [person] today. 
Check /knowledge/people/[name].md for context.
What should I bring up? What do I owe them?
```

### Step 4: Set Today's Focus
```
Based on my priorities and meetings, what are the 3 things 
I must accomplish today to stay on track for my OKRs?
```

### Step 5: Update Task Board
```
Update /tasks/current.md with today's priorities.
Move anything completed yesterday to done.
```

## Output
A crisp morning brief with:
- Today's top 3 priorities
- Meeting prep notes
- Blockers to resolve
- Updated task board
