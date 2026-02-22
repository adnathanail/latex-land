# latex-land

Isolated VS Code + Docker environment for LaTeX documents.

Features
- [LtEX](https://valentjn.github.io/ltex/index.html)
    - Spelling + Grammar checking
    - `ltex-ls` is auto-installed in the Dockerfile, so the extension doesn't have to redownload it every time you open a new workspace
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
    - Build on save
    - View file inline
    - SyncTeX, for jumping back and forth between the PDF and the code
        - `Cmd+Click` on PDF to jump to source
        - `Cmd+J` in code to jump to PDF

## Prerequisites

- [Docker](https://www.docker.com/) (or [OrbStack](https://orbstack.dev/))
- VS Code with the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension

## Usage

### Direct

Open this repo in VS Code and select **Reopen in Container** when prompted.

### Symlink into another project

To use this environment in any LaTeX project without copying the config:

```bash
ln -s ~/Document/Uni/latex-land/.devcontainer .devcontainer
```

Then open that project in VS Code and select **Reopen in Container**.

To avoid committing the symlink in other repos, add `.devcontainer` to your gitignore:

```bash
echo '.devcontainer' >> .gitignore
```
