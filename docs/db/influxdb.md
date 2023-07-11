安装

```yml
version: '3.8'

volumes:
  influxdb:

services:
  docker-influxdb:
    image: influxdb:1.7.8
    container_name: influxdb
    restart: always
    ports:
      - "8086:8086" #HTTP UI and API port
    environment:
      - INFLUXDB_ADMIN_USER=influxdb
      - INFLUXDB_ADMIN_PASSWORD=influxdb
      - INFLUXDB_DB=second_market
    volumes:
      - influxdb:/root/influxdb/data

```







![image-20221206234526854](https://gitee.com/mrzlive/picture-bed/raw/master/picture/202212062345106.png)



show databases;

create database second_market;

drop database second_market;

user second_market;

clear db;



insert into logs,name=blr age=23,address=shanghai



