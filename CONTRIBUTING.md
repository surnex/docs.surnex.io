# Contribute to the Surnex documentation

Thank you for your interest in contributing to the Surnex docs. This guide will help you get started.

## How to contribute

### Option 1: Edit directly on GitHub

1. Navigate to the page you want to edit
2. Click the "Edit this file" button (the pencil icon)
3. Make your changes and submit a pull request

### Option 2: Local development

1. Clone this repository
2. Install the Mintlify CLI: `npm i -g mint`
3. Create a branch for your changes
4. Make changes
5. Run `mint dev` from the repository root, where `docs.json` lives
6. Preview your changes at `http://localhost:3000`
7. Run `mint broken-links` before you push
8. Commit your changes and submit a pull request

## Adding a page

1. Create the MDX file at the path you want it served from — `tracking/alerts.mdx` becomes `/tracking/alerts`
2. Add `title` and `description` frontmatter
3. Add the page path to the right group in `docs.json` — a page that isn't in the navigation won't appear in the sidebar

## Writing guidelines

- **Use active voice**: "Run the audit" not "The audit should be run"
- **Address the reader directly**: Use "you" instead of "the user"
- **Keep sentences concise**: Aim for one idea per sentence
- **Lead with the goal**: Start instructions with what the reader wants to accomplish
- **Use consistent terminology**: See the terminology list in `AGENTS.md`
- **Include examples**: Show, don't just tell

See `AGENTS.md` for the full style and terminology reference, which applies to human and AI contributors alike.
