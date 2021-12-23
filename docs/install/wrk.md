### 性能测试工具

centos 安装

```shell
sudo yum groupinstall 'Development Tools'
sudo yum install -y openssl-devel git 
git clone https://github.com/wg/wrk.git wrk
cd wrk
make
# 将可执行文件移动到 /usr/local/bin 位置
sudo cp wrk /usr/local/bin
```



测试：  16核  400个并发  30秒

wrk -t16 -c400 -d30s http://192.168.2.44/api/platform/job/putIntoUseWarning