# Scoped rules: load extra rules only for some files

Keep your main brain file short. Rules that only matter for part of the codebase can live in scoped files
that each tool loads when it touches matching files.

| Tool | Folder | Scope field | Example |
|---|---|---|---|
| Cursor | `.cursor/rules/*.mdc` | `globs` (or `description` for "apply intelligently") | [`cursor/.cursor/rules/`](cursor/.cursor/rules/) |
| Claude Code | `.claude/rules/*.md` | `paths` | [`claude-code/.claude/rules/`](claude-code/.claude/rules/) |
| GitHub Copilot | `.github/instructions/*.instructions.md` | `applyTo` | [`copilot/.github/instructions/`](copilot/.github/instructions/) |
| Antigravity | `.agents/rules/*.md` | `trigger` (`always_on`, `model_decision`, `glob`, `manual`) | [`antigravity/.agents/rules/`](antigravity/.agents/rules/) |

Gotchas:
- Cursor ignores plain `.md` files in `.cursor/rules`: the extension must be `.mdc`.
- Antigravity discards a rule whose frontmatter is missing or whose trigger is misspelled, and only scans files directly inside `.agents/rules/`.
- On GitHub.com, Copilot path-specific instructions are currently used by Copilot cloud agent and code review.
