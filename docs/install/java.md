#### 安装jdk

​       1.上传jdk, tar -zxvf 解压

​       2.创建java存放目录   

​		  `` mkdir /usr/local/java``

3. 将解压后的文件内容，拷贝到新建的目录（/usr/local/java）下：

   ``mv xxx /usr/local/java``

#### 配置环境变量 vi /etc/profile 在之后添加

```bash
export JAVA_HOME=/usr/local/java/jdk1.8.0_271
export CLASSPATH=.:$JAVA_HOME/jre/lib/rt.jar:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
export PATH=$PATH:$JAVA_HOME/bin
```

#### 刷新配置

. /etc/profile



#### 添加软链接
ln -s /usr/local/java/jdk1.8.0_171/bin/java /usr/bin/java

java -version 查看