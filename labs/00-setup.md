# Lab 0 · Setup (before the session)

1. Install Claude Code and log in. Check: `claude --version` (the course uses 2.1.331).
2. Pick a work repo you know. Create a local branch you can throw away:
   ```bash
   git switch -c course/<your-name>
   ```
3. Make sure you can run the tests (or the build) from the terminal. Write the command down; you will need it all day.
4. Check hooks are not disabled: `/goal` in lab 7 needs them. None of your settings files (`~/.claude/settings.json`, the repo's `.claude/settings.json` and `.claude/settings.local.json`) may set `"disableAllHooks": true`. Run `/status` to see which settings files are loaded. If hooks are disabled by your organisation, tell the instructor.

5. Since 2.1.283 a session starts in **auto mode**: Claude acts without asking. Until module 3 we work in **manual mode**, so you approve each action. Start every session with:
   ```bash
   claude --permission-mode default
   ```
   Or press `Shift+Tab` once after starting. The status bar shows `⏸ manual mode on`.
   The first time, Claude asks whether you trust the folder. The dialog also lists the settings files and hooks the folder would load: read them. The highlighted answer is **No, exit**: move down to **Yes, I trust this folder**.
   When a permission prompt offers "Yes, and switch to auto mode", pick plain **Yes** for now.
6. Keep the course's personal files out of git, locally only (`.git/info/exclude` is never committed):
   ```bash
   printf '.claude/settings.local.json\nCLAUDE.local.md\nplans/\n' >> .git/info/exclude
   ```
7. Turn off the Claude co-author line on commits for this repo. Create `.claude/settings.local.json` (merge by hand if it exists):
   ```json
   { "attribution": { "commit": "", "pr": "" } }
   ```
8. Set the editor that `Ctrl+G` opens in lab 4. The editor's command must work in a terminal first, and `--wait` makes Claude wait until you close the file. Add the export to your shell profile (`~/.zshrc` or `~/.bashrc`), then open a new terminal.
   - **VS Code:** `Cmd+Shift+P` (`Ctrl+Shift+P` on Linux) → *Shell Command: Install 'code' command in PATH*. Then `export EDITOR="code --wait"`.
   - **IntelliJ IDEA:** in the Toolbox App, *Settings → Tools → Shell scripts* on, or add the launcher folder to your `PATH` (macOS: `/Applications/IntelliJ IDEA.app/Contents/MacOS`, or `IntelliJ IDEA CE.app` for Community). Then `export EDITOR="idea --wait"`.
   - **Terminal editor:** `export EDITOR=nano` (or `vim`).

   Check: `eval "$EDITOR /tmp/x.txt"` opens the file and the terminal returns only after you close it.

**Rule for the day:** nothing gets pushed. You review and approve every change.
