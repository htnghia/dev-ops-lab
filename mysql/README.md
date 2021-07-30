docker run --name mysql_inv -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d mysql

docker exec -it mysql_inv bash

mysql -u root -p

CREATE USER 'leo' IDENTIFIED BY '123456';

GRANT ALL PRIVILEGES ON * . * TO 'leo';

FLUSH PRIVILEGES;

exit;

mysql -u leo -p

CREATE DATABASE dacmsinv;