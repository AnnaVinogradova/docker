FROM php:7.2.1-apache

RUN apt-get update

# extensions
RUN docker-php-ext-install pdo pdo_mysql mysqli

# config
RUN a2enmod rewrite
COPY 000-default.conf /etc/apache2/sites-available/

# composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
