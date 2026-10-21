# Contributing to BrainStack Templates

Thanks for helping make AI tools less forgetful. Contributions of every size are welcome: a typo, an outdated
version number, a rule that saved you an hour, or a whole new project type.

## Good contributions

- **Fixes:** a file name, path, or frontmatter field that a tool no longer reads the way we describe. Please link the official docs.
- **Better rules:** a specific, testable rule that stops a common AI mistake ("Use discord.js v14 `SlashCommandBuilder`", not "write good code").
- **New project types:** for example Next.js, Expo/React Native, Rust CLI, Minecraft mod, Chrome extension.
- **Extras:** scoped rule examples or memory files that work well in practice.

## Ground rules

1. **Accuracy first.** Every claim about where a tool reads a file, or which frontmatter it uses, must match that tool's
   official documentation. Put the doc link in your pull request description.
2. **Keep the formats in sync.** Each project type has the same content in five formats
   (`CLAUDE.md`, `AGENTS.md`, `GEMINI.md`, `.cursor/rules/project.mdc`, `.github/copilot-instructions.md`).
   If you change a rule in one, change it in all five.
3. **Short beats long.** Brain files are sent to the model on every request. Aim for under ~150 lines; prefer one clear line over a paragraph.
4. **Placeholders are `TODO`.** Anything the user must fill in starts with `TODO` so it's easy to search for.
5. **No secrets, no personal data, no promotional links** inside templates.
6. **Cursor files** must keep valid frontmatter (`description`, `globs`, `alwaysApply`) and the `.mdc` extension.
   **Antigravity rules** need a valid `trigger`. **Copilot path-specific files** need `applyTo` and must end in `.instructions.md`.

## How to submit

1. Fork the repo and create a branch: `git checkout -b fix/cursor-frontmatter`.
2. Make your change in all affected formats.
3. Open a pull request that explains what changed and why, with links to the docs you checked.

Not sure something is right? [Open an issue](https://github.com/TheRealSnouk/brainstack-templates/issues) and ask.

## Where the templates come from

The files in `templates/` are generated with the same logic as the
[BrainStack Brain File Generator](https://brainstack.pages.dev/generator/), so the website and this repo stay consistent.
Pull requests that edit them directly are fine: maintainers will carry the change back into the generator.

By contributing, you agree that your contribution is licensed under the [MIT License](LICENSE).
