FROM php:7.4-apache

RUN apt update -y
RUN apt upgrade -y

RUN apt install -y libicu-dev curl
RUN docker-php-ext-install intl mysqli pdo pdo_mysql
RUN docker-php-ext-enable intl
RUN docker-php-ext-enable mysqli
RUN docker-php-ext-enable pdo
RUN docker-php-ext-enable pdo_mysql

COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite

RUN apt clean -y

EXPOSE 80