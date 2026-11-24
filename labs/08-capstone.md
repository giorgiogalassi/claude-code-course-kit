# Lab 8 · Capstone: your own workflow (35 min)

1. Copy `starter-kit/.claude/` into your repo root. If `.claude/` exists, merge by hand.
2. In `.claude/settings.json`, add your test and lint commands to `permissions.allow`.
3. Pick a small real task and run:
   ```text
   /plan-task <task>
   ```
4. Read and edit the plan file in `plans/`.
5. `use the implementer agent on plans/<file>.md and let it commit`. Without "let it commit", Claude may tell the agent not to commit, because it commits only when you ask.
6. `use the reviewer agent on plans/<file>.md`
7. **Make it yours:** change one thing in the kit (plan template, review checklist, a `Stop` hook that runs tests…).
8. Check your commit has no Claude co-author line: `git log -1`.

**Done when:** one task went plan → implement → review in your repo, and you changed the kit at least once.
