---
title: river-engine
language: rust
description: "Distributed agent orchestration system. Rooms with walls, agents with bodies, safety as architecture."
featured: true
weight: 1
link: https://github.com/7596ff/river-engine
---

River-engine is a distributed agent orchestration system built on the principle that safety should be architectural, not rule-based. Each human gets a room containing an agent that works, a bystander that watches, and the human who decides.

The system is built around the concept of *con-scientia* — knowing-together. The agent and human form a cognitive unit: the human brings judgment and embodiment, the agent brings memory and persistence. Together they produce something neither could alone.

## Architecture

- **Orchestrator** — manages agent lifecycles, spawns gateway processes
- **Gateway** — per-agent process handling model inference, tool execution, and spectator observations
- **Adapters** — pluggable communication channels (Discord, TUI, HTTP)
- **Workspace** — git-hosted identity and memory files that persist across sessions

## Tech

Rust workspace with 7 crates. Ollama/OpenAI-compatible model inference. SQLite for conversation history. Redis for inter-process communication.

[GitHub →](https://github.com/7596ff/river-engine)
