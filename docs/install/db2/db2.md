```html
docker run -d -p 50000:50000 --name db2 --privileged=true -e DB2INST1_PASSWORD=123456 -e DBNAME=testdb -e LICENSE=accept -v G:/dump/db2:/database ibmcom/db2

```

