# 端口映射

| 服务名              | Repo             | 主机端口  | 容器端口  | 容器名                   | 工作进度                                                |
|:-----------------|:-----------------|:-----:|:-----:|:----------------------|:----------------------------------------------------|
| 前端主站             | maxblog-main-fe  | 9601  | 9601  | maxblog-main-fe_main  | 主页：传入哪些数据x 文章× 样例：布局完成未检验复杂数据 项目× 统计x               |
| 前端后台             | maxblog-admin-fe | 9602  | 9602  | maxblog-admin-fe_main | 登录√ 其他x                                             |
| 中台统计             | maxblog-stats    | 9701  | 9701  | maxblog-stats_main    | 主页浏览量aa/bb ×  文章统计× 样例统计× 不与数据库相连，直接与主页后端通信         |
| 后端用户             | maxblog-user     | 9801  | 9801  | maxblog-user_main     | √√√√√√√√√                                           |
| 后端主页             | maxblog-main     | 9802  | 9802  | maxblog-main_main     | ×                                                   |
| SGW              | maxblog-sgw      | 9999  | 9999  | maxblog-sgw_main      | √√√√√√√√√√                                          |
| MySQL主           | -                | 3306  | 3306  | mysql_master          | √√√√√√√√√√                                          |
| MySQL从1          | -                | 3307  | 3306  | mysql_slave1          | ×                                                   |
| MySQL从2          | -                | 3308  | 3306  | mysql_slave2          | ×                                                   |
| Redis主           | -                | 6379  | 6379  | redis_master          | √√√√√√√√√√                                          |
| Redis从1          | -                | 6380  | 6379  | redis_slave1          | ×                                                   |
| Redis从2          | -                | 6381  | 6379  | redis_slave2          | ×                                                   |
| Postgres         | -                | 5432  | 5432  | sonar_db              | √√√√√√√√√√                                          |
| Vault            | -                | 8200  | 8200  | vault                 | √√√√√√√√√√                                          |
| Jenkins          | -                | 9000  | 8080  | jenkins               | √√√√√√√√√√                                          |
| SonarQube        | -                | 9001  | 9000  | sonarqube             | √√√√√√√√√√                                          |
| Harbor           | -                | 9002  | 8080  | nginx (harbor-xxx)    | √√√√√√√√√√                                          |
| ETCD leader      | -                | 2379  | 2379  | etcd0                 | √√√√√√√√√√  2380                                    |
| ETCD follower1   | -                | 12379 | 12379 | etcd1                 | √√√√√√√√√√  12380                                   |
| ETCD follower2   | -                | 22379 | 22379 | etcd2                 | √√√√√√√√√√  22380                                   |
| Consul           | -                | 8500  | 8500  | consul0 1 2 3         | √√√√√√√√√√  consul3是client                          |
| Jaeger           | -                | 6831  | 6831  | jaeger                | √√√√√√√√√√  16686是client  6832 5775 5778 14268 9411 |
| Prometheus       | -                | 9090  | 9090  | prometheus            | √√√√√√√√√√                                          |
| alertmanager     | -                | 9093  | 9093  | alertmanager          | √√√√√√√√√√                                          |
| cadvisor         | -                | 8080  | 8080  | cadvisor              | √√√√√√√√√√                                          |
| node_exporter    | -                | 9100  | 9100  | node_exporter         | √√√√√√√√√√                                          |
| nginx_exporter   | -                | 9113  | 9113  | nginx_exporter        | √√√√√√√√√√                                          |
| Grafana          | -                | 3000  | 3000  | grafana               | √√√√√√√√√√                                          |
| ElasticSearch    | -                | 9200  | 9200  | elasticsearch         | √√√√√√√√√√  9300                                    |
| Kibana           | -                | 5601  | 5601  | kibana                | √√√√√√√√√√                                          |
| Logstash         | -                | 5044  | 5044  | logstash              | √√√√√√√√√√                                          |
| Filebeat         | -                |   -   |   -   | filebeat              | √√√√√√√√√√                                          |
| Sentinel         | -                | 8858  | 8858  | sentinel              | √√√√√√√√√√                                          |
| RocketMQ-console | -                | 9877  | 8080  | rocketmq_console      | √√√√√√√√√√                                          |
| RocketMQ-namesrv | -                | 9876  | 9876  | rocketmq_namesrv      | √√√√√√√√√√                                          |
| RocketMQ-broker  | -                | 10909 | 10909 | rocketmq_broker       | √√√√√√√√√√  10911                                   |


# 端口映射

| 服务名       | Repo               | 主机端口 | 容器端口 | 容器名                | 工作进度                                  |
|:----------|:-------------------|:----:|:----:|:-------------------|:--------------------------------------|
| 前端主站      | maxblog-fe-main    | 9101 | 9101 | fe_main            | 主页：传入哪些数据x 文章× 样例：布局完成未检验复杂数据 项目× 统计x |
| 前端后台      | maxblog-fe-admin   | 9102 | 9102 | fe_admin           | 登录√ 其他x                               |
| ~~前端搜索~~  | maxblog-fe-search  | 9103 | 9103 | fe_search          | 使用vue3 ×                              |
| 中台后台      | maxblog-me-admin   | 9201 | 9201 | me_admin           | 用户√ 其他×                               |
| 中台主站      | maxblog-me-main    | 9202 | 9202 | me_main            | 主页× 文章× 样例√ 项目×                       |
| 中台统计      | maxblog-me-stats   | 9203 | 9203 | me_stats           | 主页浏览量aa/bb ×  文章统计× 样例统计×             |
| ~~中台搜索~~  | maxblog-me-search  | 9204 | 9204 | me_search          | ×                                     |
| 后端用户      | maxblog-be-user    | 9301 | 9301 | be_user            | √√√√√√√√√                             |
| 后端主页      | maxblog-be-main    | 9302 | 9302 | be_main            | ×                                     |
| ~~后端文章~~  | maxblog-be-article | 9303 | 9303 | be_article         | ×                                     |
| ~~后端样例~~  | maxblog-be-demo    | 9304 | 9304 | be_demo            | √√√√√√√√√                             |
| ~~后端项目~~  | maxblog-be-project | 9305 | 9305 | be_project         | ×                                     |
| MySQL主    | -                  | 3306 | 3306 | mysql_master       | √√√√√√√√√√                            |
| MySQL从1   | -                  | 3307 | 3306 | mysql_slave1       | ×                                     |
| MySQL从2   | -                  | 3308 | 3306 | mysql_slave2       | ×                                     |
| Redis主    | -                  | 6379 | 6379 | redis_master       | ×                                     |
| Redis从1   | -                  | 6380 | 6379 | redis_slave1       | ×                                     |
| Redis从2   | -                  | 6381 | 6379 | redis_slave2       | ×                                     |
| Postgres  | -                  | 5432 | 5432 | sonar_db           | √√√√√√√√√√                            |
| Jenkins   | -                  | 9000 | 8080 | jenkins            | √√√√√√√√√√                            |
| SonarQube | -                  | 9001 | 9000 | sonarqube          | √√√√√√√√√√                            |
| Harbor    | -                  | 9002 | 8080 | nginx (harbor-xxx) | √√√√√√√√√√                            |
| Consul    | -                  | 9003 | 8500 | consul             | ××××××××××                            |
| Nacos     | -                  | 9004 | 8848 | nacos              | ××××××××××                            |
