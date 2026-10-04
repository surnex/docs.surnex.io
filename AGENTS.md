# Documentation project instructions

## About this project

- This is the documentation site for [Surnex](https://surnex.io), built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links
- For Mintlify product knowledge (components, configuration, writing standards), install the Mintlify skill: `npx skills add https://mintlify.com/docs`

## Product context

Surnex is an SEO platform (a SEMrush/Ahrefs alternative). The user-facing surfaces are:

- `app.surnex.io` — the dashboard where all documented workflows happen
- `api.surnex.io` — the REST API, documented under the **API Reference** tab from `https://api.surnex.io/docs/openapi.json` (`openapi.source` in `docs.json`; a wrong URL there fails every deploy)
- `api.surnex.io/mcp` — the MCP server for AI agents, documented under the **MCP** tab

Most pages in the dashboard show **stored data** collected by scheduled background jobs, not
live lookups. SERP results and Google Trends are the only live/on-demand pages. Never
document a stored-data feature as if it fetches on demand.

## Terminology

- **Organization** — the top-level container for projects, team, billing, and API keys. Not "workspace" or "account".
- **Project** — one tracked domain plus its target location and language. Not "site" or "campaign".
- **Member** — someone in an organization. Not "user", except when referring to the reader.
- **Tracked keyword** — a keyword under daily rank tracking. Distinct from a **saved keyword** from research, which is not yet tracked.
- **Audit** — one crawl of a site. Not "scan".
- **AI search** — visibility in AI-generated results (AI Overviews, AI Mode, ChatGPT).
- **GEO** — generative engine optimization; prompt-level share of voice in AI answers. What it tracks is a **prompt**, not a "topic". Always expand on first use in a page.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, domains, and code references
- Lead with the reader's goal, not the interface

## Content boundaries

- Document what a customer can see and do in the dashboard, API, or MCP server
- Don't document internal architecture — Celery/pgmq queues, worker services, database schema, or job dispatch internals
- Don't document unreleased or feature-flagged functionality
- Don't state specific plan limits or prices in feature pages; link to [Plans](/billing/plans) instead
