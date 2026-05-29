---
description: Deep research — multi-source synthesis with citations, saved to vault
argument-hint: <research question>
---

Conduct deep research on: `$ARGUMENTS`

## Process

1. **Vault first** — run `python3 ~/agentic-os/memory/query.py "$ARGUMENTS"` to check existing knowledge.

2. **Web research** — use nimble:search or WebSearch for:
   - Primary sources (gov, academic, official)
   - Recent news (last 30 days)
   - Expert commentary

3. **Synthesis** — structure findings:
   - What is known with HIGH confidence
   - What is known with MODERATE confidence  
   - What is contested / unknown
   - Key sources (cited inline)

4. **Output** — produce a research note in this format:

```markdown
# Research: [topic]
Date: [DATE]
Query: $ARGUMENTS

## Summary (3-5 sentences)

## Key Findings
1. ...
2. ...

## Sources
- [title](url) — annotation

## Gaps & Follow-up Questions

## Saved to vault
```

5. **Save** — write to `~/vault/output/research-[DATE]-[slug].md`, then ingest: `python3 ~/agentic-os/memory/ingest.py [file]`
