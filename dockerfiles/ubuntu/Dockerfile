ARG UBUNTU_VERSION
FROM mcr.microsoft.com/devcontainers/base:ubuntu-${UBUNTU_VERSION}

USER root

RUN apt-get update && apt-get install -y \
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

USER vscode
