FROM ubuntu:latest

ENV HTTP_PROXY=http://
ENV HTTPS_PROXY=http://
ENV http_proxy=http://
ENV https_proxy=http://

RUN apt-get -y update && apt-get -y upgrade && apt-get install -y \
    openjdk-8-jdk \
    wget

RUN mkdir /usr/local/tomcat
RUN wget http://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.29/bin/apache-tomcat-8.5.29.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-8.5.29/* /usr/local/tomcat/

EXPOSE 8080

CMD /usr/local/tomcat/bin/catalina.sh run
