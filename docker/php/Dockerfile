FROM php:7.2-fpm

RUN apt-get update \
    && apt-get install -y \
        git autoconf pkg-config libssl-dev

RUN docker-php-ext-install \
        pdo \
        pdo_mysql \
        bcmath

RUN php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/local/bin --filename=composer \
    && chmod +x /usr/local/bin/composer

RUN curl -LsS https://symfony.com/installer -o /usr/local/bin/symfony \
    && chmod a+x /usr/local/bin/symfony
