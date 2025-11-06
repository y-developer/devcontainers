FROM appzic/dc:base-ubuntu-22.04

ARG VERSION=8.1
ARG NODE_VERSION=18.x

USER vscode

RUN sudo apt-get update -y

# Install Node Js
RUN curl -fsSL https://deb.nodesource.com/setup_${NODE_VERSION} | sudo -E bash - &&\
    sudo apt-get install -y nodejs

# Install prerequisites for php
RUN sudo apt-get install -y \
    software-properties-common \
    ca-certificates \
    lsb-release \
    apt-transport-https 

# Install php
RUN sudo add-apt-repository ppa:ondrej/php \
    && sudo apt-get update -y \
    && sudo apt-get install -y php${VERSION} \
    && sudo a2enmod php${VERSION}

# Install composer
RUN curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php \
    && sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

# Install php modules
RUN sudo apt-get install -y \
    php${VERSION}-cli \
    php${VERSION}-common \
    php${VERSION}-mysql \
    php${VERSION}-zip \
    php${VERSION}-gd \
    php${VERSION}-mbstring \
    php${VERSION}-curl \
    php${VERSION}-xml \
    php${VERSION}-bcmath \
    php${VERSION}-sqlite3
    