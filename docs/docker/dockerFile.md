#### redis
```yaml
version: '3.5'
services:
    razzil-redis:
        image: redis:5.0.4-alpine
        container_name: razzil-redis
        environment:
            - ALLOW_EMPTY_PASSWORD=yes
        volumes:
            - /var/zhigui/volumes/razzil/redis/:/data
        ports:
            - 6379:6379  
```

#### mysql

```yaml
version: '3.5'
services:
    razzil-mysql:
        image: mysql:8.0.15
        container_name: razzil-mysql
        volumes:
            - /var/zhigui/volumes/razzil/mysql/:/var/lib/mysql/
        environment:
            - MYSQL_USER=root
            - MYSQL_ALLOW_EMPTY_PASSWORD=yes
            - MYSQL_DATABASE=razzil
        ports:
            - 3306:3306
        command: mysqld --lower_case_table_names=1 --skip-ssl --character_set_server=utf8mb4 --collation-server=utf8mb4_unicode_ci --explicit_defaults_for_timestamp
```


#### mysql-3

```yml
version: '3.5'
services:
    razzil-mysql:
        restart: always
        image: mysql:8.0.15
        container_name: razzil-mysql
        volumes:
            - /var/zhigui/volumes/razzil/mysql/:/var/lib/mysql/
        environment:
            - MYSQL_ROOT_PASSWORD=!1qazxsw2
            - MYSQL_USER=user
            - MYSQL_PASS=!1qazxsw2
            - MYSQL_DATABASE=razzil
        ports:
            - 3306:3306
        command: mysqld --lower_case_table_names=1 --skip-ssl --character_set_server=utf8mb4 --collation-server=utf8mb4_unicode_ci --explicit_defaults_for_timestamp
```

#### mysql-5.7

```yml
version: '3.5'
services:
  mysql-server1:
    image: mysql:5.7
    restart: always
    container_name: mysql-server
    ports:
      - 3306:3306
    # network_mode: host
    environment:
      - MYSQL_ROOT_PASSWORD=123456
    volumes:
      - /etc/localtime:/etc/localtime:ro
      - ./mysqld.cnf:/etc/mysql/mysql.conf.d/mysqld.cnf
      - /data:/var/lib/mysql

```

```yml
[mysqld]
pid-file    = /var/run/mysqld/mysqld.pid
socket      = /var/run/mysqld/mysqld.sock
datadir     = /var/lib/mysql
# log-error  = /var/log/mysql/error.log
symbolic-links=0

character-set-server = utf8mb4

log-bin       = mysql-bin  # Binary log name $(datadir)/$(log-bin)
binlog_format = row 

server-id     = 1613306    # Must be the only
# gtid_mode     = on
# enforce_gtid_consistency = on

# [client]  # [mysql]
[mysql]
default-character-set = utf8mb4


```



#### Java8 带字体

```yml
·1 ### 创建 Dockerfile 
FROM java:8-jre-alpine
# Install cURL
RUN echo -e "https://mirror.tuna.tsinghua.edu.cn/alpine/v3.4/main\n\
https://mirror.tuna.tsinghua.edu.cn/alpine/v3.4/community" > /etc/apk/repositories

RUN apk --update add curl bash ttf-dejavu && \
      rm -rf /var/cache/apk/*

·2 ### 构建镜像
docker build -t docker.io/java-font:8-jre-alpine .

```

