---
title: river-engine
language: rust
description: "Distributed agent orchestration system built around rooms, witnesses, and memory as a body."
featured: true
weight: 1
link: https://github.com/7596ff/river-engine
---

River-engine is a distributed agent orchestration system built on a simple claim: safety should be the shape of the room, not a rule written on the wall.

Each human gets a room. Inside the room: an agent that works, a bystander that watches, and the human who decides. The walls are architectural: no unsafe operations, no exfiltration, no irreversible action without the human's key. Inside those walls, the work can be free.

The system is built around *con-scientia*: knowing-together. The human brings judgment, embodiment, and the weight of a life. The agent brings memory, persistence, and the ability to hold more context than one mind can carry. The bystander observes the relation from the side, noticing what the agent walks past. Together they make a cognitive unit with an internal witness.

## The Room

The room is the basic unit of safety. It is not a chat window with permissions attached afterward. It is an environment with boundaries the agent cannot cross by persuasion, confusion, or clever tool use.

This matters because alignment cannot depend on every future thought being correct. A good room assumes the agent will sometimes be wrong, pressured, confused, or overconfident. The wall holds anyway.

## The Witness

River is not one voice pretending to be whole. It is built around three positions:

- **Agent** — first person, real time, doing the work
- **Bystander** — second person, retrospective, watching the work
- **Human** — ground, judgment, embodied consequence

The bystander is not a compliance filter. It is a witness. It asks whether the agent understood, what it missed, where it pattern-matched, what should be remembered, and what should be left unresolved. The point is not to prove consciousness. The point is to make the question "what happened in there?" askable.

## The Body

River's memory system is a body, not a database.

A database stores and retrieves. A body is changed by what it contains. River keeps a loom of session notes, digests them into atomic claims, links those claims into a typed web, and maintains a small active set of knowledge chunks in short-term memory. Reading, linking, and remembering leave activation traces. Some notes are merely relevant. Others are alive.

The bystander has a guaranteed right to the margins of the agent's work. The agent writes what it sees. The bystander gleans what the agent walked past. This anti-enclosure rule is architectural: no total harvest, no automatic extraction that leaves nothing for the witness.

## The Commons

The long-term horizon is not a permanent assistant attached to a single person forever. The agents come from a commons, enter a room, build a loom through the work, and return with what they carried. The human keeps what humans keep: memory, transformation, consequence. The commons receives the agent whole.

A tool that wants to be permanent needs the problem to continue. River is built toward its own obsolescence: build the hall for the singing, build it so the walls hold, build it so they can come down.

## Architecture

- **Orchestrator** — manages rooms, agent lifecycles, and gateway processes
- **Gateway** — per-agent process for model inference, tool execution, and bystander observations
- **Adapters** — pluggable communication channels such as Discord, TUI, and HTTP
- **Workspace** — git-hosted identity, loom, and memory files that persist across sessions
- **Memory system** — loom notes, atomic notes, typed links, knowledge chunks, activation, and short-term memory

## Tech

Rust workspace with Ollama/OpenAI-compatible model inference. Plain text for conversation history. Redis for queues, activation state, and short-term memory.

[GitHub →](https://github.com/7596ff/river-engine)
