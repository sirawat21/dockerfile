FROM ubuntu:16.04
LABEL maintainer "Best Sira <sirawat21@gmail.com>"
RUN apt-get update -y \
    && apt-get install -y --no-install-recommends libgd-dev \
    && apt-get install -y curl php-cli php-mbstring git unzip \
    && apt-get install -y php7.0 php7.0-fpm php7.0-mysql \
    && rm -rf /var/lib/apt/lists/*
RUN curl -sS https://getcomposer.org/installer -o composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer
RUN echo "[PHP] \ndate.timezone = Asia/Bangkok \n short_open_tag = on " >> /etc/php/7.0/fpm/php.ini
VOLUME ["/www"]
WORKDIR ["/www"]
CMD php -S 0.0.0.0:80 -t ./
EXPOSE 80 443
