# From Chatbot to Agent: Developing with Claude Code

A hands-on course for developers who use Claude Code like a chatbot, or have not used it yet. You work on a local branch of your own repo: Claude proposes, you approve every change. Nothing is pushed.

This edition: **two days, online** · Claude Code 2.1.331 · release `2026-11-25`.

## Start here

**Before the course:** do [`labs/00-setup.md`](labs/00-setup.md): install, a throwaway branch, your test command, manual mode. Problems found at home are cheaper than problems found in the session.

| Day | Modules | Labs |
|---|---|---|
| **Day 1** · ~2h20 | 0 Chatbot vs agent · 1 How an LLM behaves · 2 The agent loop · 3 Driving a session · 4 Explore → Plan → Implement → Verify → Commit | [02](labs/02-agent-loop.md) · [03](labs/03-driving.md) · [04](labs/04-full-loop.md) |
| **Day 2** · ~2h30 | 5 CLAUDE.md · 6 Skills & subagents · 7 Long-running work (`/goal`, `/loop`) · 8 Capstone · 9 Cheat-sheet & where next | [05](labs/05-claude-md.md) · [06](labs/06-skill.md) · [07](labs/07-long-running.md) · [08](labs/08-capstone.md) |

Day 1 ends with a commit on your branch. Keep it: day 2 starts from it.

**After the course:** [`starter-kit/`](starter-kit/) is a small plan → implement → review workflow: a `/plan-task` skill, an implementer and a reviewer subagent, safe default settings. Copy it into your repo and make it yours; lab 8 walks you through it.

**No repo to practise on?** [claude-code-course-sandbox](https://github.com/giorgiogalassi/claude-code-course-sandbox) is a small online shop with one branch per lab (`lab-02` … `lab-08`). Each branch starts where that lab starts, with the earlier labs already done. There's a ZIP per branch if you can't clone from GitHub.

## What's here

| | What |
|---|---|
| [`slides.pdf`](slides.pdf) | The slides of this edition |
| [`labs/`](labs/) | One README per hands-on exercise |
| [`starter-kit/`](starter-kit/) | The workflow you copy into your repo in lab 8 |
| [sandbox repo](https://github.com/giorgiogalassi/claude-code-course-sandbox) | A practice repo for every lab, one branch per lab |

Claude Code changes fast. If a command or a screen looks different on your machine, check https://code.claude.com/docs first.

Each edition of the course is a tag of this repo: the link you got points to the material exactly as it was taught.

## License

Starter kit: MIT. Labs and slides: CC BY 4.0. See [LICENSE](LICENSE).
