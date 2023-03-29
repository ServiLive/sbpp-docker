FROM php:8.1-fpm-alpine
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN curl -L https://github.com/sbpp/sourcebans-pp/archive/refs/heads/php81.zip -o sourcebans-pp.zip
# unzip sourcebans-pp.zip, and then copy the web directory that's inside it to /var/www/html
RUN unzip sourcebans-pp.zip && cp -r sourcebans-pp-php81/web/* /var/www/html/
WORKDIR /var/www/html/
RUN COMPOSER_ALLOW_SUPERUSER=1 composer install