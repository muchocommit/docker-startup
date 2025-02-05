# Startup Docker project with PHP-FPM unix socket + Xdebug + Nginx ###

### Create .env file in root directory
<pre>
PROJECT_ROOT=/usr/local/var/www/projects/docker-startup
PROJECT_DIR=startup
DOCUMENT_PATH=/usr/local/var/www/projects/docker-startup/startup/public
</pre>

### Build images and run containers
Run `docker compose build` <br>
Run `docker-compose up -d`

### Why is it useful?
Rootless users for php and nginx containers provide extra security. <br>
Php-fpm connects with nginx via unix socket, which means php port is not exposed. <br>
Config files in docker-compose.yml include php-fpm setup and xdebug settings for integration with IDE.
