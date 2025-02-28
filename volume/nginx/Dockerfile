FROM nginx:stable

ARG USERNAME=nginx
ARG build_dir

RUN apt update && apt install -y nano htop net-tools lsof
WORKDIR ${build_dir:-/usr/local/var/www/projects/docker-startup}

RUN usermod -d /var/cache/nginx nginx --shell /bin/bash && usermod -a -G www-data nginx
RUN chown -R $USERNAME:0 /etc/nginx /var/cache /var/log/nginx /var/run /tmp

USER $USERNAME
