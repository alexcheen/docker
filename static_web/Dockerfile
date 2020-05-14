# Version: 0.0.1


FROM ubuntu:16.04
MAINTAINER Alex Cheen "cheen2012@gmail.com"
ENV REFRESHED_AT 2020-05-14
RUN apt-get -yqq update && apt-get -yqq install nginx
RUN mkdir -p /var/www/html/website
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80