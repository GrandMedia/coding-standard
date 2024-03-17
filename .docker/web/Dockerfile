FROM php:8.2-apache

RUN apt update && apt dist-upgrade -y && \
    # DEPENDENCIES #############################################################
    apt install -y unzip git openssl && \
    # CLEAN UP #################################################################
    apt-get clean -y && apt-get autoclean -y && apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/* /var/lib/log/* /tmp/* /var/tmp/*

# COMPOSER #################################################################
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN mkdir /.composer
RUN chown 1000:1000 /.composer
