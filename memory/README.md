# Project memory folder (docs/brain/)

A brain file holds the rules. This folder holds what the AI *learns*, so the next session starts where the last one ended.
Every template in this library tells the AI to read and update these files. Copy `docs/` into your project root.

| File | What goes in it | Who updates it |
|---|---|---|
| `docs/brain/NOW.md` | What was just done, what's next, open questions | The AI, at the end of every session |
| `docs/brain/decisions.md` | Important decisions and why | The AI, when a decision is made |
| `docs/brain/architecture.md` | How the project fits together | You and the AI, when structure changes |
| `docs/brain/gotchas.md` | Traps that cost you time once | The AI, whenever it hits one |
| `docs/brain/glossary.md` | Project-specific words and what they mean | You, when a term confuses the AI |

Commit the folder to git. It's versioned, backed up, and travels with the code.
Guide: https://brainstack.pages.dev/guides/ai-long-term-memory-backup/
