---
description: Dynamic agent spawner — pre-qualifies with numeric scoring, JSON workspace handoff DAG, metric-gated rollback, persistent learning
argument-hint: <goal description>
---

You are running `/spawn` — the multi-agent orchestrator. Goal: `$ARGUMENTS`

## Pre-Qualification (Score Before Acting)

Before spawning any agents, score the goal. Check learning history:
```bash
python3 ~/agentic-os/memory/learning_store.py report
```

Score the goal 0-100 on:
- **Clarity** (0-25): Is the goal unambiguous with defined success criteria?
- **Scope** (0-25): Can it be accomplished in ≤5 discrete sub-tasks?
- **Prior success** (0-25): Has this type of task succeeded before? (check learning store)
- **Risk** (0-25): Are any sub-tasks in the AUTO-AVOID list?

If total score < 40: clarify goal with user before proceeding.
If any subtask is AUTO-AVOID flagged: warn user, get confirmation to proceed.

## 7-Stage JSON Workspace Handoff

### Stage 1 — Strategic Plan (write strategic-plan.json)
```json
{
  "goal": "$ARGUMENTS",
  "decomposition": [
    {"id": "T1", "type": "research|analysis|synthesis|implementation|qa", "task": "...", "agent": "research-analyst|intel-analyst|fraud-investigator|content-creator|unit-tester", "depends_on": [], "score": 0}
  ],
  "success_criteria": "measurable definition of done",
  "rollback_trigger": "what metric/condition triggers revert"
}
```
Write to: `~/vault/smart-memory/spawned/strategic-plan.json`

### Stage 2 — Memory Check
```bash
python3 ~/agentic-os/memory/query.py "$ARGUMENTS"
python3 ~/agentic-os/memory/trace.py query "$ARGUMENTS"
```
Add relevant findings to strategic-plan.json as `prior_knowledge: [...]`

### Stage 3 — Agent Workspace Files
For each task, write agent file to `vault/smart-memory/spawned/[T_id]-[agent].md`:
```markdown
---
trace_id: [T_id]
agent: [agent-name]
task: "[task description]"
input_file: strategic-plan.json
output_file: [T_id]-output.json
---
[agent instructions with explicit JSON output format]
```

Each agent MUST write its output as JSON:
```json
{"status": "completed|failed", "findings": [...], "output_files": [...], "metric": null}
```

### Stage 4 — Execute (Respect Dependencies)
- Use Task tool for each agent, reading the workspace file
- Run independent tasks in parallel (no depends_on overlap)
- Pass `output_file` from upstream tasks as `input_file` to dependent tasks

### Stage 5 — Log Traces
After each agent:
```bash
python3 ~/agentic-os/memory/trace.py log --agent "[name]" --task "[task]" --status completed|failed --files "[output]"
python3 ~/agentic-os/memory/learning_store.py record --task "[task]" --agent "[name]" --status success|failure
```

### Stage 6 — Metric-Gated Rollback Check
If `rollback_trigger` was defined in the plan:
- Read all output JSON files
- Check if success_criteria was met
- If NOT met: log failure, recommend rollback, do NOT proceed with synthesis

### Stage 7 — Synthesize + Consolidate
```bash
python3 ~/agentic-os/memory/trace.py consolidate
python3 ~/agentic-os/memory/index_builder.py
```

Present: what each agent produced + integrated conclusion + vault locations + learning store update.
