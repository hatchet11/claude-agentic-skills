---
description: Add a file, URL, or pasted text to the vault RAG system
argument-hint: <file path | URL | --text "content">
---

Ingest content into the vault RAG system so it becomes queryable via `/query`.

Use the Bash tool to run:
```
python3 ~/agentic-os/memory/ingest.py $ARGUMENTS
```

After ingestion, print the output and confirm how many chunks were created. If the user pasted raw text without a path, use: `--text "content" --title "descriptive title"`.
