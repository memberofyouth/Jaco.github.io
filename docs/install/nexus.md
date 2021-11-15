```yml
version: '3'

services:
  nexus:
      container_name: nexus
      restart: always
      image: sonatype/nexus3:3.17.0
      volumes:
        - /srv/docker/nexus/nexus-data:/nexus-data:Z
      ports:
        - "8081:8081"
        - "8082:8082"
```



## 安装和运行Nexus

mkdir -p /srv/docker/nexus/nexus-data && chown -R 200 /srv/docker/nexus/nexus-data



查看日志：

```bash
docker-compose logs -f
```

Debug:

```bash
docker-compose exec nexus /bin/bash
```



配置私服地址以便于登录使用



````
vi /etc/docker/daemon.json

{
       "insecure-registries": ["192.168.0.51:8082"],
       "registry-mirrors": ["http://192.168.0.51:8082"]
}

——> 保存

保存后 登录 ： docker login 192.168.0.51:8082
````

