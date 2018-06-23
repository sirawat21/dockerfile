FROM ubuntu:16.04
LABEL maintainer "Best Sira <sirawat21@gmail.com>"
RUN apt-get update -y \
    && apt-get install -y --no-install-recommends libgd-dev \
    && apt-get install -y curl php-cli php-mbstring git unzip snmp \
    && apt-get install php7.1 php7.1-cli php7.1-common php7.1-json php7.1-opcache php7.1-mysql php7.1-mbstring php7.1-mcrypt php7.1-zip php7.1-fpm \
    && rm -rf /var/lib/apt/lists/*
RUN curl -sS https://getcomposer.org/installer -o composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer
RUN echo "[PHP] \ndate.timezone = Asia/Bangkok \n short_open_tag = on " >> /etc/php/7.1/fpm/php.ini
VOLUME /www
WORKDIR /www
CMD php -S 0.0.0.0:80 -t /www
EXPOSE 80 443
