# Reader Side

[日本語](README.ja.md)

Reader Side is a portable Agent Skill for writing from the actual reader's side instead of narrating the maker's process.

It decides what belongs in a PR description, UI message, issue, release note, document, report, or email by asking what the reader needs to understand, decide, or do.

## What it prevents

- Local instructions and setup details leaking into a public artifact.
- Temporary implementation failures and work chronology replacing the final result.
- UI copy explaining implementation details instead of what users need to know.
- One combined explanation being reused for users, reviewers, and maintainers with different needs.
- Meta-commentary about following the skill appearing in the finished text.

Reader Side is not a brevity rule or a ban on technical detail. It keeps unresolved failures, risks, constraints, uncertainty, migration requirements, and evidence that the actual reader needs.

## Installation

### Claude Code

Run these as two separate prompts:

```text
/plugin marketplace add cannorin/reader-side
```

```text
/plugin install reader-side@reader-side
```

### Codex

Run these in your shell:

```sh
codex plugin marketplace add cannorin/reader-side
codex plugin add reader-side@reader-side
```

Start a new session after installation. Claude Code exposes the skill as `/reader-side:reader-side`; Codex exposes it as `$reader-side:reader-side`. Both agents can also select it automatically when relevant.

### Other coding agents

Copy `skills/reader-side/` to the appropriate personal or project directory:

| Agent | Personal | Project |
| --- | --- | --- |
| [Cursor](https://cursor.com/help/customization/skills) | `~/.cursor/skills/reader-side/` or `~/.agents/skills/reader-side/` | `.cursor/skills/reader-side/` or `.agents/skills/reader-side/` |
| [GitHub Copilot](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) | `~/.copilot/skills/reader-side/` or `~/.agents/skills/reader-side/` | `.github/skills/reader-side/` or `.agents/skills/reader-side/` |
| [Gemini CLI](https://geminicli.com/docs/cli/tutorials/skills-getting-started/) | `~/.gemini/skills/reader-side/` | `.gemini/skills/reader-side/` or `.agents/skills/reader-side/` |

You can ask the agent explicitly:

> Use reader-side to review this PR description for details its reviewers do not need.
