FROM php:8.2-fpm

WORKDIR /var/www/html

RUN apt-get update && \
    apt-get install -y --force-yes --no-install-recommends \
        libmemcached-dev \
        libzip-dev \
        libz-dev \
        libzip-dev \
        libpq-dev \
        libjpeg-dev \
        libpng-dev \
        libfreetype6-dev \
        libssl-dev \
        openssh-server \
        libmagickwand-dev \
        git \
        cron \
        nano \
        libxml2-dev \
        libreadline-dev \
        libgmp-dev \
        mariadb-client \
        unzip

RUN docker-php-ext-install zip pdo_mysql pdo_pgsql bcmath dom sockets
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

