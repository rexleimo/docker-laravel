FROM rainbowmorel/ubuntu:16.04

MAINTAINER "傻梦兽" <rainbowmorel@163.com>

#安装 Nginx
#必须吧deamon 关闭
RUN apt-get install -y nginx \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
&& echo "daemon off;" >> /etc/nginx/nginx.conf

RUN mkdir -p /data
VOLUME [ "/data" ]

WORKDIR /etc/nginx

# PORTS
EXPOSE 80 443

CMD [ "nginx" ]