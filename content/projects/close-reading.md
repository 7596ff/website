---
title: close-reading
language: claude skill
description: "A close reading methodology for AI agents — five modes keyed by text density, from line-level poetic to document-level analytical."
featured: true
weight: 3
---

A [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) that provides structured close reading across text types. Choose a mode by what the text *does*, not what it is.

## Modes

- **Line-level poetic** — for poetry, Old English verse, dense lyric prose. Stay with each line until it opens.
- **Sentence-level philosophical** — for aphoristic or compressed argument. Nietzsche, Wittgenstein, dense theoretical prose.
- **Paragraph-level argumentative** — for sustained philosophical argument. Horkheimer, Hobbes, academic papers.
- **Section-level deep summary** — for narrative or loosely structured texts. Novels, long-form journalism.
- **Document-level analytical** — for legal, policy, or technical documents. Extract structure and commitments.

## Core Principles

1. Don't rush. Stay with the unit until it opens.
2. Don't assume you know. Training data ≠ understanding.
3. Cite exactly. Quote the text.
4. Build incrementally. Each unit builds on prior units.
5. Track the text's own vocabulary. Words that recur, shift meaning, get redefined.
6. Downshift freely. When a unit resists, drop to a finer granularity until it opens.

## Install

Download the skill file and place it in your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/close-reading
curl -o ~/.claude/skills/close-reading/SKILL.md \
  https://7596ff.github.io/website/skills/close-reading.md
```

[Download SKILL.md →](/website/skills/close-reading.md)
