FROM appzic/dc:base-ubuntu-22.04

ARG VERSION=3.7.3

USER vscode

# Install prerequisites
RUN sudo apt-get update -y && \
    sudo apt-get install -y \ 
    build-essential \
    wget \
    libffi-dev \
    libsqlite3-dev

# Download extract and python source file
RUN cd /tmp && \
    wget https://www.python.org/ftp/python/${VERSION}/Python-${VERSION}.tgz && \
    sudo tar -xf ./Python-${VERSION}.tgz

# Install
RUN cd /tmp/Python-${VERSION} &&\
    sudo ./configure --enable-optimizations &&\
    sudo make install

# Remove .tgz file
RUN sudo rm -fr /tmp/Python-${VERSION}.tgz

# Install python packages 
RUN sudo pip3 install pipenv
