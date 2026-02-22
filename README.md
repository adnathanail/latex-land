# latex-land

Isolated VS Code + Docker environment for LaTeX documents.

## Prerequisites

- [Docker](https://www.docker.com/) (or [OrbStack](https://orbstack.dev/))
- VS Code with the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension

## Usage

### Direct

Open this repo in VS Code and select **Reopen in Container** when prompted.

### Symlink into another project

To use this environment in any LaTeX project without copying the config:

```bash
ln -s ~/your/path/to/latex-land/.devcontainer .devcontainer
```

Then open that project in VS Code and select **Reopen in Container**.

To avoid committing the symlink in other repos, add `.devcontainer` to your gitignore:

```bash
echo '.devcontainer' >> .gitignore
```
