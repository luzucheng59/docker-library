# php7.2-fpm-alpine
基于docker官方 php:5.6-fpm-alpine 构建的镜像。

Registry:
```
docker pull luzucheng/php5.6-fpm-alpine-ext:latest
```
> 镜像大小：68 M

更新记录
==============================
2019-03-08
------------------------------
### 新增扩展
- pcntl
- event 2.0.0

2019-01-17
------------------------------
### 空间
- 优化配置，缩减镜像大小

2019-01-15
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
- redis 4.2.0
- imagick 3.4.3