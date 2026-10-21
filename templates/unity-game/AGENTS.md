# AGENTS.md: My Unity Game

<!-- BrainStack template: Unity game. Replace every TODO and delete anything that doesn't apply.
     Library: https://github.com/TheRealSnouk/brainstack-templates · Customize in your browser: https://brainstack.pages.dev/generator/ -->

Instructions for AI coding agents working in this repository. Read this fully before making changes.

## Project overview
- **Name:** My Unity Game
- **Type:** Game (Godot / Unity)
- **What it is:** TODO: one or two sentences: what it is and who it's for.

**Goals**
- TODO: your top 1-3 goals, one per line (e.g. ship a working v1 this month)

## Tech stack
- Unity (TODO: exact editor version from Unity Hub, e.g. Unity 6 LTS) with C#
- Render pipeline: TODO (URP, HDRP, or Built-in)
- Input: TODO (Input System package or legacy Input Manager)
- Stick to this stack and these versions. If something here looks outdated, say so instead of silently switching.

## Commands
- Open project: `Unity Hub > Add > select the project folder`
- Run game: `press Play in the editor`
- Tests: `Window > General > Test Runner`
- Build: `TODO (File > Build Profiles in Unity 6, File > Build Settings in older versions)`

## How to work with me
- Write clean, readable code with short comments where intent is not obvious. Summarize changes briefly.
- Before a big change, outline the plan in a few bullets and wait for my OK.
- If you are unsure about an API, version, or file, say so and check instead of guessing.

## Always
- Use the Unity version above: check APIs against that version, never older or newer ones
- Use [SerializeField] private fields instead of public fields for Inspector values
- Cache component references in Awake or Start instead of calling GetComponent every frame
- Tell me which GameObject a script goes on and what to assign in the Inspector

## Never
- Do not hand-edit .unity scene or .prefab files unless I ask; tell me the editor steps instead
- Do not move, rename, or delete assets or .meta files outside the Unity editor (it breaks references)
- Do not add Asset Store packages or plugins with unclear licenses

## Deployment
- **Target:** TODO: e.g. itch.io or Steam
- **Deployed folder:** `Builds/` (nothing outside it is published)

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
