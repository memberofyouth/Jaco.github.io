#### mysql

```yaml
version: '3.6'
services:
  mysql:
    container_name: mysql
    image: mysql:8.0.15
    environment:
      TZ: Asia/Shanghai
      MYSQL_ROOT_PASSWORD: 123456
      # 初始化用户(不能是root 会报错, 后续需要给新用户赋予权限)
      MYSQL_USER: user
      # 用户密码
      MYSQL_PASSWORD: 123456
    command:
      --default-authentication-plugin=mysql_native_password
      --lower_case_table_names=1
      --character_set_server=utf8mb4
      --collation-server=utf8mb4_unicode_ci
      --explicit_defaults_for_timestamp=true
    volumes:
      - /data:/var/lib/mysql/
      - /etc/localtime:/etc/localtime:ro
      - /home/mysql/conf/:/etc/mysql/conf.d/
    ports:
      - 3306:3306
    networks:
      - default-network
    restart: always
networks:
  default-network:
    driver: bridge
```

### conf 文件夹创建my.conf

```shell
touch my.conf

[client]
default-character-set = utf8mb4
[mysql]
default-character-set = utf8mb4
[mysqld]
character-set-client-handshake = FALSE
character-set-server = utf8mb4
collation-server = utf8mb4_unicode_ci
init_connect='SET NAMES utf8mb4'
sql_mode=STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION


```

修改密码：

use mysql;

ALTER USER ‘test’@‘localhost’ IDENTIFIED WITH MYSQL_NATIVE_PASSWORD BY ‘新密码’;

```bash
-- 创建用户
CREATE USER 'username'@'%' IDENTIFIED BY 'password';

-- 授权使用数据库
GRANT ALL ON *.* TO 'username'@'%';

GRANT ALL PRIVILEGES ON *.* TO ‘myuser‘@‘%‘ IDENTIFIED BY ‘mypass‘ WITH GRANT OPTION;

GRANT ALL PRIVILEGES ON xinlian.* TO 'xinlian';

撤销所有权限：
REVOKE ALL PRIVILEGES,GRANT OPTION FROM 'xinlian';
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

