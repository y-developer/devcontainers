FROM appzic/dc:base-ubuntu-22.04

ARG VERSION=20.x

USER vscode

RUN sudo apt-get update -y

# Install Node 20.x
RUN curl -fsSL https://deb.nodesource.com/setup_${VERSION} | sudo -E bash - &&\
    sudo apt-get install -y nodejs