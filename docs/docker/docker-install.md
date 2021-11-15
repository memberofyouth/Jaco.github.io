#### 安装docker

```bsh
#升级yum
sudo yum update
#卸载旧版本docker
sudo yum remove docker  docker-common docker-selinux docker-engine
#安装依赖
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
#设置源
sudo yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
sudo yum makecache fast
#安装docker
sudo yum install docker-ce
#启动服务
sudo systemctl start docker
#查看版本
docker version


#拉取镜像
docker pull hello-world
#启动容器
docker run hello-world
```

#### 安装docker-compose，运行下面的脚本可以自动安装，并且授权

```bsh
curl -L https://get.daocloud.io/docker/compose/releases/download/1.25.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

