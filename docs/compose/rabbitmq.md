```yml
version: '3'
services:
  rabbitmq:
    image: rabbitmq:management
    container_name: rabbitmq
    restart: always
    hostname: my-rabbitmq
    ports:
      - 15672:15672
      - 5672:5672
    volumes:
      - /home/rabbitmq/data:/var/lib/rabbitmq
    environment:
      - RABBITMQ_DEFAULT_USER=rabbitmq
      - RABBITMQ_DEFAULT_PASS=rabbitmq

```







