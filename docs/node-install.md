

```shell
yum info epel-release


yum install epel-release -y


sudo yum install nodejs -y



升级

安装node管理软件 n

npm install -g n

n latest


n   #安装
 
切换失效解决：
which node

配置环境变量

export N_PREFIX=/usr/local/bin/node #node实际安装位置
export PATH=$N_PREFIX/bin:$PATH


ln -s /usr/local/bin/node/bin/node  /usr/local/bin/node



安装json-server

npm install -g json-server

nohup json-server --watch ./mock/db.json --port 9999 &
```



