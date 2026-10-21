<p align="center">
  <a href="https://brainstack.pages.dev"><img src="https://brainstack.pages.dev/logo.svg" width="72" height="72" alt="BrainStack logo"></a>
</p>

<h1 align="center">BrainStack Templates</h1>

<p align="center"><b>Copy-paste brain files for your AI coding tools.</b><br>
CLAUDE.md · AGENTS.md · GEMINI.md · Cursor rules (.mdc) · copilot-instructions.md</p>

<p align="center">
  <a href="https://brainstack.pages.dev/generator/">Generator</a> ·
  <a href="https://brainstack.pages.dev/guides/">Guides</a> ·
  <a href="https://brainstack.pages.dev/#newsletter">Newsletter</a> ·
  <a href="https://x.com/BrainStacksAI">@BrainStacksAI</a>
</p>

---

Your AI forgets your project every time you open a new chat. A **brain file** fixes that: a short Markdown file in
your repo that your AI tool loads automatically at the start of every session, with your stack, commands, rules,
and where to keep memory. Write it once, and you stop re-explaining your project (and stop finding API keys in your code).

This repo is a free library of ready-made brain files for common project types, in the format each tool expects.
They're built with the same logic as the free [BrainStack Brain File Generator](https://brainstack.pages.dev/generator/),
so you can start from a template here or generate a pre-filled one in your browser.

## Which tool reads which file?

| Tool | File it reads | Where it goes |
|---|---|---|
| **Claude Code** | `CLAUDE.md` | Project root (or `.claude/CLAUDE.md`). Global: `~/.claude/CLAUDE.md`. Supports `@path` imports; recent versions also read `AGENTS.md` when there's no `CLAUDE.md`. |
| **AGENTS.md agents** (OpenAI Codex, Cursor, GitHub Copilot cloud agent, Google Antigravity, and others) | `AGENTS.md` | Project root. Nested `AGENTS.md` files in subfolders add folder rules. |
| **Gemini CLI** and **Google Antigravity** | `GEMINI.md` | Project root and subfolders. Global: `~/.gemini/GEMINI.md`. Plain Markdown, no frontmatter. |
| **Cursor** | `.cursor/rules/*.mdc` | Must be `.mdc` with frontmatter (`description`, `globs`, `alwaysApply`). Cursor also reads `AGENTS.md`. |
| **GitHub Copilot** | `.github/copilot-instructions.md` | Repository-wide. Path-specific: `.github/instructions/*.instructions.md` with `applyTo`. |

