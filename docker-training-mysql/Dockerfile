FROM ubuntu:latest

ENV HTTP_PROXY=http://
ENV HTTPS_PROXY=http://
ENV http_proxy=http://
ENV https_proxy=http://

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y \
    apache2 \
    php7.0 \
    libapache2-mod-php7.0 \
    mysql-server \
    curl

 RUN sed -i -e"s/^bind-address\s*=\s*127.0.0.1/bind-address = 0.0.0.0/" /etc/mysql/my.cnf 

 RUN mkdir -p /var/run/mysqld

 EXPOSE 3306

 CMD apache2ctl -D FOREGROUND