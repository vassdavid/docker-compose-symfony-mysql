FROM php:8.2-fpm-alpine

ARG STABILITY="stable"
# installs
## composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# php extensions installer: https://github.com/mlocati/docker-php-extension-installer
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions gd xdebug

RUN apk add --update -q --no-interactive \
    unzip \
    libzip-dev \
    autoconf \
    acl \
    git\
    fcgi \
    file \
    gettext \
    git \
    pecl install redis\
;

RUN install-php-extensions \
     apcu \
     intl \
     opcache \
     zip \
     pdo_mysql \
;

WORKDIR /app

#RUN bin/console doctrine:schema:create
#RUN bin/console doctrine:fixtures:load
#RUN bin/console lexik:jwt:generate-keypair --skip-if-exists
