FROM gbrayhan/debian10-php7.4:v1.0
# docker image gbrayhan/php74-xdebug:v1.0
MAINTAINER Alejandro Guerrero (gbrayhan@gmail.com)

RUN apt-get install php7.4-xdebug; \
echo "xdebug.remote_enable = 1 \n  " >> /etc/php/7.4/mods-available/xdebug.ini ;
