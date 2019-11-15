FROM php:7.4.0RC6-fpm

RUN docker-php-ext-install pdo_mysql

RUN pecl install xdebug-2.8.0beta2 \
  && echo "zend_extension=$(find /usr/local/lib/php/extensions/ -name xdebug.so)" > /usr/local/etc/php/conf.d/xdebug.ini;

RUN docker-php-ext-enable xdebug

WORKDIR /var/www/

CMD ["php-fpm"]

EXPOSE 9000
