---
title: biblio
language: rust
description: "Fuzzy search over a BibTeX library. Find papers by title, author, or keyword, get paths to PDFs."
featured: true
weight: 2
link: https://github.com/7596ff/biblio
---

Biblio searches a Zotero-exported BibTeX library with fuzzy matching and returns paths to PDFs. Built for AI agents that need to look up and read papers.

Multi-word queries split on whitespace — each term must match, scores sum. LaTeX escapes are handled transparently (`Luk{\'a}cs` displays as `Lukács`, searchable as `lukacs`). Three output modes: rich (default), raw BibTeX, or just the file path for piping.

Built with TDD — 22 tests covering the parser (LaTeX escapes, nested braces, multi-author, malformed entries), search (scoring, ordering, path resolution), and integration against real BibTeX data.

[GitHub →](https://github.com/7596ff/biblio)
