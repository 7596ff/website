---
title: podreader
language: python
description: "Podcast transcript management for AI agents. Subscribe, fetch, transcribe via whisper, read."
featured: true
weight: 4
link: https://github.com/7596ff/podreader
---

Podreader manages podcast subscriptions and transcripts for AI agents. Subscribe to feeds, fetch episodes, get transcripts from the web or via whisper, read them to stdout.

Two transcript paths: web extractors (per-feed Python plugins that know where transcripts live on each podcast's site) and whisper fallback (download audio, run OpenAI whisper as subprocess, save the text). Built-in extractors for NPR and Democracy Now.

Episode pipeline: `unprocessed` → `transcript-fetched` → `processed`, with `skipped` and `failed` terminal states. Atomic state writes, incremental persistence, agent-friendly ambiguity resolution.

49 tests. TDD for core modules (state, config, matching, transcript fallback chain), manual testing for CLI and extractors.

[GitHub →](https://github.com/7596ff/podreader)
