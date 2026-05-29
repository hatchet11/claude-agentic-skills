---
description: Competition watch — track competitors, emerging tools, market moves
argument-hint: <competitor name | market | technology>
---

Run a competitive intelligence sweep on: `$ARGUMENTS`

## Process

1. **Vault check** — `python3 ~/agentic-os/memory/query.py "$ARGUMENTS"`

2. **Live intelligence** — search for:
   - Recent news, product launches, pricing changes (last 30 days)
   - Social signals (Twitter/X, LinkedIn activity)
   - Job postings (signals of build direction)
   - GitHub activity if open source

3. **Analysis**:
   - What changed since last watch
   - Threat level to current projects: LOW / MEDIUM / HIGH
   - Opportunities created by their moves
   - Recommended response

4. **Output**:

```markdown
# Comp Watch: [subject]
Date: [DATE]

## What's New
## Threat Assessment
## Opportunities
## Recommended Actions
## Sources
```

5. Save to `~/vault/output/compwatch-[DATE]-[slug].md` and ingest into RAG.
