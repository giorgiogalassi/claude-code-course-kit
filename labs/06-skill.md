# Lab 6 · Write one skill (25 min)

1. Think of something you explain to Claude again and again: how to add an endpoint, how to write a component, how your team names branches, how to run a migration.
2. Create `.claude/skills/<name>/SKILL.md`:
   ```markdown
   ---
   name: <name>
   description: <what it does and WHEN Claude should use it>
   ---
   1. ...
   2. ...
   ```
3. The skill should appear in the slash menu on its own. If `/<name>` doesn't show up, run `/reload-skills`; `/status` lists skill files that failed to load. Run it with `/<name>`. Then start a fresh session and describe the task *without* the slash command. Does Claude pick the skill up from the description?
4. **Subagent.** Ask: "Use a subagent to review my current diff for bugs and missed edge cases." Notice the review happens in a separate context and only the summary comes back.
5. **Optional: a cheap subagent.** Ask Claude to create `.claude/agents/test-runner.md` with `model: haiku`, `effort: low` and `maxTurns: 15`, that runs your tests and reports only the failures. Then ask: "Use the test-runner subagent."

**Done when:** your skill runs with `/<name>` and you have read one subagent review.
