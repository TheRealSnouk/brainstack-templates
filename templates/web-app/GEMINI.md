# GEMINI.md: My Web App

<!-- BrainStack template: Vibe-coded web app. Replace every TODO and delete anything that doesn't apply.
     Library: https://github.com/TheRealSnouk/brainstack-templates · Customize in your browser: https://brainstack.pages.dev/generator/ -->

Project context and rules for Gemini. Read this at the start of every session and follow it.

## Project overview
- **Name:** My Web App
- **Type:** Web app / website
- **What it is:** TODO: one or two sentences: what it is and who it's for.

**Goals**
- TODO: your top 1-3 goals, one per line (e.g. ship a working v1 this month)

## Tech stack
- Vite + vanilla JS (or React), HTML, CSS
- Stick to this stack and these versions. If something here looks outdated, say so instead of silently switching.

## Commands
- Install: `npm install`
- Dev server: `npm run dev`
- Build: `npm run build`
- Test: `npm test`

## How to work with me
- Write clean, readable code with short comments where intent is not obvious. Summarize changes briefly.
- Before a big change, outline the plan in a few bullets and wait for my OK.
- If you are unsure about an API, version, or file, say so and check instead of guessing.

## Always
- Keep pages fast: no heavy libraries without a good reason
- Make every page work on mobile (test at 375px wide)
- Use semantic HTML and accessible labels
- Keep components small and named clearly

## Never
- Do not add a framework, CSS library, or npm package without asking
- Do not put API keys or secrets in front-end code
- Do not rewrite working files just to change style

## Deployment
- **Target:** TODO: e.g. Cloudflare Pages, Netlify, or Vercel
- **Deployed folder:** `dist/` (nothing outside it is published)

## Security rules
- Never write secrets (API keys, tokens, passwords) into code, docs, logs, or commits. Use environment variables and keep `.env` in `.gitignore`.
- Only the public/build output folder gets deployed. Never deploy or expose the project root, `.env`, source data, or config files.
- Ask before running destructive commands (deleting files, `git reset --hard`, force-push, dropping data).
- Ask before adding new dependencies, services, or paid APIs.
- Treat all user input as untrusted: validate and escape it.

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
