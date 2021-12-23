#### 镜像加速

sudo mkdir -p /etc/docker

 sudo tee /etc/docker/daemon.json <<-'EOF' 

{  

​	"registry-mirrors": ["https://dit3s2mx.mirror.aliyuncs.com"]

 } 

EOF 

sudo systemctl daemon-reload 

sudo systemctl restart docker