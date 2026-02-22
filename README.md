# latex-land

Isolated VS Code + Docker environment for LaTeX documents.

Features
- LaTeX installation inside Dockerfile
    - Prevents any collisions with your system LaTeX install
- [LTeX](https://valentjn.github.io/ltex/index.html)
    - Spelling + Grammar checking
    - `ltex-ls` is auto-installed in the Dockerfile, so the extension doesn't have to redownload it every time you open a new workspace
- [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
    - Build on save
    - View file inline
    - SyncTeX, for jumping back and forth between the PDF and the code
- [TikZiT](https://tikzit.github.io)
    - Editing `.tikz` files, specifically for ZX-Diagrams
- Custom keybindings
    - `Cmd+J` to **jump** from a line in source code to the corresponding location in a PDF, or the TikZiT editor, or from a selected element in the TikZiT editor back to the source code
    - `Cmd+Click` on a location in a PDF to the location in `.tex` source code
    - `Cmd+D` to duplicate a file
        - This won't work if you're in the TikZiT editor, open the text editor for the file first with `Cmd+J`

## Prerequisites

- [Docker](https://www.docker.com/) (or [OrbStack](https://orbstack.dev/))
- VS Code with the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension

## Usage (symlink)

To use this environment in any LaTeX project without copying the config:

```bash
ln -s ~/Document/Uni/latex-land/.devcontainer .devcontainer
```

Then open that project in VS Code and select **Reopen in Container**.

To avoid committing the symlink in other repos, add `.devcontainer` to your gitignore:

```bash
echo '.devcontainer' >> .gitignore
```

## Updating LTeX LS

The `ltex-ls` language server is manually installed in the Dockerfile, to prevent it redownloading every time a new workspace is opened.

The version used needs to match the version expected by the VS Code extension

See the [VS Code extension changelog](https://valentjn.github.io/ltex/vscode-ltex/changelog.html) to check which version is the latest supported