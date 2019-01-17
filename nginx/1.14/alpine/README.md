# nginx1.14-alpine
基于docker官方 nginx:1.14.2-alpine 构建的镜像

Registry:
```
docker pull registry.cn-hangzhou.aliyuncs.com/azu/nginx1.14-alpine
```
> 镜像大小：7 MB

更新记录
==============================
2019-01-17
------------------------------
### 配置
- 新增全局变量配置，方便系统直接系统直接引用
- 新增默认域名配置 - my.domain.io