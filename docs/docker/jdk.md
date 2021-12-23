#### Java8 带字体

```yml
·1 ### 创建 Dockerfile 
FROM java:8-jre-alpine
# Install cURL
RUN echo -e "https://mirror.tuna.tsinghua.edu.cn/alpine/v3.4/main\n\
https://mirror.tuna.tsinghua.edu.cn/alpine/v3.4/community" > /etc/apk/repositories

RUN apk --update add curl bash ttf-dejavu && \
      rm -rf /var/cache/apk/*

·2 ### 构建镜像
docker build -t docker.io/java-font:8-jre-alpine .

```

