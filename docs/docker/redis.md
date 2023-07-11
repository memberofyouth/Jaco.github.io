#### redis
```yaml
version: '3.5'
services:
    redis:
    	restart: always
        image: redis:5.0.4-alpine
        container_name: redis
        command: redis-server --requirepass 123456
        volumes:
        - /home/redis/data:/data
        ports:
        - 6379:6379  

environment:
            - ALLOW_EMPTY_PASSWORD=yes
```

配置文件方式启动

```shell
version: '3.5'
services:
    redis:
    	restart: always
        image: redis:5.0.4-alpine
        container_name: redis
        command: redis-server /etc/redis/redis.conf 
        volumes:
        - /home/redis/data:/data
        - ./redis.conf:/etc/redis/redis.conf
        network_mode: host
        environment:
          TZ: "Asia/Shanghai"

```

当前文件夹新建 redis.conf

redis.conf

```
masterauth 'cde34rfv'

requirepass 'cde34rfv'
```



```
docker run -p 6379:6379 --name redis --restart=always -v C:\redis\data:/data -v C:\redis\conf\redis.conf:/etc/redis/redis.conf -d redis:3.2 redis-server /etc/redis/redis.conf 

```
