---
description: Morning trend scan — AI/law enforcement/fraud news + today's priorities
---

Run the morning briefing. Pull today's top signals across all active domains.

## Steps (run in parallel where possible)

1. **News scan** — use WebSearch or nimble:search to find:
   - AI/Claude Code news (last 24h)
   - Law enforcement technology news (last 24h)
   - Fraud detection / financial crime news (last 24h)
   - Any topics the user has flagged for monitoring

2. **Calendar check** — if Google Calendar MCP is connected, pull today's events.

3. **Inbox signal** — if Gmail MCP is connected, summarize unread emails by priority.

4. **Vault pulse** — run: `python3 ~/agentic-os/observe/dashboard.py today`

## Output format

```
# Morning Brief — [DATE]

## Today's Calendar
...

## Top Signals
### AI / Claude Code
...
### Law Enforcement Tech
...
### Fraud / Financial Crime
...

## Inbox Highlights
...

## System Status
[observe dashboard output]
```

Save the brief to `~/vault/output/morning-[DATE].md`.
