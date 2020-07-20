# MySQL Docker


docker-compose.yml

```yaml
version: '3.2'
services:
  spring-beet-mariadb:
    image: coolbeevip/docker-MySQL
    hostname: spring-beet-mysql
    container_name: spring-beet-mysql
    ports:
      - '3306:3306'
    volumes:
      - ~/mydocker/docker_volume/spring-beet-mysql/data:/var/lib/mysql
      - ~/mydocker/docker_volume/spring-beet-mysql/conf:/etc/mysql/conf.d
    environment:
      - TZ=Asia/Shanghai
      - MYSQL_ROOT_PASSWORD=root
      - MYSQL_DATABASE=mydb
      - MYSQL_USER=mydb-user
      - MYSQL_PASSWORD=mydb-pass
```

端口

```
3306
```

环境变量

```properties
MYSQL_ROOT_PASSWORD=<root_password> #root密码，默认111111
MYSQL_DATABASE=<dbname1>,<dbname2> #数据库名,多个逗号分隔
MYSQL_USER=<dbuser1>,<dbuser2> #数据库用户,多个逗号分隔
MYSQL_PASSWORD=<dbpass1>,<dbpass2> #数据库用户密码,多个逗号分隔
```

卷

```
/app
```
