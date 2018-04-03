FROM ubuntu:latest
ENV HTTP_PROXY=http://
ENV HTTPS_PROXY=http://
ENV http_proxy=http://
ENV https_proxy=http://

RUN apt-get update && apt-get install -y \
	apache2 \
	openjdk-8-jdk \
	nano \
	wget

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80

CMD apache2ctl -D FOREGROUND 
