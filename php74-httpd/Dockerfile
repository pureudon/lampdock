FROM php:7.4-apache

RUN a2enmod rewrite

# install the PHP extensions we need
RUN apt-get update \
  # && apt-get install php7.3-mysql
  # && apt-get install -y libpng-dev libjpeg-dev libpq-dev \
  # && rm -rf /var/lib/apt/lists/* \
  # && docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
  # && docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip \
    # && docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql \
  && pecl install trader

RUN docker-php-ext-install mysqli pdo pdo_mysql

# option 2
# RUN apt-get update -y && apt-get install -y libpng-dev curl libcurl4-openssl-dev

# RUN docker-php-ext-install pdo pdo_mysql gd curl

# RUN a2enmod rewrite
# RUN service apache2 restart


WORKDIR /var/www/html