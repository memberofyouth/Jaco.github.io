```shell
echo "nohup java -jar agent.jar -jnlpUrl http://192.168.0.31/computer/prod-57/jenkins-agent.jnlp -secret @secret-file -workDir "/home/software/jenkins-agent" &" >> start.sh

chmod u+x start.sh
```

