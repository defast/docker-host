FROM php:7.3-apache

RUN apt-get update && apt-get install -y \
    libzip-dev \
    zip \
    libjpeg-dev \
    libpng-dev \
  && docker-php-ext-configure zip --with-libzip \
  && docker-php-ext-configure gd \
    --with-gd \
    --with-freetype-dir=/usr/include/freetype2 \
    --with-png-dir=/usr/include \
    --with-jpeg-dir=/usr/include \
  && docker-php-ext-install zip \
  && docker-php-ext-install gd \
  && docker-php-ext-install opcache \
  && docker-php-ext-install mysqli \
  && docker-php-ext-enable gd