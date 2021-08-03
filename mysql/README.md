## docker:
# with volume
docker run --name mysql -v ~/dev/docker_volume/mysql/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 mysql

# without volume
docker run --name mysql_inv -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d mysql

## create database:
docker exec -it mysql_inv bash

mysql -u root -p

CREATE USER 'leo' IDENTIFIED BY '123456';

GRANT ALL PRIVILEGES ON * . * TO 'leo';

FLUSH PRIVILEGES;

exit;

mysql -u leo -p

CREATE DATABASE dacmsinv;

## clone db

mysqldump -u leo --password=123456 dacmsinv | mysql -u leo -p tmp

## mysql connection and driver
connection URL: jdbc:mysql://localhost:3306/dacmsinv?useSSL=false&allowMultiQueries=true&serverTimezone=UTC
driver class: com.mysql.jdbc.Driver
driver path: ~/Library/DBeaverData/drivers/maven/maven-central/mysql/mysql-connector-java-8.0.17.jar