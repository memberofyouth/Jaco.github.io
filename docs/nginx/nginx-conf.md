## nginx.conf

```
events {
    accept_mutex on;   #设置网路连接序列化，防止惊群现象发生，默认为on
    multi_accept on;  #设置一个进程是否同时接受多个网络连接，默认为off
    #use epoll;      #事件驱动模型，select|poll|kqueue|epoll|resig|/dev/poll|eventport
    worker_connections  1024;    #最大连接数，默认为512
}
http {
    include       mime.types;   #文件扩展名与文件类型映射表
    default_type  application/octet-stream; #默认文件类型，默认为text/plain
    #access_log off; #取消服务日志
    log_format myFormat '$remote_addr–$remote_user [$time_local] $request $status $body_bytes_sent $http_referer $http_user_agent $http_x_forwarded_for'; #自定义格式

    sendfile on;   #允许sendfile方式传输文件，默认为off，可以在http块，server块，location块。
    sendfile_max_chunk 100k;  #每个进程每次调用传输数量不能大于设定的值，默认为0，即不设上限。
    keepalive_timeout 65;  #连接超时时间，默认为75s，可以在http，server，location块。

   #配置上游服务器网关端口集群,默认轮询机制
   upstream gateway {
        server 192.168.2.42:9082;
        server 192.168.2.44:9082;
        server 192.168.2.45:9082;
    }

   server {
    listen 80;
    # gzip config
    gzip on;
    gzip_min_length 1k;
    gzip_comp_level 9;
    gzip_types text/plain application/javascript application/x-javascript text/css application/xml text/javascript application/x-httpd-php image/jpeg image/gif image/png;
    gzip_vary on;
    gzip_disable "MSIE [1-6]\.";

    proxy_intercept_errors on;
    fastcgi_intercept_errors on;

    add_header Access-Control-Allow-Methods 'GET,POST';
    keepalive_timeout  150;  #保持

    error_page 404 /404.html; #错误页

    location / {
 	root /usr/share/nginx/html;
	index index.html;
    }

   location /upload/ {
        proxy_pass http://192.168.2.38:9089/;
        proxy_set_header   X-Forwarded-Proto $scheme;

        client_max_body_size    20m;
        #ip
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;  #获取客户端真实IP
        proxy_set_header REMOTE-HOST $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /api/ {
        proxy_pass http://gateway/;
        proxy_set_header   X-Forwarded-Proto $scheme;

        #ip
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;  #获取客户端真实IP
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

	location /block/ {
         proxy_pass http://192.168.2.240:30080/;
         proxy_set_header   X-Forwarded-Proto $scheme;
         proxy_set_header   X-Real-IP         $remote_addr;
	}

    location = /404.html {
        root /usr/share/nginx/error;
    }

    location /images {
            alias /usr/share/nginx/error;
            autoindex on;
    }

   }

}

```



```
server {
     listen       9000;
     server_name  localhost;

     location  ~ .*\.(gif|jpg|jpeg|png)$ {
            expires 24h;
            root  /zg/uploadPath; #指定图片存放路径  
            proxy_store on;  
            proxy_temp_path     /zg/uploadPath/;#图片访问路径  
            proxy_redirect     off;
            proxy_set_header    Host 192.168.0.179;  
            client_max_body_size  10m;
            client_body_buffer_size 1280k;  
            proxy_connect_timeout  900;  
            proxy_send_timeout   900;  
            proxy_read_timeout   900;  
            proxy_buffer_size    40k;  
            proxy_buffers      40 320k;  
            proxy_busy_buffers_size 640k;  
            proxy_temp_file_write_size 640k;  
            if ( !-e $request_filename)
              {
                 proxy_pass http://127.0.0.1:9001; #默认80端口  
              }
        }
    }
```

