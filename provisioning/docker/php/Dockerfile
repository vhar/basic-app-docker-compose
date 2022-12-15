FROM phpdockerio/php:8.1-fpm
WORKDIR "/var/www/html"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    php8.1-bz2 \
    php8.1-calendar \
    php8.1-common\
    php8.1-ctype \
    php8.1-curl \
    php8.1-dom \
    php8.1-fileinfo \
    php8.1-ftp \
    php8.1-gd \
    php8.1-gettext \
    php8.1-iconv \
    php8.1-interbase \
    php8.1-intl \
    php8.1-mbstring \
    php8.1-mysqli \
    php8.1-mysqlnd \
    php8.1-opcache \
    php8.1-pdo \
    php8.1-phar \
    php8.1-posix \
    php8.1-simplexml \
    php8.1-soap \
    php8.1-sockets \
    php8.1-tokenizer \
    php8.1-xdebug \
    php8.1-xml \
    php8.1-xmlreader \
    php8.1-xmlrpc \
    php8.1-xmlwriter \
    php8.1-xsl \
    php8.1-zip \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

ADD ./php.ini /etc/php/8.1/fpm/conf.d/90-php.ini
ADD ./www.conf /etc/php/8.1/fpm/pool.d/www.conf
ADD ./php.ini /etc/php/8.1/cli/conf.d/90-php.ini

RUN usermod -u 1000 www-data
