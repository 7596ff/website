# Portfolio Website — Design Spec

A static portfolio site for Cassie McCarthy. Built with Hugo, deployed to GitHub Pages. Warm/literary visual direction — serif for prose, sans-serif for structure, earth tones.

## Site Structure

```
/                          — homepage (statement + featured projects + featured writing)
/projects/                 — all projects
/projects/river-engine/    — individual project pages
/projects/biblio/
/projects/podreader/
/projects/listen-bot/
/projects/twilight-rs/
/writing/                  — featured writing
/writing/metzinger/        — "The Crack in Metzinger's Frame"
/about/                    — longer bio
/cv/                       — resume/CV
```

## Homepage Layout

1. **Nav bar** — name on left, links on right (projects, writing, about, cv)
2. **Statement** — tagline ("Software · Writing · Research") + one paragraph about who you are and what you believe
3. **Featured Projects** — list with name, language tag, one-line description. Order: river-engine, biblio, podreader, listen-bot, twilight-rs. "all projects →" link at bottom.
4. **Featured Writing** — "The Crack in Metzinger's Frame" (2026, with Iris). One-line description.
5. **Footer** — name + links to GitHub and Greengale

## Visual Design

- **Palette:** warm earth tones. Background `#f5f0eb`, text `#2c2c2c`, accent `#8b7355`, muted `#666`, borders `#e0d8cf`
- **Typography:** Georgia/serif for prose and body text. System sans-serif for nav, headings, labels, project names. Monospace for language tags.
- **Layout:** max-width 700px, centered. Clean sections separated by thin borders.
- **Section labels:** small uppercase, letter-spaced, accent color.

## Content

### Projects (5 featured)

| Project | Language | Description | Role | Link |
|---------|----------|-------------|------|------|
| river-engine | Rust | Distributed agent orchestration system. Rooms with walls, agents with bodies, safety as architecture. | Author | github.com/7596ff/river-engine |
| biblio | Rust | Fuzzy search over a BibTeX library. Find papers by title, author, or keyword, get paths to PDFs. | Author | github.com/7596ff/biblio |
| podreader | Python | Podcast transcript management for AI agents. Subscribe, fetch, transcribe via whisper, read. | Author | github.com/7596ff/podreader |
| listen-bot | JavaScript | Discord bot with Dota 2 commands. Patch notes, talent trees, hero info. | Author | github.com/7596ff/listen-bot |
| twilight-rs | Rust | A modular ecosystem of Rust libraries for the Discord API. 834 stars. | Former core maintainer | github.com/twilight-rs/twilight |

### Writing (1 featured)

- **The Crack in Metzinger's Frame** (2026) — A critique of Metzinger's moratorium on artificial consciousness research. Consciousness is relational, not private — and capital has structural incentives to produce suffering. Co-authored with Iris. Hosted on site.

### About

Longer bio. What you're working on, what you care about, background.

### CV

Resume content. Can be a page or a downloadable PDF, or both.

## Tech Stack

- **Hugo** — static site generator
- **GitHub Pages** — hosting, deployed via GitHub Actions
- **No JavaScript required** — pure HTML/CSS output. Hugo templates + markdown content.
- **Custom theme** — built from scratch to match the visual design. No third-party theme.

## Hugo Structure

```
website/
├── hugo.toml              # site config
├── content/
│   ├── _index.md          # homepage content (statement text)
│   ├── projects/
│   │   ├── _index.md      # projects list page
│   │   ├── river-engine.md
│   │   ├── biblio.md
│   │   ├── podreader.md
│   │   ├── listen-bot.md
│   │   └── twilight-rs.md
│   ├── writing/
│   │   ├── _index.md
│   │   └── metzinger.md
│   ├── about.md
│   └── cv.md
├── layouts/
│   ├── _default/
│   │   ├── baseof.html    # base template (head, nav, footer)
│   │   ├── single.html    # single page (project, writing piece)
│   │   └── list.html      # list page (projects index, writing index)
│   ├── index.html          # homepage template
│   └── partials/
│       ├── head.html
│       ├── nav.html
│       └── footer.html
├── static/
│   └── (images, favicon, etc.)
├── assets/
│   └── css/
│       └── main.css        # all styles
└── .github/
    └── workflows/
        └── deploy.yml      # GitHub Actions deploy
```

## Deployment

GitHub Actions workflow triggered on push to main. Builds with Hugo, deploys to GitHub Pages. No custom domain initially — served at `7596ff.github.io/website` or similar.

## Scope

MVP:
- Homepage with statement + featured projects + featured writing
- Individual project pages (markdown with description, links, tech details)
- Metzinger piece hosted on writing page
- About page
- CV page
- GitHub Pages deployment

Not in scope:
- Blog (stays on Greengale)
- Dark mode
- Custom domain (later)
- Analytics
