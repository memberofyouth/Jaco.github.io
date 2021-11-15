#### 修改为固定ip

```sh
vi /etc/sysconfig/network-scripts/ifcfg-ens192
```

添加：

```sh
BOOTPROTO="static"
IPADDR=192.168.0.29
GATEWAY=192.168.1.1
DNS1=192.168.1.1
DNS2=8.8.8.8
```

重启网络

```sh
service network restart
```

