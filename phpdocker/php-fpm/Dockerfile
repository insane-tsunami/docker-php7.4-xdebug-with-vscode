# FROM phpdockerio/php74-fpm:latest
# FROM phpdockerio/php80-fpm:latest
FROM phpdockerio/php:8.1-fpm
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update

# ## Install selected extensions and other stuff in php 7.4
# RUN apt-get -y --no-install-recommends install php7.4-memcached php7.4-mysql php7.4-xdebug php7.4-bz2

# ## Enable remote xdebug in php 7.4
# RUN echo "xdebug.remote_enable=on" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.mode=debug" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.idekey=VSCODE" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.client_host=host.docker.internal" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.log=/application/xdebug.logs" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.discover_client_host=1" >> /etc/php/7.4/mods-available/xdebug.ini
# RUN echo "xdebug.remote_connect_back=0" >> /etc/php/7.4/mods-available/xdebug.ini

# ## Install selected extensions and other stuff in php 8.0
# RUN apt-get -y --no-install-recommends install \
#     git \ 
#     php8.0-gd \ 
#     php8.0-imagick \ 
#     php8.0-memcached \ 
#     php8.0-mysql \ 
#     php8.0-xdebug \
#     php8.0-bz2

# ## Enable remote xdebug in php 8.0
# RUN echo "xdebug.remote_enable=on" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.mode=debug" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.idekey=VSCODE" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.client_host=host.docker.internal" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.log=/application/xdebug.logs" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.discover_client_host=1" >> /etc/php/8.0/mods-available/xdebug.ini
# RUN echo "xdebug.remote_connect_back=0" >> /etc/php/8.0/mods-available/xdebug.ini

## Install selected extensions and other stuff in php 8.1
RUN apt-get -y --no-install-recommends install \
    git \ 
    php8.1-gd \ 
    php8.1-imagick \ 
    php8.1-memcached \ 
    php8.1-mysql \ 
    php8.1-xdebug \
    php8.1-bz2

## Enable remote xdebug in php 8.1
RUN echo "xdebug.remote_enable=on" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.mode=debug" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.idekey=VSCODE" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.client_host=host.docker.internal" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.log=/application/xdebug.logs" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.discover_client_host=1" >> /etc/php/8.1/mods-available/xdebug.ini
RUN echo "xdebug.remote_connect_back=0" >> /etc/php/8.1/mods-available/xdebug.ini

# Install git
RUN apt-get -y install git 

# apt-get cleanup
RUN apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Update the PHP.ini file, enable <? ?> tags in php 7.4
# RUN sed -i "s/short_open_tag = Off/short_open_tag = On/" /etc/php/7.4/fpm/php.ini    
# RUN sed -i "s/asp_tags = Off/asp_tags = On/" /etc/php/7.4/fpm/php.ini
