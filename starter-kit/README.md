# Starter kit: plan → implement → review

A small, local workflow for Claude Code: write a plan, implement it, review the diff against it. No GitHub issues, no PRs, nothing is pushed. The plan file plays the role of the ticket.

## What's inside

| File | What it does |
|---|---|
| `.claude/settings.json` | Turns off the Claude attribution on commits and PRs, allows safe git commands, blocks `git push` and reading `.env` files |
| `.claude/skills/plan-task/SKILL.md` | `/plan-task <task>` explores the code and writes `plans/<slug>.md` |
| `.claude/agents/implementer.md` | Implements one plan, runs its checks, commits locally |
| `.claude/agents/reviewer.md` | Read-only review of the diff against the plan |

## Install

Copy `.claude/` into the root of your repo. If the repo already has a `.claude/` folder, merge by hand: don't overwrite the team's `settings.json`, add these keys to it.

Add `plans/` to `.gitignore` if you don't want plans committed.

The `permissions.allow` entries only apply once the folder is trusted: open `claude` there interactively once and accept the trust dialog.

The `deny` rules apply in every permission mode, auto mode included. They match the command the way Claude usually writes it (`git push ...`, also inside `cd x && git push`), but not every spelling: `git -C . push` is not matched. They are a guard rail, not a security boundary. For a hard block, use a `PreToolUse` hook or the sandbox.

## Use

```text
/plan-task the refund total ignores discounts on partial refunds
# read and edit plans/refund-partial-discount.md
use the implementer agent on plans/refund-partial-discount.md
use the reviewer agent on plans/refund-partial-discount.md
```

## Make it yours

Every file has a `CUSTOMISE` comment. Good first changes:

- Add your real test and lint commands to the allowlist in `settings.json`
- Add your team's sections to the plan template
- Add your review checklist to the reviewer
- Add a `Stop` hook that runs the tests, so a check runs even when Claude forgets
