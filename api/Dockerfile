FROM php:8.2-fpm

ARG PHP_VERSION="8.2"

RUN apt-get update \
  && apt-get install -y libzip-dev libpq-dev git wget lsb-release gnupg sudo

# INSTALLATION DE POSTGRES 15 POUR GERER DES EXPORTS
# RUN echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list && \
#   wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add - && \
#   apt-get update && \
#   apt install -y postgresql-15
# RUN docker-php-ext-install pdo pdo_pgsql pgsql

RUN docker-php-ext-install zip

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

COPY ./script/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

WORKDIR /var/www

ENTRYPOINT ["/entrypoint.sh"]