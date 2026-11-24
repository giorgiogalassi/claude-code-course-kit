# Lab 2 · The agent loop (20 min)

Goal: see Claude gather context, act and check, instead of just answering.

1. Open Claude Code in the root of your repo, in manual mode: `claude --permission-mode default`
2. Ask, one at a time:
   - "Give me an overview of this codebase: main modules and how they talk to each other."
   - "How are the tests organised, and how do I run them?"
   - "Trace what happens when <a real user action> happens, from the entry point to the database/API."
3. While it works, watch **which tools** it calls and **which files** it reads.
4. Pick one claim you are not sure about and ask: "Show me the file and lines that prove this."

**Done when:** you have seen at least one answer that Claude backed with a file it read, and one you corrected.
