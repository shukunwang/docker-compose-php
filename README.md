# docker-compose-php
docker-compose搭建Docker化的PHP开发环境(PHP-FPM + Mysql + Nginx + Redis)

基本用法：

```
docker-compose up --build

docker-compose down
```

基于Mac新款M1上安装Mysql：

```
services:
  db:
    platform: linux/x86_64
    image: mysql
    ...
```
or
```
services:
  db:
    image: mariadb:10.5.8
    ...
```
