#### redis
```yaml
version: '3.5'
services:
    redis:
        image: redis:5.0.4-alpine
        container_name: redis
        command: redis-server --requirepass 123456
        volumes:
        - /var/zhigui/volumes/razzil/redis/:/data
        ports:
        - 6379:6379  

environment:
            - ALLOW_EMPTY_PASSWORD=yes
```

```
docker run -p 6379:6379 --name redis --restart=always -v C:\redis\data:/data -v C:\redis\conf\redis.conf:/etc/redis/redis.conf -d redis:3.2 redis-server /etc/redis/redis.conf 

```
