```yml
version: '2.0'
services:
  nginx:
    container_name: nginx
    image: nginx
    ports:
      - 80:80
      - 443:443
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
      - /home/integral/ui/build:/usr/share/nginx/html
      - ./logs:/var/log/nginx
       # - ./nginx/default.conf:/etc/nginx/conf.d/default.conf
    restart: always
```

