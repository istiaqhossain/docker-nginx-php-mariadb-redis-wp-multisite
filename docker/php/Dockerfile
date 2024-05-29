FROM php:8.3-fpm-alpine

## Install dependencies
RUN apk add libzip-dev \
    git \
    zip \
    unzip \
    libpng-dev \
    libwebp-dev \
    libjpeg-turbo-dev \
    freetype-dev \
    && docker-php-ext-configure gd --with-webp=/usr/include/webp --with-jpeg=/usr/include --with-freetype=/usr/include/freetype/ \
    && docker-php-ext-install \ 
    mysqli \
    pdo_mysql \
    bcmath \
    zip \
    exif \
    gd  

## Install Composer
COPY --from=composer /usr/bin/composer /usr/bin/composer 


