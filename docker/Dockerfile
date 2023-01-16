FROM php:8.1-apache

RUN apt update && \
    apt install -y ffmpeg zlib1g-dev libpng-dev libjpeg-dev

RUN docker-php-ext-configure gd --with-jpeg && \
    docker-php-ext-install gd

WORKDIR /var/www/html

ENV ALLSKY_CONFIG /var/www/html
ENV ALLSKY_VIDEOS /var/www/html/videos
ENV ALLSKY_KEOGRAMS /var/www/html/keograms
ENV ALLSKY_STARTRAILS /var/www/html/startrails

ADD . .
