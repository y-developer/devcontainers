ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ARG PHP_VERSION

USER vscode

# Install php
RUN sudo add-apt-repository ppa:ondrej/php \
    && sudo apt-get update -y \
    && sudo apt-get install -y php${PHP_VERSION} \
    && sudo a2enmod php${PHP_VERSION}

# Install composer
RUN curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php \
    && sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

# Install php modules
RUN sudo apt-get install -y \
    php${PHP_VERSION}-cli \
    php${PHP_VERSION}-common \
    php${PHP_VERSION}-mysql \
    php${PHP_VERSION}-zip \
    php${PHP_VERSION}-gd \
    php${PHP_VERSION}-mbstring \
    php${PHP_VERSION}-curl \
    php${PHP_VERSION}-xml \
    php${PHP_VERSION}-bcmath \
    php${PHP_VERSION}-sqlite3
