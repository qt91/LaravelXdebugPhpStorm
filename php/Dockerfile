FROM php:7.3-fpm-alpine

RUN apk --update add vim freetype-dev libjpeg-turbo-dev libpng-dev shadow libzip-dev && \
    docker-php-ext-install pdo_mysql mbstring gd zip

RUN apk add autoconf build-base \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY php/xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini