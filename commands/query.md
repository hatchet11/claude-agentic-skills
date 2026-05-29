---
description: RAG search the vault — finds relevant chunks from ingested documents
argument-hint: <question or topic>
---

Search the vault RAG system for content related to `$ARGUMENTS`.

Use the Bash tool to run:
```
python3 ~/agentic-os/memory/query.py $ARGUMENTS
```

Print the full output. If results are found, summarize the top 3 in plain language and note the source documents. Save noteworthy findings as a follow-up with `/ingest`.
