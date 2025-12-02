ARG UBUNTU_VERSION
FROM mcr.microsoft.com/devcontainers/base:ubuntu-${UBUNTU_VERSION}

USER vscode

RUN apt-get update && sudo apt-get install -y \
    build-essential \
    wget \
    curl \
    libffi-dev \
    libsqlite3-dev \
    software-properties-common \
    ca-certificates \
    lsb-release \
    apt-transport-https \
    telnet
