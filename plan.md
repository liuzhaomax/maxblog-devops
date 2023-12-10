# 计划

## 1. 负载均衡
云+Nginx

## 2. 网关和鉴权
微服务

## 3. 注册中心
ETCD

## 4. 配置中心
Nacos

## 5. 监控中心
Prometheus+Grafana/Kibana

## 6. 日志中心
Jaeger/fileBeat+Logstash日志链路追踪，ElasticSearch持久化

## 7. 消息队列
RocketMQ

## 8. 分布式事务
DTM

## 9. 缓存
Redis

## 10. 数据库
MySQL

## 11. 集群
OCP4

## 12. CI/CD
Jenkins流水线
1. checkout
2. app version
3. lint: golangci-lint
4. build
5. 静态扫描: sonarqube
6. 漏洞扫描: nessus
7. 安全扫描: blackduck
8. build image Harbour
9. git tag
10. package config
11. create package
12. deploy package
