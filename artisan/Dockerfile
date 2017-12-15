FROM php-cli:v1

MAINTAINER "傻梦兽" <rainbowmorel@163.com>
WORKDIR /tpm

RUN apt-get update -y && \
apt-get install -y \
php-mcrypt \
php-mongodb \
php-mysql \
php-pgsql \
php-redis \
php-sqlite3 \
imagemagick \
php-imagick \
php-gd

RUN mkdir -p /data/www
VOLUME [ "/data" ]
WORKDIR /data/www

ENTRYPOINT [ "php","artisan" ]
CMD [ "--help" ]