ssh 公钥登录

```shell
执行命令生成公私钥：
ssh-keygen -t rsa
查看公私钥：
ls ~/.ssh/
id_rsa id_rsa.pub known_hosts
将公钥复制到被管理机器上面：
scp ~/.ssh/id_rsa.pub root@192.168.0.1:~/.ssh/authorized_keys
```

