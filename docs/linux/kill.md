```
pid=`ps -ef|grep "agent.jar"|grep -v grep|awk '{print $2}'`
kill -9 $pid


```

