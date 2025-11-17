FROM php:7.4-apache
RUN sed -i 's|http://deb.debian.org/debian/|http://ftp.debian.org/debian/|g' /etc/apt/sources.list
RUN apt-get update -y
RUN docker-php-ext-install mysqli
COPY ./mompopcafe /var/www/html/
RUN apachectl restart
EXPOSE 80
