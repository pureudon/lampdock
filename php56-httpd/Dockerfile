FROM php:5.6-apache

RUN a2enmod rewrite

# install the PHP extensions we need
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libpq-dev \
  && rm -rf /var/lib/apt/lists/* \
  && docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
  && docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip

# option 2
# RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev

# RUN docker-php-ext-install pdo pdo_mysql gd curl

# RUN a2enmod rewrite
# RUN service apache2 restart


WORKDIR /var/www/html