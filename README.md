# Claude Agentic Skills

A collection of custom **slash commands** and **subagents** for [Claude Code](https://claude.com/claude-code) — built and used daily across law-enforcement, fraud, intelligence, content, and emergency-management work. Free to use, adapt, and build on.

Built by an Army Ranger combat veteran working in fraud detection, intelligence analysis, and applied AI. If these are useful, **follow along** — more get added as the system grows.

---

## What's inside

### Slash commands (`commands/`)
Drop into `~/.claude/commands/`. Invoke with `/name`.

| Command | What it does |
|---|---|
| `/morning` | Morning trend scan — AI/news + today's priorities |
| `/review` | Daily review — what was built/learned, what's next |
| `/research` | Deep research — multi-source synthesis with citations |
| `/intel` | Intelligence analysis — OSINT, threat assessment, pattern of life |
| `/fraud` | Fraud detection — check fraud, identity theft, financial-crime patterns |
| `/lawpractice` | Law-enforcement best practices — tactics, policy, investigations |
| `/content` | Content creation — scripts, posts, articles, social |
| `/deck` | Slide-deck builder for training/briefings |
| `/compwatch` | Competition watch — track competitors and market moves |
| `/spawn` | Dynamic agent spawner with scoring + handoff |
| `/supersane` | Council of 3 — ask multiple AIs in parallel, synthesize* |
| `/observe` | Observability — usage/cost dashboard* |
| `/query` · `/ingest` · `/index` | RAG memory — search / add / rebuild index* |
| `/consolidate` | Consolidate short-term notes into long-term learnings |
| `/worktree` | Git worktree helper for parallel agent workspaces |

\* These call a local backend (observability + RAG + multi-AI). The build for that lives in the companion repo **[agentic-os-blueprint](https://github.com/hatchet11/agentic-os-blueprint)** — a sanitized, step-by-step build you can follow.

### Subagents (`agents/`)
Drop into `~/.claude/agents/`.

| Agent | Role |
|---|---|
| `research-analyst` | Deep research & literature synthesis |
| `intel-analyst` | OSINT, threat assessment, link analysis |
| `fraud-investigator` | Check/wire fraud, identity theft, financial crime |
| `content-creator` | YouTube, social, articles, decks |
| `geo-*` (5) | Generative-Engine-Optimization audit suite |
| `unit-tester` | Restricted test-runner agent |

---

## Install

```bash
git clone https://github.com/hatchet11/claude-agentic-skills.git
cp claude-agentic-skills/commands/*.md ~/.claude/commands/
cp claude-agentic-skills/agents/*.md   ~/.claude/agents/
```

Then in Claude Code, type `/` to see the commands, or let Claude pick agents automatically.

> **Note:** All paths in these files use `~/...` placeholders and `<...>` for keys/emails. Adjust to your environment. No personal data, keys, or proprietary content is included.

---

## Skills I use but did NOT republish here (credit where due)

These are excellent third-party skills I rely on — get them from the source rather than from me:

- **[Anthropic Skills](https://github.com/anthropics/skills)** — `pdf`, `docx`, `pptx`, `xlsx`, artifact builders, and more.
- **[awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)** — a large community catalog (file-organizer, invoice-organizer, changelog-generator, mcp-builder, and others).

---

## Contributing & following

PRs welcome — see `CONTRIBUTING.md`. Star the repo and follow [@hatchet11](https://github.com/hatchet11) to get new skills as they drop.

## License

MIT — see `LICENSE`. Use them, ship them, make them yours.
