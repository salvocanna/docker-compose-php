FROM php:7.1.0-fpm-alpine

WORKDIR /var/www/

RUN apk update \
    && apk add --no-cache libmcrypt-dev \
    && docker-php-ext-install mcrypt mysqli pdo_mysql bcmath \
    && rm /var/cache/apk/*

RUN curl -sS https://getcomposer.org/installer | php \
    && \
    mv composer.phar /usr/local/bin/composer

