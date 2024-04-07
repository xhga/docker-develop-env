FROM mysql:8.3.0

# nacos 中间件所需的数据库 ↓ （如果不需要nacos 可以将下面两行注释掉）
ADD https://raw.githubusercontent.com/alibaba/nacos/develop/distribution/conf/mysql-schema.sql /docker-entrypoint-initdb.d/nacos-mysql.sql
RUN chown -R mysql:mysql /docker-entrypoint-initdb.d/nacos-mysql.sql
# nacos 中间件所需的数据库 ↑

EXPOSE 3306
CMD ["mysqld", "--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci"]