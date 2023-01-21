FROM php:8.1-apache

RUN apt update \
    && apt install -y ffmpeg zlib1g-dev libpng-dev libjpeg-dev

RUN docker-php-ext-configure gd --with-jpeg \
    && docker-php-ext-install gd

ENV ALLSKY_CONFIG /var/www/html
ENV ALLSKY_VIDEOS .
ENV ALLSKY_KEOGRAMS .
ENV ALLSKY_STARTRAILS .

WORKDIR /var/www/html

ADD . .
