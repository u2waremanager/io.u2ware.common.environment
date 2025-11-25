# [Mysql](https://hub.docker.com/_/mysql) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | 이미지 이름|
| [IMAGE_TAG] | 이미지 태그 또는 버전. latest|
| [HOST_PORT] | HOST_PORT|
| [HOST_VOLUMN] | HOST_VOLUMN|
| [CONTAINER_NAME] | CONTAINER_NAME |
| [MYSQL_DATABASE] | MYSQL_DATABASE |
| [MYSQL_USER] | MYSQL_USER |
| [MYSQL_PASSWORD] | MYSQL_PASSWORD |

, 

# Containing
Usage :

```bash
docker run -d \
-p [HOST_PORT]:3306 \
-v [HOST_VOLUMN]:/var/lib/mysql \
-e MYSQL_DATABASE=[MYSQL_DATABASE] \
-e MYSQL_USER=[MYSQL_USER] \
-e MYSQL_PASSWORD=[MYSQL_PASSWORD] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 3306:3306 \
-e MYSQL_DATABASE=guest \
-e MYSQL_USER=guest \
-e MYSQL_PASSWORD=guest \
--name guest-mysql \
mysql:9.5.0
```


# Package

```bash
docker build \
--platform linux/arm64,linux/amd64 \
-t ghcr.io/u2waremanager/io.u2ware.common.environment:mysql-9.5.0 \
.
```

# Publish
```bash
docker push ghcr.io/u2waremanager/io.u2ware.common.environment:mysql-9.5.0
```

# Install
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.common.environment:mysql-9.5.0
```

