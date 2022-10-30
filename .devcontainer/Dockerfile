ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/rust:1-${VARIANT}

USER root

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends build-essential libssl-dev pkg-config cmake

RUN rustup default nightly

# RUN cargo install casper-client