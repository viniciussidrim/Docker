# Script base para build aplicação Laravel 

FROM jenkins/jenkins:lts-jdk17

USER root

RUN apt-get update && apt-get install -y \
    php \
    php-xml \
    php-mbstring \
    php-curl \
    php-zip \
    php-cli \
    php-gmp \
    php-pdo-mysql \
    unzip \
    git \
    curl \
    npm \
    && \
    rm -rf /var/lib/apt/lists/*

RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

RUN php -v && composer -v

USER jenkins
