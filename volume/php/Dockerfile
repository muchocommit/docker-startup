FROM muchocommit/symfony:latest

ARG build_dir

WORKDIR ${build_dir:-/usr/local/var/www/projects/docker-startup}

RUN chown -R www-data:www-data ${build_dir:-/usr/local/var/www/projects/docker-startup}

USER www-data
