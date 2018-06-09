FROM php:5.6-apache
LABEL maintainer "Best Sira <sirawat21@gmail.com>"
ENV ENVIRONMENT production
RUN echo "[PHP] \ndate.timezone = Asia/Bangkok" >> /usr/local/etc/php/php.ini
RUN apt-get update -y \
    && apt-get install -y --no-install-recommends libgd-dev \
    && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install mysqli gd
RUN a2enmod rewrite
RUN echo "<?php phpinfo(); " > /var/www/html/index.php
RUN chmod 777 /var/www/html/index.php
VOLUME [ "/var/www/html" ]
EXPOSE 80 443
