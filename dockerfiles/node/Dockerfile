ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ARG NODE_VERSION

RUN apt-get update -y

RUN curl -fsSL https://deb.nodesource.com/setup_${NODE_VERSION} | bash - &&\
    apt-get install -y nodejs
