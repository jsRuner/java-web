# lnmp

java web的容器编排。多容器组合。

实现对项目多个服务的编排：nginx、mysql、tomcat。一键启动和销毁。支持配置的修改和日志的查看。方便开发和测试。


# 结构
- nginx容器负责前端web
- tomcat负责后端接口
- mysql 负责数据存储

```	
	.
├── README.md
├── db_data             mysql的数据存储目录
├── docker-compose.yml
├── logs    日志目录
│   ├── mysql
│   │   ├── error.log
│   │   ├── mysql.log
│   │   └── slow.log
│   ├── nginx
│   │   ├── access.log
│   │   ├── error.log
│   │   └── log
│   │       └── host.access.log
│   └── tomcat
│       └── error.log
├── mysql   mysql的配置和dockerfile
│   ├── Dockerfile
│   └── mysql.conf.d
│       └── mysqld.cnf
├── nginx   ngxinx的配置
│   ├── Dockerfile
│   ├── default.conf
│   └── nginx.conf
├── tomcat    tomcat的配置
│   ├── Dockerfile
│   ├── server.xml
│   └── tomcat-users.xml
└── web_data    项目代码
    ├── web     前端代码。 
    └── webapps   后端代码。建议放入war包。已经配置了自动解压war
    
```



## 版本-最新版本。

- nginx  latest
- mysql  latest
- tomcat  latest

## 命令


- 编译服务

	```
	docker-compose build --force-rm --no-cache
	
	```
- 启动服务

	```
	docker-compose up -d --force-recreate
	
	```

- 停止服务

	```
	docker-compose stop
	```
- 查看某个容器的日志。查看34aa的容器运行的日志。

	尤其容器启动失败的时候，很需要这个。

	```
	docker logs 34aa
	```

## 数据库的配置
- 地址 127.0.0.1
- 端口3306   
- 用户 root/123456  test/123456
- 数据库 testdb


