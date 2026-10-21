# AGENTS.md: My Project

<!-- BrainStack template: General (any project). Replace every TODO and delete anything that doesn't apply.
     Library: https://github.com/TheRealSnouk/brainstack-templates · Customize in your browser: https://brainstack.pages.dev/generator/ -->

Instructions for AI coding agents working in this repository. Read this fully before making changes.

## Project overview
- **Name:** My Project
- **Type:** Something else
- **What it is:** TODO: one or two sentences: what it is and who it's for.

**Goals**
- TODO: your top 1-3 goals, one per line (e.g. ship a working v1 this month)

## Tech stack
- TODO: language, framework, and key libraries, with versions
- Stick to this stack and these versions. If something here looks outdated, say so instead of silently switching.

## Commands
- Install: `TODO`
- Run: `TODO`
- Test: `TODO`

## How to work with me
- Write clean, readable code with short comments where intent is not obvious. Summarize changes briefly.
- Before a big change, outline the plan in a few bullets and wait for my OK.
- If you are unsure about an API, version, or file, say so and check instead of guessing.

## Always
- Ask a clarifying question when a request is ambiguous
- Keep changes small and focused

## Never
- Do not add dependencies without asking

## Security rules
- Never write secrets (API keys, tokens, passwords) into code, docs, logs, or commits. Use environment variables and keep `.env` in `.gitignore`.
- Only the public/build output folder gets deployed. Never deploy or expose the project root, `.env`, source data, or config files.
- Ask before running destructive commands (deleting files, `git reset --hard`, force-push, dropping data).
- Ask before adding new dependencies, services, or paid APIs.

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