Not sure? Start with **`AGENTS.md`**: the most tools read it. More detail: [GEMINI.md vs CLAUDE.md vs AGENTS.md vs Cursor rules vs Copilot](https://brainstack.pages.dev/guides/ai-rules-file-formats/).

## Templates

Every project type comes in all five formats. Same rules, each tool's file name and format.

| Project type | Claude Code | AGENTS.md | Gemini / Antigravity | Cursor | Copilot |
|---|---|---|---|---|---|
| [Vibe-coded web app](templates/web-app/) | [CLAUDE.md](templates/web-app/CLAUDE.md) | [AGENTS.md](templates/web-app/AGENTS.md) | [GEMINI.md](templates/web-app/GEMINI.md) | [project.mdc](templates/web-app/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/web-app/.github/copilot-instructions.md) |
| [Godot game](templates/godot-game/) | [CLAUDE.md](templates/godot-game/CLAUDE.md) | [AGENTS.md](templates/godot-game/AGENTS.md) | [GEMINI.md](templates/godot-game/GEMINI.md) | [project.mdc](templates/godot-game/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/godot-game/.github/copilot-instructions.md) |
| [Unity game](templates/unity-game/) | [CLAUDE.md](templates/unity-game/CLAUDE.md) | [AGENTS.md](templates/unity-game/AGENTS.md) | [GEMINI.md](templates/unity-game/GEMINI.md) | [project.mdc](templates/unity-game/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/unity-game/.github/copilot-instructions.md) |
| [Discord bot](templates/discord-bot/) | [CLAUDE.md](templates/discord-bot/CLAUDE.md) | [AGENTS.md](templates/discord-bot/AGENTS.md) | [GEMINI.md](templates/discord-bot/GEMINI.md) | [project.mdc](templates/discord-bot/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/discord-bot/.github/copilot-instructions.md) |
| [Python / data / automation](templates/python-data/) | [CLAUDE.md](templates/python-data/CLAUDE.md) | [AGENTS.md](templates/python-data/AGENTS.md) | [GEMINI.md](templates/python-data/GEMINI.md) | [project.mdc](templates/python-data/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/python-data/.github/copilot-instructions.md) |
| [General (any project)](templates/general/) | [CLAUDE.md](templates/general/CLAUDE.md) | [AGENTS.md](templates/general/AGENTS.md) | [GEMINI.md](templates/general/GEMINI.md) | [project.mdc](templates/general/.cursor/rules/project.mdc) | [copilot-instructions.md](templates/general/.github/copilot-instructions.md) |

### Extras

| Folder | What's inside |
|---|---|
| [`memory/`](memory/) | A `docs/brain/` memory folder (`NOW.md` handoff, decision log, architecture, gotchas, glossary). Every template tells the AI to use it. |
| [`extras/one-source-of-truth/`](extras/one-source-of-truth/) | Use several AI tools on one repo with a single `AGENTS.md` plus tiny pointer files (`CLAUDE.md` with `@AGENTS.md`, Gemini CLI `settings.json`, and more). |
| [`extras/scoped-rules/`](extras/scoped-rules/) | Rules that load only for some files: Cursor `globs`, Claude Code `.claude/rules` `paths`, Copilot `applyTo`, Antigravity `.agents/rules` triggers. |
| [`extras/global/`](extras/global/) | A personal "about me" file for `~/.claude/CLAUDE.md` or `~/.gemini/GEMINI.md`. |

## How to use

1. **Pick your project type** in the table above and open the file for your tool.
2. **Copy it to the same path in your project.** `CLAUDE.md`, `AGENTS.md`, and `GEMINI.md` go in the root;
   the Cursor file goes in `.cursor/rules/`; the Copilot file goes in `.github/`.
3. **Replace every `TODO`.** Put in your real versions and commands. Exact versions are what stop your AI from writing outdated code.
4. **Delete what doesn't apply.** Shorter files get followed better. Aim for under ~150 lines.
5. **Copy [`memory/docs/`](memory/docs/)** into your project root if you want the AI to keep session notes and a decision log.
6. **Test it.** Start a fresh session and ask: *"What are the rules for this project, and what command runs the tests?"*
   If the answer doesn't match your file, it isn't loaded.
7. **Commit it.** Your AI's brain is now versioned and backed up with your code.

Prefer not to edit by hand? The [Brain File Generator](https://brainstack.pages.dev/generator/) fills all of this in from a short form, in your browser. Nothing is uploaded.

Or grab one from the command line, for example:

```bash
curl -fsSL -o AGENTS.md https://raw.githubusercontent.com/TheRealSnouk/brainstack-templates/main/templates/web-app/AGENTS.md
```

## Tips that make brain files actually work

- **Be specific.** "Run `npm test` before saying you're done" beats "test your changes".
- **Pin versions.** "Godot 4.5, never Godot 3 syntax" saves hours.
- **Write security rules down.** No secrets in code, only deploy the build folder, ask before destructive commands.
- **Grow it from mistakes.** When you correct the AI on the same thing twice, add a rule.
- **No secrets in brain files, ever.** They're committed to git and sent to the model.

## Learn more

- [What a brain file is (and why your AI keeps forgetting)](https://brainstack.pages.dev/guides/what-is-a-brain-file/)
- [GEMINI.md vs CLAUDE.md vs AGENTS.md vs Cursor rules vs Copilot instructions](https://brainstack.pages.dev/guides/ai-rules-file-formats/)
- [How to write a GEMINI.md for Gemini CLI and Antigravity](https://brainstack.pages.dev/guides/gemini-md-gemini-cli-antigravity/)
- [Set up your AI for a vibe-coded web app in 10 minutes](https://brainstack.pages.dev/guides/vibe-coded-web-app-setup/)
- [Set up an AI agent for a Godot or Unity game project](https://brainstack.pages.dev/guides/game-dev-ai-setup-godot-unity/)
- [Set up AI for a Discord bot project](https://brainstack.pages.dev/guides/discord-bot-ai-setup/)
- [Give your AI long-term memory (and back it up)](https://brainstack.pages.dev/guides/ai-long-term-memory-backup/)

Official docs: [Claude Code memory](https://code.claude.com/docs/en/memory) ·
[AGENTS.md](https://agents.md) ·
[Gemini CLI GEMINI.md](https://geminicli.com/docs/cli/gemini-md/) ·
[Antigravity rules](https://antigravity.google/docs/rules/) ·
[Cursor rules](https://cursor.com/docs/context/rules) ·
[Copilot custom instructions](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions)

AI tools change fast. These templates were checked against the official docs in October 2026; if something behaves
differently, please [open an issue](https://github.com/TheRealSnouk/brainstack-templates/issues).

## Get new templates by email

The free [BrainStack newsletter](https://brainstack.pages.dev/#newsletter) sends one short email when there's a new
guide, template, or AI setup trick worth stealing. Subscribers also get the **Brain File Starter Pack**: these templates
in one zip, plus a printable quickstart.

## Contributing

Fixes and new templates are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE). Use these in any project, commercial or not. No attribution required (but a star helps others find it ⭐).

<sub>BrainStack is independent and not affiliated with Anthropic, Google, OpenAI, Cursor (Anysphere), or GitHub. Product names are trademarks of their owners.</sub>
