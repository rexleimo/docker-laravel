FROM rainbowmorel/php-cli

MAINTAINER "傻梦兽" <rainbowmorel@163.com>

WORKDIR /tmp

RUN apt-get update -y && \
apt-get install -y curl git php-mcrypt php-gd && \
apt-get install -y php-curl && \
apt-get install -y php-mysql && \
apt-get install -y php-mbstring && \
apt-get install -y php-xml && \
apt-get install -y unzip && \
curl -sS https://getcomposer.org/installer | php && \
mv composer.phar /usr/local/bin/composer && \
composer self-update && \
apt-get remove --purge curl -y && \
apt-get clean && \
composer config -g repo.packagist composer https://packagist.phpcomposer.com

RUN mkdir -p /data/www
VOLUME [ "/data" ]
WORKDIR /data/www

ENTRYPOINT [ "composer" ]
CMD [ "--help" ]
