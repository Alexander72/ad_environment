FROM php:7.2-fpm

RUN apt-get update && apt-get -y -f install gettext-base mysql-client libmemcached-dev zlib1g-dev mc

RUN pecl install redis-4.0.1 \
    && pecl install xdebug-2.6.0 \
    && docker-php-ext-enable redis xdebug

COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

COPY composer.phar /usr/local/bin/composer
