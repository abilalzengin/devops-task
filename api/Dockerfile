FROM php:7.1-apache

RUN apt-get update && apt-get install -y \
        unixODBC-dev \
        && pecl install pdo_sqlsrv \
        && docker-php-ext-enable pdo_sqlsrv

COPY QuickDbTest.php /var/www/html/

RUN chown -R www-data:www-data /var/www/html

CMD ["apache2-foreground"]

