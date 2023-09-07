FROM php:8.1.23-fpm-alpine

## Install dependencies
RUN apk add libzip-dev \
    git \
    zip \
    unzip \
    && docker-php-ext-install \ 
    mysqli \
    pdo_mysql \
    bcmath \
    zip \
    exif

## Install Composer
COPY --from=composer /usr/bin/composer /usr/bin/composer 


