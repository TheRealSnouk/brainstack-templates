# One source of truth: AGENTS.md + thin pointer files

Using more than one AI tool on the same repo? Don't keep five copies of the same rules.
Write everything once in `AGENTS.md`, then add the tiny files below so each tool finds it.

| File | What it does | Why it works |
|---|---|---|
| `CLAUDE.md` | `@AGENTS.md` import + Claude-only notes | Claude Code expands `@path` imports. (Recent versions also read AGENTS.md on their own when no CLAUDE.md exists.) |
| `.gemini/settings.json` | Tells Gemini CLI to load `AGENTS.md` | Gemini CLI's `context.fileName` setting accepts a list of file names. |
| `GEMINI.md` | Optional Gemini-only notes | Antigravity reads both GEMINI.md and AGENTS.md natively. Don't repeat AGENTS.md rules here. |
| `.github/copilot-instructions.md` | Short Copilot notes that point at AGENTS.md | Copilot cloud agent reads AGENTS.md natively; the pointer helps other Copilot features. |

Cursor reads `AGENTS.md` in the project root (and subfolders) natively, so it needs no pointer.

Copy the files you need into your project root next to your `AGENTS.md`.

> A pointer written in plain words ("follow AGENTS.md") only works if the AI decides to open the file.
> Prefer real imports or native AGENTS.md support where the tool has it, and keep must-follow rules in the main file.

Sources: [Claude Code memory docs](https://code.claude.com/docs/en/memory) · [Gemini CLI GEMINI.md docs](https://geminicli.com/docs/cli/gemini-md/) · [Cursor rules docs](https://cursor.com/docs/context/rules) · [GitHub Copilot custom instructions](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-repository-instructions)
