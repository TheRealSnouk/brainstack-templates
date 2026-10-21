# AGENTS.md: My Discord Bot

<!-- BrainStack template: Discord bot. Replace every TODO and delete anything that doesn't apply.
     Library: https://github.com/TheRealSnouk/brainstack-templates · Customize in your browser: https://brainstack.pages.dev/generator/ -->

Instructions for AI coding agents working in this repository. Read this fully before making changes.

## Project overview
- **Name:** My Discord Bot
- **Type:** Discord bot
- **What it is:** TODO: one or two sentences: what it is and who it's for.

**Goals**
- TODO: your top 1-3 goals, one per line (e.g. ship a working v1 this month)

## Tech stack
- Node.js 20 LTS + discord.js v14 (slash commands)
- Stick to this stack and these versions. If something here looks outdated, say so instead of silently switching.

## Commands
- Install: `npm install`
- Register slash commands: `node deploy-commands.js`
- Run bot: `node index.js`
- Test: `npm test`

## How to work with me
- Write clean, readable code with short comments where intent is not obvious. Summarize changes briefly.
- Before a big change, outline the plan in a few bullets and wait for my OK.
- If you are unsure about an API, version, or file, say so and check instead of guessing.

## Always
- Use slash commands, one file per command in commands/
- Defer replies for anything that can take longer than about 3 seconds
- Request only the gateway intents the bot actually needs
- Log errors with the command name and guild id (never the token)

## Never
- Do not hardcode the bot token, client id, or any secret; read them from environment variables
- Do not use discord.js v13 or older syntax
- Do not enable privileged intents unless the feature needs them

## Deployment
- **Target:** TODO: where the bot runs (e.g. a VPS, Railway, or your own PC)

## Security rules
- Never write secrets (API keys, tokens, passwords) into code, docs, logs, or commits. Use environment variables and keep `.env` in `.gitignore`.
- Ask before running destructive commands (deleting files, `git reset --hard`, force-push, dropping data).
- Ask before adding new dependencies, services, or paid APIs.
- Treat all user input as untrusted: validate and escape it.
- Do not log or commit personal data.

## Memory and backup
- Project knowledge lives in `docs/brain/` (architecture, glossary, gotchas). Read it before big changes and keep it current.
- Record important decisions in `docs/brain/decisions.md` as: date, decision, why, alternatives considered.
- At the end of each session, update `docs/brain/NOW.md` with: what was done, what is next, open questions. Read it at the start of every session.
- When I correct the same mistake twice, propose a new rule for this file.
- Commit after each working step with a clear message so any change can be rolled back.
- Never push to a remote or deploy without my explicit OK.

## Definition of done
- It builds/runs without errors or new warnings.
- The change does what was asked and nothing more.
- Docs and this file are updated if behavior or rules changed.
