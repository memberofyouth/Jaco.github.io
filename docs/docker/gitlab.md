```yml
version: '3.6'
services:
  gitlab:
    container_name: gitlab.dazzlemagnet.com
    image: gitlab/gitlab-ce:latest
    environment:
      - GITLAB_HOME=/gitlab
    hostname: gitlab
    volumes:
      - ./config:/etc/gitlab
      - ./logs:/var/log/gitlab
      - ./data:/var/opt/gitlab
    restart: always
    ports:
      - "80:80"
      - "2222:22" 
      - "443:443"

```

修改 config 中 gitlab.rb 配置

`external_url 'http://192.168.0.29'`

进入容器修改管理员密码

cd /opt/gitlab/bin

执行  **gitlab-rails console -e production**



在irb(main):001:0> 后面通过 u=User.where(id:1).first 来查找与切换账号（User.all 可以查看所有用户）



通过 u.password='12345678' 设置密码为12345678



通过u.password_confirmation='12345678' 再次确认密码



通过 u.save!进行保存


