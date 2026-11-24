# Lab 7 · Long-running work (15 min)

## /goal

1. On your branch, find (or make) a state with a few failing tests or lint errors.
2. Run:
   ```text
   /goal all tests in <folder> pass and <lint command> exits with no errors
   ```
3. Watch Claude keep working after each turn. Check progress with `/goal`. Stop it with `/goal clear` if it goes off track.

The model that checks the goal cannot run commands: it only reads the conversation. Name the command in the goal so Claude runs it and the output is visible.

Write goals a command can prove. "Make the code cleaner" is not a goal; "`npm run lint` exits 0" is.

## /loop (demo, optional to try)

```text
/loop 5m check the latest CI run for this branch and tell me if it failed
```

Without an interval, Claude chooses the wait itself (1 minute to 1 hour). To stop a self-paced loop, press `Esc` while it waits; it also ends by itself when Claude finishes a turn without scheduling the next one. A fixed-interval loop like the one above does not stop on `Esc` or `Ctrl+C`: open `/tasks`, select it and press `x`, or ask Claude to cancel it. Recurring loops run for up to 30 days while the session stays open.

**Done when:** a `/goal` reached its condition, or you can explain why it could not.
