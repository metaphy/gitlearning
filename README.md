**PHP installation
Version:
    peter@~ $ php -v
    PHP 7.2.19-0ubuntu0.18.04.1 (cli) (built: Jun  4 2019 14:48:12) ( NTS )  
Installation path:
    Loaded Configuration File	/etc/php/7.2/apache2/php.ini
    Configuration File (php.ini) Path	/etc/php/7.2/apache2
    Scan this dir for additional .ini files	/etc/php/7.2/apache2/conf.d
HTML path:  /var/www/html


**MySQL installation
MySQL configuration:
    sudo mysql_secure_installation
    Check MySQL service:  systemctl status mysql.service
sudo mysql -v
    version:Server version: 5.7.26-0ubuntu0.18.04.1 (Ubuntu)
List DBs:
    show databases;
    select * from table limit 10;
load sql:
    sudo mysql -u root -p yuweishi < /home/peter/workspace2/yuweishi.sql
    Password for root@local db: Xing....
MySQL Server Port:
    mysql> show variables where Variable_name ='port';

ERROR: SQLSTATE[HY000] [1698] Access denied for user 'root'@'localhost'
Create new user and use it instead of Root:
    sudo mysql -p -u root
    CREATE USER 'pmauser'@'%' IDENTIFIED BY '----PASSWROD----';
    GRANT ALL PRIVILEGES ON *.* TO 'pmauser'@'%' WITH GRANT OPTION;


application/config/config.php
application/config/database.php

CREATE DATABASE yuweishi CHARACTER SET utf8 COLLATE utf8_general_ci;
-----------------------------------------------------------------------------

1. 网站运行的PHP/MySQL 版本分别是什么？
PHP 7.1     mysql5.6

2. 最新的代码是这个吗 -- 0429-full?
 是的
网站上有没有比0429-full更新的code?
 ftp可以自己下载


3. 后台入口admin.php 没找到...

upload		- 文件上传目录

index.php	- 首页入口文件
/var/www/html/application/controllers/U_user.php

admin.php	- 后台入口文件
/var/www/html/application/controllers/index.php


ywsw780593-AA$$$

-----------------------------------------------------------------------------
mysql -u root -p yuweishi < /tmp/yuweishi.sql


