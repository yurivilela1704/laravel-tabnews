FROM php:8.3-fpm

RUN apt-get update && apt-get install -y \
    git curl unzip \
    libpq-dev \
    libzip-dev \
    libpng-dev libjpeg62-turbo-dev libfreetype6-dev \
    libonig-dev libxml2-dev \
  && docker-php-ext-configure gd --with-freetype --with-jpeg \
  && docker-php-ext-install -j$(nproc) \
     pdo_pgsql mbstring exif pcntl bcmath gd zip opcache \
  && rm -rf /var/lib/apt/lists/*

# Composer
COPY --from=composer:2.7 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www

# Add user setup for host UID/GID
ARG UID=1000
ARG GID=1000

RUN groupadd -g $GID laravel && \
    useradd -u $UID -g laravel -m laravel

USER laravel
