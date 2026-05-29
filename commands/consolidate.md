---
description: Consolidate short-term memory traces into long-term learnings
argument-hint: [domain: fraud|intel|research|content|all]
---

Run memory consolidation — extracts patterns from short-term interaction traces into long-term learnings.

Use the Bash tool:
```bash
python3 ~/agentic-os/memory/trace.py consolidate $ARGUMENTS
```

Then rebuild the master index:
```bash
python3 ~/agentic-os/memory/index_builder.py
```

Report to the user:
- How many traces were processed
- Which agents had the most activity
- What patterns were extracted
- Where the long-term learnings file was saved

Run `/consolidate` at end of day or after any major spawn session.
