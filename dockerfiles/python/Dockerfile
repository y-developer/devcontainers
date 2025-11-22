ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ARG PYTHON_VERSION

USER vscode

# Download extract and python source file
RUN cd /tmp && \
    wget https://www.python.org/ftp/python/${PYTHON_VERSION}/Python-${PYTHON_VERSION}.tgz && \
    sudo tar -xf ./Python-${PYTHON_VERSION}.tgz

# Install
RUN cd /tmp/Python-${PYTHON_VERSION} &&\
    sudo ./configure --enable-optimizations &&\
    sudo make install

# Remove .tgz file
RUN sudo rm -fr /tmp/Python-${PYTHON_VERSION}.tgz

# Install python packages 
RUN sudo pip3 install pipenv
