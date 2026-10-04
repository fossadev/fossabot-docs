# Fossabot Docs

[![Markdown linting](https://github.com/fossadev/fossabot-docs/actions/workflows/markdown-lint.yaml/badge.svg)](https://github.com/fossadev/fossabot-docs/actions/workflows/markdown-lint.yaml)

> The official public Fossabot documentation, hosted at [fossabot.com/docs](https://fossabot.com/docs).

## Feedback

Issues are currently disabled for this repo, however we do welcome plenty of discusion about our documentation, and encourage others to get involved. Most of our discussion happens on Discord right now, simply to keep contributors in one place where we can work together.

If you would like to give feedback, or bring up anything you'd typically make a GitHub issue for, feel free to [Join the Discord](https://fossabot.com/discord) and post in #support!

## Setup

This website is built using [Mintlify](https://mintlify.com). The site lives in the `docs/` directory, with navigation and site settings defined in [`docs/docs.json`](docs/docs.json).

### Local Development

```
$ cd docs
$ npx mint dev
```

This command starts a local preview at `http://localhost:3000`. Most changes are reflected live without having to restart the server.

### Adding a page

Create an `.mdx` file under `docs/` with a `title` in its frontmatter, then add its path (without the extension) to the `navigation` section of `docs/docs.json`.

### Validation

```
$ cd docs
$ npx mint validate
$ npx mint broken-links
```

### Linting

```
$ npx markdownlint-cli2 "docs/**/*.mdx"
```

Lints/validates all markdown files in the project.
