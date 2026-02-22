FROM texlive/texlive:latest

RUN apt-get update && apt-get install -y --no-install-recommends \
    default-jre \
    && rm -rf /var/lib/apt/lists/*

RUN curl -L https://github.com/valentjn/ltex-ls/releases/download/16.0.0/ltex-ls-16.0.0-linux-x64.tar.gz \
    | tar xz -C /opt \
    && mv /opt/ltex-ls-16.0.0 /opt/ltex-ls
