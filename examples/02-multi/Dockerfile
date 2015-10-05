FROM php:5.6-fpm

# Install packages and extensions
RUN apt-get update -y && apt-get install -y \
    git \
    zlib1g-dev\
    && rm -rf /var/lib/apt/lists/* \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install zip

# Install Composer
ENV COMPOSER_VERSION 1.0.0-alpha10
RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/local/bin --filename=composer --version=${COMPOSER_VERSION}

# Configure php
COPY ./conf/php.ini /usr/local/etc/php/conf.d/default.ini

# Bundle app source
COPY . /srv

# Install app dependencies
RUN cd /srv; composer install

EXPOSE 9000
CMD ["php-fpm"]