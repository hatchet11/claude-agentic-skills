# Contributing to Claude Agentic Skills

Contributions are welcome — new commands, new agents, or improvements to existing ones. This project is built and used in active production work across law enforcement, fraud detection, intelligence analysis, and emergency management. Practical, field-tested contributions carry the most weight.

---

## Ground rules

1. **No secrets, no PII, no proprietary data.** Use `~/...` for paths and `<PLACEHOLDER>` for keys, emails, and tokens. PRs containing real credentials will be rejected without further review.
2. **One skill per file.** Commands go in `commands/`, agents in `agents/`. Use clear YAML frontmatter (`description`, `argument-hint` for commands).
3. **Keep it general.** A skill that works for anyone beats one hardwired to your machine or workflow. If it's inherently specialized, document that clearly.
4. **Credit upstream.** If your skill adapts someone else's work, link it. See the README for examples of skills I use but deliberately didn't republish.
5. **Test before submitting.** Install it in your own `~/.claude/commands/` or `~/.claude/agents/` and verify it works.

---

## How to contribute

1. **Fork** this repository.
2. **Create a branch** — use a short descriptive name: `add-warrant-drafter`, `improve-intel-agent`, etc.
3. **Add your file** in the appropriate folder. Follow the frontmatter format of existing skills.
4. **Test it** end-to-end in your Claude Code environment.
5. **Open a pull request** using the PR template. Include a one-line description and an example invocation.

---

## What makes a good contribution

- **Solves a real problem.** The best skills here came from actual work — an investigative need, a reporting workflow, a repetitive briefing task. If it saved you time, it will save others time.
- **Clear description and argument hint.** Claude Code uses the frontmatter to route and invoke — make it precise.
- **Idiomatic for Claude Code.** Use `$ARGUMENTS`, system prompts, and tool calls the way the platform expects. Avoid hacks that only work with specific model versions.
- **Fail gracefully.** If the user provides no arguments, the skill should explain what it needs, not error silently.

---

## Ideas wanted

- Investigative and OSINT commands
- Reporting and briefing generators (incident reports, operational summaries)
- Cost-aware model routing helpers
- Memory and RAG utilities
- Commands for the companion [agentic-os-blueprint](https://github.com/hatchet11/agentic-os-blueprint) layers

---

## Questions

Open an issue with the `question` label. No question is too basic.

Star the repo and follow [@hatchet11](https://github.com/hatchet11) if you build on these.
