---
description: Daily review — what was built/learned today, what's next
argument-hint: [optional notes]
---

Generate today's daily review. This closes the day and sets up tomorrow.

## Steps

1. **Observe** — run `python3 ~/agentic-os/observe/dashboard.py today` to get usage/cost data.

2. **Vault scan** — check what files were modified today in `~/vault/` using Bash: `find ~/vault -newer ~/vault/master-index.md -type f 2>/dev/null | head -20`

3. **Session log** — summarize what was accomplished based on observe data and user context.

4. **User notes** — incorporate `$ARGUMENTS` if provided.

## Output format

```
# Daily Review — [DATE]

## Built / Completed
...

## Learned
...

## API Usage Today
[observe output]

## Open Loops
...

## Tomorrow's Priorities
1.
2.
3.
```

Save to `~/vault/output/review-[DATE].md`.
