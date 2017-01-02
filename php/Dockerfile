FROM php:7.1.0-fpm-alpine

# Why this, you may ask?
# Because who made the base php fpm 7.1 alpine image set up /var/www/html as working directory
# and Docker tries as much as it can to honour that. Making me break this pearl of Dockerfile
# in the moment I mount my code in /var/www (without the html folder)
WORKDIR /var/www/

RUN apk update \
    && apk add --no-cache libmcrypt-dev \
    && docker-php-ext-install mcrypt mysqli pdo_mysql bcmath \
    && rm /var/cache/apk/*

RUN curl -sS https://getcomposer.org/installer | php \
    && \
    mv composer.phar /usr/local/bin/composer

