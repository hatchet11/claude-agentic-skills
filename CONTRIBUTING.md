# Contributing

Contributions welcome — new commands, new agents, or improvements to existing ones.

## Ground rules
1. **No secrets, no PII, no proprietary data.** Use `~/...` for paths and `<PLACEHOLDER>` for keys/emails/tokens. PRs containing real credentials will be rejected.
2. **One skill per file.** Commands go in `commands/`, agents in `agents/`. Use clear YAML frontmatter (`description`, `argument-hint` for commands).
3. **Keep it general.** A skill others can use beats one hardwired to your machine.
4. **Credit upstream.** If your skill adapts someone else's work, link it.

## How
1. Fork, branch, add your `.md` file.
2. Test it in your own `~/.claude/commands` or `~/.claude/agents`.
3. Open a PR with a one-line description and an example invocation.

## Ideas wanted
- More investigative/OSINT commands
- Reporting and briefing generators
- Cost-aware routing helpers
- Memory/RAG utilities

Star the repo and follow [@hatchet11](https://github.com/hatchet11) if you build on these.
