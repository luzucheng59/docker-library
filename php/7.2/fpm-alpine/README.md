# php7.2-fpm-alpine
基于docker官方 php:7.2.14-fpm-alpine3.8 构建的镜像

更新记录
==============================
2019-01-17 (2.0)
------------------------------
### 空间
- 优化配置，缩减镜像大小
> 镜像大小：小于200M

2019-01-15 (1.0)
------------------------------
### 新增核心扩展
- gd
- mysqli
- bz2
- zip
- pdo_mysql
- opcache
- ldap
- sockets
- bcmath
- sysvmsg
- sysvsem
- sysvshm

### 新增pecl扩展
- memcached 3.1.3
- redis 4.2.0
- imagick 3.4.3
- swoole 4.2.12
- amqp 1.9.4

> 镜像大小：300M+
