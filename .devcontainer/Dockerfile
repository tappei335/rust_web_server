FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y \
    curl \
    git \
    gnupg2 \
    jq \
    sudo \
    zsh \
    vim \
    build-essential \
    openssl

ENV PATH="/root/.cargo/bin:${PATH}"
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- --default-toolchain none -y
RUN rustup toolchain install nightly --allow-downgrade --profile minimal --component clippy

