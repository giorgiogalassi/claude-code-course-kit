# Lab 3 · Driving a session (20 min)

1. **Context.** Run `/context`. Pull a big source file into context with `@` (e.g. `explain @src/path/to/big-file`), then run `/context` again. What changed? On a 1M-token window the percentage moves little: look at the **Messages** line. If you only *ask* Claude to read a huge file, it may sensibly count or grep it instead of loading it.
2. **Interrupt.** Give it a broad task ("refactor this module"). Press `Esc` after a few steps and redirect: "stop, only rename the function, nothing else."
3. **Rewind.** Let it make a small edit. Then, with an empty prompt, press `Esc Esc` (or run `/rewind`) and choose **Restore code** to go back to before the edit.
4. **Permissions.** Run `/permissions` → **Add a new rule…** and allow two commands you use all the time, e.g. `Bash(npm test *)`. When asked where to save it, choose **Project settings (local)**, not the team's checked-in settings. Then ask Claude to run one: no prompt should appear.
5. **Reset.** Run `/clear`. Notice that Claude no longer knows what you just did.

**Done when:** you have used `Esc`, `/rewind`, `/context` and `/clear` at least once each.
