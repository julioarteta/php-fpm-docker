FROM julioarteta/php-fpm:wordpress-7.3
MAINTAINER Julio R. Arteta<julioarteta93@gmail.com>

ARG uid
ARG gid

RUN apk --no-cache add shadow && \
    usermod -u $uid www-data && \
    groupmod -g $gid www-data

#RUN rc-service php-fpm7 

COPY php-fpm.conf /etc/php/7.3/fpm/pool.d/www.conf
COPY php.ini /etc/php/7.0/mods-available/php.ini

WORKDIR /etc/php/7.3/fpm/conf.d/
RUN ln -s /etc/php/7.3/mods-available/php.ini 00-php.in


WORKDIR /var/www/html

#CMD ["/usr/sbin/php-fpm7.2"]



