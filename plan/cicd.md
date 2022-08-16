# CI/CD指南

采用Jenkins Pipeline作为自动化CI的主要工具，
集成Harbor，SonarQube，golangci-lint，（js的ci lint），Nessus等工具。
放弃K8s部署方案。

## 1. 准备工作

### 1.1 VM配置要求
+ CPU：2核
+ 内存：1G
+ 硬盘空间：30G
+ 操作系统：Centos7.9

### 1.2 必备工具 - jdk，node，go
```shell
# 安装包位置
cd ~
mkdir pkg
cd pkg

# 解压安装包
# jdk8u333
tar -zxvf jdk-8u333-linux-aarch64.tar.gz -C /home/opc/tools
# node-v16
tar -zxvf node-v16.16.0.tar.gz -C /home/opc/tools
# go1.17
tar -zxvf go1.17.5.linux-amd64.tar.gz -C /home/opc/tools

# 修改文件名 （go不用改）
cd /home/opc/tools
mv jdk1.8.0_333 jdk
mv node-v16.16.0 node
```

### 1.3 必备工具 - docker，docker-compose
```shell
# docker
# 下载安装 要等好久
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
# 启动 重启用restart
sudo systemctl start docker
# 开机启动
sudo systemctl enable docker
# 检查安装结果
docker --version

# docker-compose
# 下载安装
sudo curl -L https://github.com/docker/compose/releases/download/1.23.2/docker-compose-`uname -s`-`uname -m` -o /usr/bin/docker-compose
# 增加执行权限
sudo chmod +x /usr/bin/docker-compose
# 检查安装结果
docker-compose --version
```

### 1.4 必备工具 - Jenkins
```shell
# Jenkins
# 拉取镜像（所用版本为下面）
docker pull jenkins/jenkins
sudo docker pull jenkins/jenkins:2.319.3-lts
# 创建docker-compose.yaml路径
cd ~
mkdir docker
cd docker
mkdir jenkins_docker
cd jenkins_docker
# 拷贝配置好的docker-compose.yaml（配置见下面yaml）
# 启动Jenkins
cd /home/ops/docker/jenkins_docker
sudo docker-compose up -d
# 赋予宿主机jenkins data目录权限
sudo chmod -R 777 data
# 重启Jenkins容器
sudo docker-compose restart
```

Jenkins配置文件docker-compose.yaml
```yaml
version: '3.1'
services:
  jenkins:
    image: 'jenkins/jenkins:2.319.3-lts'
    container_name: jenkins
    restart: always
    ports:
      - '9000:8080'
      - '50000:50000'
    volumes:
      - './data:/var/jenkins_home'
```


## 2. 配置Jenkins

### 2.1 初始化Jenkins
```shell
# 查看jenkins日志
sudo docker logs -f jenkins
```
找到日志里的密码，浏览器中访问jenkins，输入密码。<br/>
密码在`Please use the following password to proceed to installation:`后面。两坨星星中间夹着。

选择手动安装插件（右边按钮）。默认选项即可，直接点击安装。<br/>
如果失败，进入面板后找到`Mange Jenkins`→`Manage Plugins`→`Available`，手动安装<br/>
如果总是不成功，就更改为国内的插件源。

设置用户名密码。根据提示操作，直到进入到Welcome界面。

### 2.2 安装重要插件
`Manage Jenkins` → `Manage Plugins` → `Available` → `Search` `Git Parameter` → 勾选 → 
`Search` `Publish Over SSH` → 勾选 → 点击`Install without restart`


## 3. 流水线Pipeline

### 3.1 创建流水线
`New Item` → 输入名称 → `Pipeline` → OK

编写流水线脚本框架，并粘贴入Script区域

![流水线脚本.png](cicd/流水线脚本.png)

在图中`Pipeline Syntax`可进入生成指定功能脚本的页面，比如checkout功能的脚本

![生成语法.png](cicd/生成语法.png)

点击`Generate Pipeline Script`，复制代码。



