# Laravel5.1
[继承镜像sixbyte/fpm56:0.1](https://github.com/sixbyter/docker-fpm5.6)

一个Laravel5.1的镜像, 其实就是在我的php镜像增加了nodeJs的支持

## 使用

#### 创建镜像
```
docker build -t yourimagename .
```

#### 使用镜像,创建容器
```
docker run -d \
-v /path/to/www:/var/www \
-v /path/to/php-fpm.conf:/usr/local/etc/php-fpm.conf \
-v /path/to/php.ini:/usr/local/etc/php/php.ini:ro \
-p 9000:9000
--name fpm56 \
yourimagename
```