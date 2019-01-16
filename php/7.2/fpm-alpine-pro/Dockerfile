#
# 基于 alpine php7.2基础镜像
#

FROM php:7.2.14-fpm-alpine3.8

LABEL maintainer="765131678@qq.com" \
    version="1.0" \
    description="基于alpine php7.2镜像扩展"

# install base rely on
# search by https://pkgs.alpinelinux.org/packages
# alpine not include gcc g++ make
RUN apk --update add --no-cache gcc g++ make \
    autoconf \
    bzip2 \
    bzip2-dev \
    binutils \
    cyrus-sasl-dev \
    freetype-dev \
    git \
    icu-dev \
    libc-dev \
    icu-dev \
    libpcre32 \
    libbz2 \
    # libxml2 \
    # libxml2-utils \
    \
    imagemagick-dev \
    libjpeg-turbo-dev \
    libpng-dev \
    libmcrypt-dev \
    libmemcached-dev \
    openldap-dev \
    rabbitmq-c \
    rabbitmq-c-dev

# install core extensions
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd \
    && docker-php-ext-install mysqli \
    && docker-php-ext-install bz2 \
    && docker-php-ext-install zip \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install opcache \
    && docker-php-ext-install ldap \
    && docker-php-ext-install sockets \
    && docker-php-ext-install bcmath \
    && docker-php-ext-install sysvmsg \
    && docker-php-ext-install sysvsem \
    && docker-php-ext-install sysvshm \
    # xmlrpc install fail
    # && docker-php-ext-install xmlrpc \
    \
    # install pecl state version extensions
    # search from https://pecl.php.net/package-search.php
    \
    # install memcached
    && pecl install memcached 3.1.3 \
    && docker-php-ext-enable memcached \
    \
	# install redis
    && pecl install redis 4.2.0 \
    && docker-php-ext-enable redis \
    \
    # install mcrypt fail
    # && pecl install mcrypt 1.0.2 \
    # && docker-php-ext-enable mcrypt \
    \
    # install imagick
    && pecl install imagick 3.4.3 \
    && docker-php-ext-enable imagick \
    \
    # install swoole
    && pecl install swoole 4.2.12 \
    && docker-php-ext-enable swoole \
    \
    # install amqp
    && pecl install amqp 1.9.4 \
    && docker-php-ext-enable amqp \
    \
    && pecl update-channels \
    && rm -rf /var/cache/apk/* \
    && rm -rf /tmp/pear

ENTRYPOINT ["docker-php-entrypoint"]

EXPOSE 9000

CMD ["php-fpm"]