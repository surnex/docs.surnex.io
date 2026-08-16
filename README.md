# Surnex documentation

The source for [docs.surnex.io](https://docs.surnex.io), built on [Mintlify](https://mintlify.com).

## Structure

| Path | Contents |
| --- | --- |
| `docs.json` | Site config, theme, and navigation. A page must be listed here to appear in the sidebar. |
| `introduction.mdx`, `quickstart.mdx` | Landing and getting-started pages |
| `<feature>/*.mdx` | Product pages, one directory per feature area |
| `guides/` | End-to-end workflow walkthroughs |
| `api/` | REST API reference — the endpoint pages are generated from `https://api.surnex.io/openapi.json` |
| `mcp/` | MCP server documentation for AI agents |
| `changelog/` | Monthly release notes |
| `AGENTS.md` | Style, terminology, and content boundaries for contributors and AI tools |

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```
npm i -g mint
```

Run the dev server from the repository root, where `docs.json` lives:

```
mint dev
```

View your local preview at `http://localhost:3000`.

Check links before pushing:

```
mint broken-links
```

## AI-assisted writing

Install Mintlify's documentation skill for your AI coding tool:

```bash
npx skills add https://mintlify.com/docs
```

The skill covers component reference, writing standards, and workflow guidance. Project-specific rules live in `AGENTS.md`.

## Publishing

Changes are deployed to production automatically after merging to the default branch, via the Mintlify GitHub app.

## Troubleshooting

- Dev server won't start: run `mint update` to get the latest CLI
- A page 404s: confirm the file exists at the path and that the path is listed in `docs.json`

See [CONTRIBUTING.md](CONTRIBUTING.md) for the contribution workflow.
