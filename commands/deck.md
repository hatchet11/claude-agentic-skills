---
description: Slide deck builder — law enforcement, fraud, intelligence, tactical training decks
argument-hint: <topic> [audience: patrol|investigators|command|public] [slides: N]
---

Build a slide deck on: `$ARGUMENTS`

Parse: topic, audience (default: investigators), slide count (default: 15).

## Deck Structure

1. **Title slide** — topic, presenter placeholder, date
2. **Agenda** — 4-6 agenda items
3. **Content slides** — each with:
   - Slide title
   - 3-5 bullet points (presentation-density, not essay)
   - Speaker notes (2-3 sentences expanding the slide)
   - Suggested visual/graphic description
4. **Case study / scenario** — real or composite example
5. **Legal/policy basis** — statutes, case law, department policy hooks
6. **Key takeaways** — 3-5 action items
7. **Resources slide** — further reading, contacts, forms
8. **Q&A / Discussion**

## Domain expertise to apply
- Law enforcement: constitutional law, use of force, documentation, Brady
- Fraud: detection methods, red flags, financial forensics, prosecution prep
- Intelligence: analytical standards, source handling, product dissemination
- Tactical: threat assessment, scene management, officer safety

## Output

Produce the full deck outline in markdown, then offer to:
- Generate as PPTX via `/pptx` skill
- Save outline to `~/vault/slide-decks/[topic]-[DATE].md`
- Ingest into RAG for future reference
