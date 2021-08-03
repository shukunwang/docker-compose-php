FROM php:7.4-fpm-alpine

# 常用工具
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    && docker-php-ext-install pdo_mysql \
    && apk add ${PHPIZE_DEPS} \
    && pecl install redis-4.0.1 \
    && docker-php-ext-enable redis \
    && apk del ${PHPIZE_DEPS}

# 复制准备好的配置文件
COPY ./config/php.ini /usr/local/etc/php/conf.d/
COPY ./config/opcache-recommended.ini /usr/local/etc/php/conf.d/
