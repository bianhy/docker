# Docker
> 

## Nginx1.22.1+php7.4镜像
```
docker build -t nginx-php .

    ports:
        - "80:80"
    volumes:
        - ./docker_www:/data/www
```

## Mysql8.0镜像
```
docker build -t mysql:8.0 ./docker_images/Dockerfile_mysql
docker run -p 3306:3306 --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:8.0
```

## Redis7.4.2镜像
```
docker build -t redis:7.4.2 ./docker_images/Dockerfile_redis
docker run -p 6379:6379 --name redis --restart=always --log-opt max-size=100m --log-opt max-file=2 -d redis:7.4.2

```
