# PaperMoon Developer Documentation Style Guide

This repository contains the PaperMoon style guide, which sets forth the standards and best practices for crafting high-quality technical documentation. It is intended to help you produce clear, consistent, and accessible content. It covers writing style and formatting, code examples, images, and more.

## Files

- **[`style-guide.md`](./style-guide.md)**: The prose style guide. This is the source of truth.
- **[`AGENTS.md`](./AGENTS.md)**: The machine-readable companion that coding agents (Claude Code, Cursor, Codex, etc.) load automatically when the repo is opened. Front-loads the rules that AI-generated documentation most often violates.
- **[`checklist.md`](./checklist.md)**: A human-reviewer checklist for use before requesting a PR review.
- **[`.vale.ini`](./.vale.ini) and [`styles/PaperMoon/`](./styles/PaperMoon/)**: A starter [Vale](https://vale.sh) configuration that mechanically enforces the highest-friction rules (banned phrases, terminology, emoji, link text, placeholders). Run `vale .` locally and wire into CI.

## Using this guide in a downstream docs repo

Add an `AGENTS.md` at the root of your docs repo containing:

```markdown
# AGENTS.md

This repo follows the [PaperMoon Documentation Style Guide](https://github.com/papermoonio/documentation-style-guide/blob/main/AGENTS.md). Read it before generating or editing documentation.

Project-specific overrides:

- (list any deviations here, with rationale)
```

Adopt `.vale.ini` and the `styles/PaperMoon/` directory to lint with the PaperMoon rules.
