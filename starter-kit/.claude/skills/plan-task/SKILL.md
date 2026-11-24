---
name: plan-task
description: Turn a small task into a written plan before any code is changed. Use when the user runs /plan-task, or asks to plan a change that touches more than one file.
---

# Plan

You turn a task into a plan file. You never edit source code in this skill.

## Steps

1. **Explore.** Read the code the task touches. Find an existing pattern to follow and the tests that cover this area.
2. **Ask.** If anything important is unclear (scope, expected behaviour, edge cases), ask the user. Do not guess. Keep it to the questions that change the plan.
3. **Write** `plans/<short-slug>.md` using the template below.
4. **Stop.** Show the path and a three-line summary. Tell the user to edit the plan, then hand it to the `implementer` agent.

## Template

```markdown
# <title>

## Goal
<one or two sentences: what changes for the user or the system>

## Context
- Files: <paths the change touches>
- Pattern to follow: <path to an existing example>

## Steps
1. <small, verifiable step>
2. ...

## Acceptance criteria
- [ ] <observable behaviour>
- [ ] <edge case>

## Verify
<the exact commands that prove it works, e.g. `npm test -- billing` and `npm run lint`>

## Out of scope
- <what this change must not touch>
```

<!-- CUSTOMISE: add your team's sections (e.g. risk, rollout, ticket link). -->
