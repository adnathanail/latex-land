FROM texlive/texlive:latest

ARG LTEX_LS_VERSION=15.2.0

RUN apt-get update && apt-get install -y --no-install-recommends \
    default-jre \
    && rm -rf /var/lib/apt/lists/*

RUN curl -L https://github.com/valentjn/ltex-ls/releases/download/${LTEX_LS_VERSION}/ltex-ls-${LTEX_LS_VERSION}-linux-x64.tar.gz \
    | tar xz -C /opt \
    && mv /opt/ltex-ls-${LTEX_LS_VERSION} /opt/ltex-ls

COPY keybindings-extension/package.json /root/.vscode-server/extensions/local.latex-land-keybindings-0.0.1/package.json
