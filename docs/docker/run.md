```yml
docker rm -f integral-platform
docker build -t integral-platform .
docker run --name integral-platform -p 8086:8086 -d integral-platform
docker  ps
docker logs -f --tail=200 integral-platform

```

