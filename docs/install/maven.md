wget https://mirrors.tuna.tsinghua.edu.cn/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz





tar -xf apache-maven-3.6.3-bin.tar.gz -C /usr/local/

mv /usr/local/apache-maven-3.6.3 /usr/local/maven3.6

export PATH=$PATH:/usr/local/maven3.6/bin





配置mirror



<mirror> 
         <id>alimaven</id> 
         <name>aliyun maven</name> 
         <url>https://maven.aliyun.com/nexus/content/groups/public/</url> 
         <mirrorOf>central</mirrorOf> 
     </mirror>



配置jdk

 <profile>
      <id>jdk-1.8</id>
      <activation>
        <activeByDefault>true</activeByDefault>
        <jdk>1.8</jdk>
      </activation>
      <properties>
        <maven.compiler.source>1.8</maven.compiler.source>
        <maven.compiler.target>1.8</maven.compiler.target>
        <maven.compiler.compilerVersion>1.8</maven.compiler.compilerVersion>
      </properties>
    </profile>













