FROM php:7.4-apache

RUN docker-php-ext-install pdo pdo_mysql mysqli

COPY 000-default.conf /etc/apache2/sites-available/000-default.conf

RUN a2enmod rewrite