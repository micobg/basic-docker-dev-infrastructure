FROM php:apache
MAINTAINER Mihail Nikolov <micobg@gmail.com>

# Apache config active site
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
RUN apache2ctl configtest
COPY backend.conf /etc/apache2/sites-available
RUN a2ensite backend
RUN a2dissite 000-default
RUN rm /etc/apache2/sites-available/000-default.conf

# PHP PDO MySQL suppport
RUN docker-php-ext-install pdo pdo_mysql

EXPOSE 80
