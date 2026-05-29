---
description: Git worktree helper — create parallel agent workspaces for simultaneous tasks
argument-hint: create <branch> [base] | list | status | remove <branch>
---

Manage git worktrees so two Claude Code agents can work on different branches simultaneously without blocking each other.

Use the Bash tool to run:
```bash
bash ~/agentic-os/architecture/worktree.sh $ARGUMENTS
```

## Common workflows

**Start a parallel task:**
```
/worktree create feature/my-task main
```
Then open a NEW Claude Code terminal session in that folder and work there independently.

**Check what's running in parallel:**
```
/worktree status
```

**Clean up when done:**
```
/worktree remove feature/my-task
```

## Why worktrees
- Each Claude Code session gets its own isolated branch — no conflicts
- Both agents can write files, run tests, build — fully independent
- Merge when done, or cherry-pick what you want
- No stashing, no branch switching, no "wait for the other task to finish"

Print the full output and guide the user on next steps.
