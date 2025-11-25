# [Postgres](https://hub.docker.com/_/postgres) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | 이미지 이름|
| [IMAGE_TAG] | 이미지 태그 또는 버전. latest|
| [CONTAINER_NAME] | CONTAINER_NAME |
| [POSTGRES_DB] | POSTGRES_DB |
| [POSTGRES_USER] | POSTGRES_USER |
| [POSTGRES_PASSWORD] | POSTGRES_PASSWORD |

# Containing
Usage :

```bash
docker run -d \
-p 5432:5432 \
-e POSTGRES_HOST_AUTH_METHOD=trust \
-e POSTGRES_DB=[POSTGRES_DB] \
-e POSTGRES_USER=[POSTGRES_USER] \
-e POSTGRES_PASSWORD=[POSTGRES_PASSWORD] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 5432:5432 \
-e POSTGRES_HOST_AUTH_METHOD=trust \
-e POSTGRES_DB=guest \
-e POSTGRES_USER=guest \
-e POSTGRES_PASSWORD=guest \
--name guest-postgres \
postgres:16.4-alpine3.20
```


# Package

```bash
docker build -t ghcr.io/u2waremanager/postgres:16.4-alpine3.20 .
```

# Publish
```bash
docker push ghcr.io/u2waremanager/postgres:16.4-alpine3.20
```

# Install
```bash
docker pull ghcr.io/u2waremanager/postgres:16.4-alpine3.20
```
