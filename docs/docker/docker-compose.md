#### 安装docker-compose，运行下面的脚本可以自动安装，并且授权

```bsh
curl -L https://get.daocloud.io/docker/compose/releases/download/1.25.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```







#### 启动指定yml

docker-compose -f xx.yml up -d

