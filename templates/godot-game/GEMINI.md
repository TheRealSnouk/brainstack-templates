# GEMINI.md: My Godot Game

<!-- BrainStack template: Godot game. Replace every TODO and delete anything that doesn't apply.
     Library: https://github.com/TheRealSnouk/brainstack-templates · Customize in your browser: https://brainstack.pages.dev/generator/ -->

Project context and rules for Gemini. Read this at the start of every session and follow it.

## Project overview
- **Name:** My Godot Game
- **Type:** Game (Godot / Unity)
- **What it is:** TODO: one or two sentences: what it is and who it's for.

**Goals**
- TODO: your top 1-3 goals, one per line (e.g. ship a working v1 this month)

## Tech stack
- Godot 4.x with GDScript (TODO: your exact version, e.g. 4.5)
- Target platforms: TODO (e.g. Windows, Web)
- Stick to this stack and these versions. If something here looks outdated, say so instead of silently switching.

## Commands
- Open project: `godot --editor project.godot`
- Run game: `press F5 in the editor`
- Export: `Project > Export (presets in export_presets.cfg)`

## How to work with me
- Write clean, readable code with short comments where intent is not obvious. Summarize changes briefly.
- Before a big change, outline the plan in a few bullets and wait for my OK.
- If you are unsure about an API, version, or file, say so and check instead of guessing.

## Always
- Use the engine version above: never use APIs or syntax from older or newer versions
- Use typed variables and signals instead of polling where possible
- Keep one script per scene or node responsibility
- Explain which node a script attaches to and how to wire signals in the editor

## Never
- Do not hand-edit scene or resource files unless I ask; tell me the editor steps instead
- Do not rename or move assets outside the editor (it breaks references)
- Do not add plugins or assets with unclear licenses

## Deployment
- **Target:** TODO: e.g. itch.io or Steam
- **Deployed folder:** `build/` (nothing outside it is published)

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
