FROM php:8.2-fpm

WORKDIR /var/www/html

RUN apt-get update \
        && apt-get install -y git acl openssl openssh-client wget zip vim librabbitmq-dev libssh-dev \
        && apt-get install -y libpng-dev zlib1g-dev g++ libzip-dev libxml2-dev libicu-dev \
        && docker-php-ext-install pdo_mysql && docker-php-ext-enable pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]