# 端口映射

| 服务名       | Repo               | 主机端口 | 容器端口 | 容器名                |
|:----------|:-------------------|:----:|:----:|:-------------------|
| 前端主页      | maxblog-fe-main    | 9101 |  80  | fe_main            |
| 前端后台      | maxblog-fe-admin   | 9102 |  80  | fe_admin           |
| 前端搜索      | maxblog-fe-search  | 9103 |  80  | fe_search          |
| 中台后台      | maxblog-me-admin   | 9201 | 8080 | me_admin           |
| 中台主页      | maxblog-me-home    | 9202 | 8080 | me_home            |
| 中台文章      | maxblog-me-article | 9203 | 8080 | me_article         |
| 中台样例      | maxblog-me-demo    | 9204 | 8080 | me_demo            |
| 中台项目      | maxblog-me-project | 9205 | 8080 | me_project         |
| 中台搜索      | maxblog-me-search  | 9206 | 8080 | me_search          |
| 后端后台      | maxblog-be-admin   | 9301 | 8080 | be_admin           |
| 后端主页      | maxblog-be-home    | 9302 | 8080 | be_home            |
| 后端文章      | maxblog-be-article | 9303 | 8080 | be_article         |
| 后端样例      | maxblog-be-demo    | 9304 | 8080 | be_demo            |
| 后端项目      | maxblog-be-project | 9305 | 8080 | be_project         |
| 后端搜索      | maxblog-be-search  | 9306 | 8080 | be_search          |
| 后端缓存      | maxblog-be-cache   | 9307 | 8080 | be_cache           |
| 后端统计      | maxblog-be-stats   | 9308 | 8080 | be_stats           |
| MySQL主    | -                  | 3306 | 3306 | mysql_master       |
| MySQL从1   | -                  | 3307 | 3306 | mysql_slave1       |
| MySQL从2   | -                  | 3308 | 3306 | mysql_slave2       |
| Redis主    | -                  | 6379 | 6379 | redis_master       |
| Redis从1   | -                  | 6380 | 6379 | redis_slave1       |
| Redis从2   | -                  | 6381 | 6379 | redis_slave2       |
| Postgres  | -                  | 5432 | 5432 | sonar_db           |
| Jenkins   | -                  | 9000 | 8080 | jenkins            |
| SonarQube | -                  | 9001 | 9000 | sonarqube          |
| Harbor    | -                  | 9002 | 8080 | nginx (harbor-xxx) |
