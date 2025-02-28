FROM php:8.3-fpm-bookworm

ARG build_dir

RUN pecl install xdebug-3.3.2 && docker-php-ext-enable xdebug
RUN mkdir /socket
WORKDIR ${build_dir:-/usr/local/var/www/projects/docker-startup}

RUN chown -R www-data:www-data ${build_dir:-/usr/local/var/www/projects/docker-startup} /socket

USER www-data
