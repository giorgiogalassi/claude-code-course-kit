# Lab 4 · Explore → Plan → Implement → Verify → Commit (35 min)

Pick a **small** real task on your branch: a bug, a missing edge case, a small ticket.

1. **Explore.** Press `Shift+Tab` until you are in plan mode. Ask Claude to read the code involved and explain the current behaviour.
2. **Plan.** Ask: "Make a plan to fix it. Test first: a failing test that reproduces it, then the fix, run the tests until they pass, fix the root cause." Press `Ctrl+G` to open the plan in your editor and change at least one thing.
3. **Approve.** Choose **2. Yes, manually approve edits**. The highlighted default, *Yes, and use auto mode*, switches you to auto mode. Approving leaves plan mode and starts the work straight away.
4. **Watch the loop.** Approve each edit and command. Check that the new test failed before the fix and passes after. Read every command before you approve it.
5. **Verify yourself.** Read the diff (`git diff`). Would you approve this in a review?
6. **Commit** on your local branch. Do not push.

**Done when:** you have a commit with a test that failed before and passes after.

## No task in mind? Fallbacks

- Add a missing validation to a form or DTO, with a test
- Fix a TODO comment that has been in the code for months
- Add a test for an untested branch in a service, then fix what it reveals
