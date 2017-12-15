FROM ubuntu:16.04

MAINTAINER "傻梦兽" <rainbowmorel@163.com>

ADD sources.list /etc/apt/sources.list

RUN apt-get clean && \
apt-get update && \
apt-get install vim -y

# Define working directory.
WORKDIR /root

CMD [ "ture" ]