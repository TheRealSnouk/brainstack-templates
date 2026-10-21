# Discord bot: brain file templates

discord.js v14 bots with slash commands. Keeps the token out of code and intents minimal.

| Tool | Template |
|---|---|
| Claude Code | [`CLAUDE.md`](CLAUDE.md) |
| AGENTS.md agents (OpenAI Codex, Cursor, GitHub Copilot cloud agent, Antigravity, and more) | [`AGENTS.md`](AGENTS.md) |
| Gemini CLI and Google Antigravity | [`GEMINI.md`](GEMINI.md) |
| Cursor | [`.cursor/rules/project.mdc`](.cursor/rules/project.mdc) |
| GitHub Copilot | [`.github/copilot-instructions.md`](.github/copilot-instructions.md) |

**How to use:** copy the file for your tool into the same path in your project (for example `CLAUDE.md` goes in the project root,
`.github/copilot-instructions.md` goes in a `.github` folder at the root). Then replace every `TODO` and delete anything that doesn't apply.
All five files say the same thing in each tool's format, so you only need the one(s) for the tools you use.

Want it pre-filled for your project? Use the free generator: https://brainstack.pages.dev/generator/
Guide for this kind of project: https://brainstack.pages.dev/guides/discord-bot-ai-setup/
