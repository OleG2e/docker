FROM php:8.1-fpm

RUN apt update \
    && apt install -y zlib1g-dev libpng-dev libexpat1-dev libicu-dev libfreetype6-dev libjpeg-dev zip \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd intl \
    && rm -rf /var/lib/apt/lists/*

COPY php.ini /usr/local/etc/php/conf.d/php-custom-conf.ini

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

EXPOSE 9000
