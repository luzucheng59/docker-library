# docker-library
常用docker镜像Dockerfile文件整理

## php镜像 - 基于php:7.2.14-fpm-alpine3.8构建

### 新增扩展
#### 核心扩展
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

#### pecl扩展
- memcached 3.1.3
- redis 4.2.0
- imagick 3.4.3
- swoole 4.2.12
- amqp 1.9.4

> 镜像大小：小于200M
