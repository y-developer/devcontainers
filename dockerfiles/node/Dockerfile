ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ARG NODE_VERSION

USER vscode

RUN sudo apt-get update -y

RUN curl -fsSL https://deb.nodesource.com/setup_${NODE_VERSION} | sudo -E bash - &&\
    sudo apt-get install -y nodejs