### 拉取代码：
系统业务代码：ssh://git@gitlab.ziggurat.cn:10000/taizhou/taizhou.git
任务调度代码：ssh://git@gitlab.ziggurat.cn:10000/taizhou/xxl-job.git
文件存储服务代码：ssh://git@gitlab.ziggurat.cn:10000/taizhou/upload-server.git

### 代码部署

- 部署准备

  - 设置mysql数据库统一编码：utf8mb4、utf8mb4_unicode_ci

  - 设置数据库忽略大小写

  - 创建数据库：taizhou_asc、taizhou_dic、taizhou_platform

  - 修改项目中连接mysql、redis相关配置

    

- 部署后端服务
   - kw-eureka、kw-asc、kw-dic、kw-zuul、taizhou-platform
   - 启动 
     - 进入服务目录 
     - 执行脚本run.bat启动

- 部署前端服务
   - taizhou-ui 
     - 配置环境文件地址 .env.production、.env.production.monitor
       - 执行打包命令：
         yarn build:prod
         yarn build:prodMon
     - 启动
       - 进入taizhou-ui 目录
       
       - (企业系统)执行启动脚本
       
         ```
         install.sh
         ```
       
         (监管系统)
       
       - 执行启动脚本
       
         ```
         install-mon.sh
         ```
- 部署xxljob
  
  - 进入xxl-job/xxl-job-admin下执行启动脚本
  
    ```
    sh deploy.sh
    ```
  
  - 进入xxl-job/xxl-job-executor-samples/xxl-job-executor-sample-springboot/target 下执行启动脚本
  
    ```
    sh deploy.sh
    ```

- 部署文件服务
   - 进入 upload-server 目录下执行启动脚本

     ```
     sh deploy.sh
     ```



bass:

企业：

综保区：comprehensive

企业：enterprise   

海关：customs








|               项目（目录）                |     服务器地址     |                             部署                             |
| :---------------------------------------: | :----------------: | :----------------------------------------------------------: |
| 企业平台-前端（/root/taizhou/taizhou-ui） |    192.168.2.44    | 192.168.2.42上执行 yarn build:prod   生成 dist-enterprise 包  scp到 192.168.2.44:/root/taizhou/taizhou-ui  执行脚本  sh install.sh |
| 监管平台-前端（/root/taizhou/taizhou-ui） |    192.168.2.45    | 192.168.2.42上执行 yarn build:prodMon   生成 dist-monitor 包  scp到 192.168.2.45:/root/taizhou/taizhou-ui  执行脚本  sh install-mon.sh |
| 业务服务(/root/taizhou/taizhou-platform)                | 192.168.2.42/44/45 |  cd到 /root/taizhou/taizhou-platform 下执行脚本  sh run.bat  |
| 网关服务(/root/taizhou/kw-zuul)         | 192.168.2.42/44/45 |      cd到 /root/taizhou/kw-zuul 下执行脚本  sh run.bat       |
|  注册中心服务(/root/taizhou/kw-eureka) | 192.168.2.42/44/45 | cd到 /root/taizhou/kw-eureka 下执行脚本  sh run.bat(注意服务ip地址，如果重新部署需要修改配置文件ip) |
|     数据字典服务(/root/taizhou/kw-dic) | 192.168.2.42/44/45 |       cd到 /root/taizhou/kw-dic 下执行脚本  sh run.bat       |
| 任务调度服务-管理端(/root/taizhou/xxl-job)    |    192.168.2.39    |     cd到 /root/xxl-job/xxl-job-admin 下执行脚本  sh deploy.sh      |
| 任务调度服务-执行器(/root/taizhou/xxl-job) |    192.168.2.39    |     cd到 /root/xxl-job/xxl-job-executor-samples/xxl-job-executor-sample-springboot 下执行脚本  sh deploy.sh      |
| 文件存储服务(/root/taizhou/upload-server) | 192.168.2.38 |       cd到 /root/upload-server 下执行脚本  sh deploy.sh       |
|               Mysql                | 192.168.2.221（主）192.168.2.43（从） | zhagnbo  !1qazxsw2@Z |
|               Redis                | 192.168.2.37 |       docker restart redis       |