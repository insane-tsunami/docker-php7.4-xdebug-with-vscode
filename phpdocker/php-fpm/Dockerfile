FROM phpdockerio/php74-fpm:latest
WORKDIR /application

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff#
RUN apt-get update
RUN apt-get -y --no-install-recommends install php7.4-memcached php7.4-mysql php7.4-xdebug php7.4-bz2

# Enable remote xdebug
RUN echo "xdebug.remote_enable=on" >> /etc/php/7.4/mods-available/xdebug.ini

# Install git
RUN apt-get -y install git 

# apt-get cleanup
RUN apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

# Update the PHP.ini file, enable <? ?> tags
RUN sed -i "s/short_open_tag = Off/short_open_tag = On/" /etc/php/7.4/fpm/php.ini    
RUN sed -i "s/asp_tags = Off/asp_tags = On/" /etc/php/7.4/fpm/php.ini
