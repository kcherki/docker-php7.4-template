FROM php:8.1-apache

# Installation des dépendances PHP et extensions nécessaires pour CakePHP
RUN apt-get update --fix-missing && \
    apt-get install -y \
        libpng-dev \
        libjpeg62-turbo-dev \
        libfreetype6-dev \
        libicu-dev \
        libxml2-dev \
        libzip-dev \
        zip \
        unzip \
        git \
        curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Installation des extensions PHP requises pour CakePHP
RUN docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-configure intl \
    && docker-php-ext-install -j$(nproc) \
        gd \
        intl \
        pdo \
        pdo_mysql \
        zip \
        soap \
        opcache

# Installation de Composer de manière plus sûre
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

# Activation du mod_rewrite pour Apache
RUN a2enmod rewrite

# Configuration d'Apache pour permettre .htaccess
RUN sed -i '/<Directory \/var\/www\/>/,/<\/Directory>/ s/AllowOverride None/AllowOverride All/' /etc/apache2/apache2.conf

# Configuration des permissions
RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html

WORKDIR /var/www/html