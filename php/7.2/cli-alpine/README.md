# php7.2.15-cli-alpine
基于docker官方 php:7.2.15-cli-alpine 构建的镜像, 新增常用扩展，满足日常开发需求。

Registry:
```
docker pull luzucheng/php7.2.15-cli-alpine-ext:1.2
```
> 镜像大小(压缩后)：68 M

更新记录
==============================
2019-03-08
------------------------------
### 新增扩展
- pcntl
- event 2.4.3

==============================
2019-01-29
------------------------------
### 空间
- 优化php配置

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
- memcached 3.1.3
- redis 4.2.0
- imagick 3.4.3
- swoole 4.2.12