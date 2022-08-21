# 端口映射

| 服务名       | Repo               | 主机端口  | 容器端口 | 容器名                |
|:----------|:-------------------|:-----:|:----:|:-------------------|
| 前端主页      | maxblog-fe-main    | 10080 |  80  | fe_main            |
| 前端后台      | maxblog-fe-admin   | 10081 |  80  | fe_admin           |
| 前端搜索      | maxblog-fe-search  | 10082 |  80  | fe_search          |
| 后端综合      | maxblog-be-general | 11001 | 8080 | be_general         |
| 后端后台      | maxblog-be-admin   | 11002 | 8080 | be_admin           |
| 后端搜索      | maxblog-be-search  | 11003 | 8080 | be_search          |
| 后端文章      | maxblog-be-article | 11004 | 8080 | be_article         |
| 后端样例      | maxblog-be-demo    | 11005 | 8080 | be_demo            |
| 后端项目      | maxblog-be-project | 11006 | 8080 | be_project         |
| 后端数据库     | maxblog-be-db      | 11007 | 8080 | be_db              |
| 后端缓存      | maxblog-be-cache   | 11008 | 8080 | be_cache           |
| 后端统计      | maxblog-be-stats   | 11009 | 8080 | be_stats           |
| MySQL主    | -                  | 3306  | 3306 | mysql_master       |
| MySQL从1   | -                  | 3307  | 3306 | mysql_slave1       |
| MySQL从2   | -                  | 3308  | 3306 | mysql_slave2       |
| Redis主    | -                  | 6379  | 6379 | redis_master       |
| Redis从1   | -                  | 6380  | 6379 | redis_slave1       |
| Redis从2   | -                  | 6381  | 6379 | redis_slave2       |
| Postgres  | -                  | 5432  | 5432 | sonar_db           |
| Jenkins   | -                  | 9000  | 8080 | jenkins            |
| SonarQube | -                  | 9001  | 9000 | sonarqube          |
| Harbor    | -                  | 9002  | 8080 | nginx (harbor-xxx) |
