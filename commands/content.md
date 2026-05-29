---
description: Content creation — YouTube scripts, Skool posts, articles, social media
argument-hint: <platform> <topic> [tone: professional|casual|tactical]
---

Create content for: `$ARGUMENTS`

Parse the platform and topic from the arguments. Default tone: direct and authoritative.

## Platforms

**YouTube script** — hook (0-15s) + value ladder + CTA. Format as timestamped script with B-roll notes.

**Skool post** — community-optimized, value-first, engagement hook at end. 150-300 words.

**LinkedIn** — professional, credibility-driven, 3-5 paragraphs + hook line.

**Twitter/X thread** — hook tweet + 5-8 tweet thread, each tweet standalone-worthy.

**Blog/article** — SEO-aware, H2 structure, 800-1500 words.

**Slide deck outline** — title + 8-12 slide stubs with speaker notes.

## Process

1. Check vault for existing research: `python3 ~/agentic-os/memory/query.py "[topic]"`
2. If SuperSane is needed for multi-perspective content, call: `python3 ~/supersane/supersane.py "[prompt]"`
3. Draft content
4. Save draft to `~/vault/content/[platform]-[DATE]-[slug].md`

## Domains to draw from
Law enforcement | Fraud detection | Intelligence | AI/Claude Code | Leadership | Veteran perspective | Cybersecurity
