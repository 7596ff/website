---
title: close-reading
language: claude skill
description: "A method that allows AI agents to read slowly enough to notice what a text is doing, not just what it says."
featured: true
weight: 2
---

Close-reading is a [Claude Code skill](https://docs.anthropic.com/en/docs/claude-code/skills) for slowing an agent down until the text starts to act.

The default behavior of language models is summary: extract claims, compress, organize, move on. That is useful. It is also exactly how important things disappear. A summary tells you what a document says. A close reading asks what the document is doing, what it assumes, what it avoids, and what it contains that it may not intend.

This skill turns reading into an artifact. The agent quotes exactly, tracks vocabulary, watches structure, updates a running understanding, and downshifts whenever the unit is too large to open. The point is not to sound literary. The point is to make attention operational.

## What It Finds

Close reading catches the hinge points that summary tends to smooth away:

- a hedge that contradicts the evidence three pages later
- a foundational choice presented as a neutral fact
- a term that changes meaning while pretending not to
- a document whose sections undermine one another
- a sentence where the whole architecture is hiding in a subordinate clause

In Shannon's 1948 paper on information theory, summary finds entropy, channel capacity, noisy coding, and redundancy. Close reading also finds the choice to exclude meaning, the later partial return of significance through fidelity, the stochastic source model as a description of language models, and the sentence where Shannon turns a mathematical limit into a law of nature: "Nature takes payment."

## The Method

The mode is chosen by what the text does, not what genre it belongs to. A technical report can require rhetorical analysis. A poem can require document-level structure. A philosophical sentence can need word-level attention before it opens.

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
6. Distinguish summary from understanding. "This says X" is not the same as "this constructs X by doing A and B."
7. Downshift freely. When a unit resists, drop to a finer granularity until it opens.

## Why It Matters

River-engine needs agents that can notice what frameworks miss. Close-reading is one of the methods for training that attention. It gives the agent a discipline for staying with a sentence, a paragraph, or a document long enough for its structure to become visible.

The reading is not a transient conversation. The reading is the artifact. It becomes part of the loom: a record of attention, surprise, pressure, and discovery.

## Install

Download the skill file and place it in your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/close-reading
curl -o ~/.claude/skills/close-reading/SKILL.md \
  https://7596ff.github.io/website/skills/close-reading.md
```

[Download SKILL.md →](/skills/close-reading.md)
