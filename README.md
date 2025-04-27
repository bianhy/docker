# Docker Images

- mysql 8.0
- redis 7.4.2
- nginx 1.22.3
- php   7.4.33


## Nginx+php

```
docker build -t nginx-php .

    ports:
        - "80:80"
    volumes:
        - ./docker_www:/data/www
```

## Mysql
```
docker build -t mysql:8.0 -f ./docker_images/Dockerfile_mysql .
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:8.0
```

## Redis
```
docker build -t redis:7.4.2 -f ./docker_images/Dockerfile_redis .
docker run -p 6379:6379 --name redis --restart=always --log-opt max-size=100m --log-opt max-file=2 -d redis:7.4.2
```
