# CLAUDE.md

This is a dev container configuration repo for LaTeX work in VS Code. There are no source files here — just `.devcontainer/` config that gets symlinked into LaTeX projects.

## Structure

- `.devcontainer/Dockerfile` — Container image (texlive, ltex-ls, keybindings extension)
- `.devcontainer/devcontainer.json` — VS Code extensions, settings
- `.devcontainer/keybindings-extension/` — Minimal VS Code extension that provides custom keybindings (baked into the image via `COPY` in Dockerfile)

## Key details

- The keybindings extension has no code — just `contributes.keybindings` in its `package.json`. After editing, rebuild the container for changes to take effect.
- The devcontainer.json uses JSONC (JSON with comments).
- This repo is meant to be symlinked into other projects via `ln -s`, not used as a standalone LaTeX project.
